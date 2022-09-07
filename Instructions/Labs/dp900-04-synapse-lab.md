---
lab:
  title: استكشاف تحليلات البيانات في Azure باستخدام Azure Synapse Analytics
  module: Explore fundamentals of large-scale data warehousing
---

# <a name="explore-data-analytics-in-azure-with-azure-synapse-analytics"></a>استكشاف تحليلات البيانات في Azure باستخدام Azure Synapse Analytics

في هذا الإجراء، ستقوم بتوفير وظيفة مساحة عمل Azure Synapse Analytics في اشتراكك في Azure، واستخدامها لمعالجة البيانات وتحريها.

سيستغرق إكمال هذا التمرين المعملي **30** دقيقة.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="provision-an-azure-synapse-analytics-workspace"></a>توفير مساحة عمل Azure Synapse Analytics

لاستخدام Azure Synapse Analytics، يجب توفير مورد مساحة عمل Azure Synapse Analytics في اشتراك Azure.

1. افتح مدخل Microsoft Azure على [https://portal.azure.com](https://portal.azure.com?azure-portal=true)، وقم بتسجيل الدخول باستخدام حساب Microsoft المقترن باشتراك Azure.

    > <bpt id="p1">**</bpt>Tip<ept id="p1">**</ept>:  Ensure you are working in the directory containing your subscription - indicated at the top right under your user ID. If not, select the user icon and switch directory.

2. في مدخل Microsoft Azure، في صفحة **"Home"**، استخدم **&#65291; إنشاء رمز مورد** لإنشاء مورد جديد.
3. ابحث عن *Azure Synapse Analytics*، وإنشاء مورد **Azure Synapse Analytics** جديد باستخدام الإعدادات التالية:
    - **الاشتراك**: *اشتراكك في Azure*
        - **Resource group**: *إنشاء مجموعة موارد جديدة ذات اسم فريد مثل "synapse-rg"*
        - **مجموعة الموارد المُدارة**: *أدخل اسماً مناسباً، على سبيل المثال "synapse-managed-rg"*.
    - **Workspace name**: *أدخل اسماً فريداً لمساحة العمل، على سبيل المثال "synapse-ws-<your_name>"* .
    - **«المنطقة»**: *حدد أيا من المناطق التالية*:
        - شرق أستراليا
        - وسط الولايات المتحدة
        - East US 2
        - شمال أوروبا
        - جنوب وسط الولايات المتحدة
        - جنوب شرق آسيا
        - جنوب المملكة المتحدة
        - غرب أوروبا
        - غرب الولايات المتحدة
        - WestUS 2
    - **حدد "Data Lake Storage Gen 2"**: من الاشتراك
        - **اسم الحساب**: *إنشاء حساب جديد باسم فريد، على سبيل المثال "<your_name> datalake"*.
        - **اسم نظام الملفات**: *إنشاء نظام ملفات جديد باسم فريد، على سبيل المثال "fs<your_name>"*.

    > <bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: A Synapse Analytics workspace requires two resource groups in your Azure subscription; one for resources you explicitly create, and another for managed resources used by the service. It also requires a Data Lake storage account in which to store data, scripts, and other artifacts.

4. عند إدخال هذه التفاصيل، حدد **"Review + create"**، ثم حدد **"Create"** لإنشاء مساحة العمل.
5. انتظر حتى يتم إنشاء مساحة العمل - قد يستغرق ذلك خمس دقائق أو نحو ذلك.
6. عند اكتمال التوزيع انتقل إلى مجموعة الموارد التي تم إنشاؤها ولاحظ أنه يحتوي على مساحة عمل Synapse Analytics وحساب تخزين مستودع البيانات.
7. حدد مساحة عمل Synapse، وفي صفحة **"Overview"** الخاصة بها، في بطاقة **"Open Synapse Studio"**، حدد **"Open"** لفتح Synapse Studio في علامة تبويب متصفح جديدة. Synapse Studio هي واجهة قائمة على الويب يمكنك استخدامها للعمل مع مساحة عمل Synapse Analytics.
8. على الجانب الأيسر من استوديو Synapse، استخدم الرمز **&rsaquo;&rsaquo;** لتوسيع القائمة - وهذا يكشف عن الصفحات المختلفة داخل Synapse Studio التي ستستخدمها لإدارة الموارد وتنفيذ مهام تحليل البيانات، كما هو موضح هنا:

    ![صورة تعرض قائمة Synapse Studio المُوسّعة لإدارة الموارد وتنفيذ مهام تحليل البيانات](images/synapse-studio.png)

## <a name="ingest-data"></a>استيعاب البيانات

واحدة من المهام الرئيسية التي يمكنك القيام بها مع Azure Synapse Analytics هي تحديد *البنية الأساسية لبرنامج ربط العمليات التجارية* التي تنقل (وإذا لزم الأمر، تُحوّل) البيانات من مجموعة واسعة من المصادر إلى مساحة العمل الخاصة بك للتحليل.

1. في Synapse Studio، في صفحة **Home**، حدد **Ingest** ثم حدد **Built-in copy task** لفتح أداة **Copy Data tool**.
2. في أداة Copy Data، في خطوة **"Properties"**، تأكد من تحديد **"Built-in copy task"** و **"Run once now"**، ثم انقر فوق **"Next >"**.
3. في خطوة **"Source"** في الخطوة الفرعية **"Dataset"** حدد الإعدادات التالية:
    - **Source type**: الكل
    - **Connection**: *أنشئ اتصالا جديدا، وفي جزء **Linked service** الذي يظهر، في علامة التبويب **File**، حدد **HTTP**. ثم تابع وأنشئ اتصالا بملف بيانات باستخدام الإعدادات التالية:*
        - **"Name"**: منتجات شركة مغامرة
        - **"Description"**: قائمة المنتجات عبر HTTP
        - **"Connect via integration runtime"**: AutoResolveIntegrationRuntime
        - **"Base URL"**: `https://raw.githubusercontent.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/master/Azure-Synapse/products.csv`
        - **"Server Certificate Validation"**: تمكين
        - **"Authentication type"**: مجهول
4. بعد إنشاء الاتصال، على الخطوة الفرعية **"Source/Dataset"** تأكد من تحديد الإعدادات التالية، ثم حدد **"Next >"**:
    - **"Source/Dataset"**: *اتركه فارغاً*
    - **طريقة الطلب**: GET
    - **عناوين إضافية**: *اتركه فارغاً*
    - **نسخة ثنائية**: <u>غير</u> مُحدد
    - **مُهلة الطلب**: *اتركه فارغاً*
    - **أقصى الاتصالات المتزامنة**: *اتركه فارغاً*
5. في خطوة **"Source"** في الخطوة الفرعية **"Configuration"** حدد **"Preview data"** لرؤية معاينة بيانات المنتج التي سيتم استيعابها في البنية الأساسية لبرنامج ربط العمليات التجارية، ثم أغلق المعاينة.
6. بعد معاينة البيانات، في خطوة **"Source/Configuration"** الفرعية تأكد من تحديد الإعدادات التالية، ثم حدد **"Next >"**:
    - **File format**: DelimitedText
    - **عمود محدِّد**: فاصلة (،)
    - **صف محدِّد**: موجز الخط (\n)
    - **"First row as header"**: محدَّد
    - **"Compression type"**: بلا
7. في خطوة **"Target"** في الخطوة الفرعية **"Dataset"** حدد الإعدادات التالية:
    - **Target type**: Azure Data Lake Storage Gen 2
    - **Connection**: *حدد الاتصال الموجود بمخزن مستودع البيانات (تم إنشاء هذا لك عند إنشاء مساحة العمل).*
8. بعد تحديد الاتصال، في الخطوة **Target/Dataset** تأكد من تحديد الإعدادات التالية، ثم حدد "**Next >** ":
    - **مسار الملف**: *استعرض للوصول إلى مجلد نظام الملفات*
    - **اسم الملف**: منتجات.csv
    - **سلوك النسخ**: بلا
    - **أقصى الاتصالات المتزامنة**: *اتركه فارغاً*
    - **حجم الكتلة (ميغا بايت)**: *اتركه فارغاً*
9. On the <bpt id="p1">**</bpt>Target<ept id="p1">**</ept> step, in the <bpt id="p2">**</bpt>Configuration<ept id="p2">**</ept> substep, ensure that the following properties are selected. Then select <bpt id="p1">**</bpt>Next &gt;<ept id="p1">**</ept>:
    - **File format**: DelimitedText
    - **عمود محدِّد**: فاصلة (،)
    - **صف محدِّد**: موجز الخط (\n)
    - **"Add header to file"**: مُحدَّد
    - **"Compression type"**: بلا
    - **"Max rows per file"**: *اتركه فارغاً*
    - **"File name prefix"**: *اتركه فارغاً*
10. في خطوة **"Settings"** أدخل الإعدادات التالية ثم انقر فوق **"Next >"**:
    - **اسم المهمة**: نسخ المنتجات
    - **وصف المهمة** نسخ بيانات المنتجات
    - **التسامح مع الخطأ**: *اتركه فارغاً*
    - **تمكين التسجيل**: <u>إلغاء</u> التحديد
    - **تمكين التشغيل المرحلي**: <u>إلغاء</u> التحديد
11. في خطوة **"Review and finish"** في الخطوة الفرعية **"Review"** اقرأ الملخص ثم انقر فوق **"Next >"**.
12. في خطوة **"Deployment"** انتظر البنية الأساسية لبرنامج ربط العمليات التجارية ليتم توزيعها ثم انقر فوق **"Finish"**.
13. في Synapse Studio، حدد صفحة "**Monitor**"، وفي علامة التبويب "**Pipeline runs**"، انتظر حتى اكتمال البنية الأساسية لبرنامج ربط العمليات التجارية "**Copy products**" بحالة "**Succeeded**" (يمكنك استخدام الزر " **&#8635; Refresh**" في صفحة "Pipeline runs" لتحديث الحالة).
14. On the <bpt id="p1">**</bpt>Data<ept id="p1">**</ept> page, select the <bpt id="p2">**</bpt>Linked<ept id="p2">**</ept> tab and expand the <bpt id="p3">**</bpt>Azure Data Lake Storage Gen 2<ept id="p3">**</ept> hierarchy until you see the file storage for your Synapse workspace. Then select the file storage to verify that a file named <bpt id="p1">**</bpt>products.csv<ept id="p1">**</ept> has been copied to this location, as shown here:

    ![صورة توضح عرض Synapse Studio الموسع لتدرج Azure Data Lake Storage Gen 2 الهرمي مع تخزين الملفات لمساحة عمل Synapse](images/synapse-storage.png)

## <a name="use-a-sql-pool-to-analyze-data"></a>استخدام تجمع SQL لتحليل البيانات

Now that you've ingested some data into your workspace, you can use Synapse Analytics to query and analyze it. One of the most common ways to query data is to use SQL, and in Synapse Analytics you can use a <bpt id="p1">*</bpt>SQL pool<ept id="p1">*</ept> to run SQL code.

1. في Synapse Studio، انقر بزر الماوس الأيمن فوق ملف **"products.csv"** في تخزين الملفات لمساحة عمل Synapse، أشر إلى **البرنامج النصي SQL الجديد**وحدد **"Select TOP 100 rows"**.
2. في جزء **SQL Script 1** الذي يفتح، راجع التعليمات البرمجية لـ SQL التي تم إنشاؤها، والتي يجب أن تكون مشابهة لهذا:

    ```SQL
    -- This is auto-generated code
    SELECT
        TOP 100 *
    FROM
        OPENROWSET(
            BULK 'https://datalakexx.dfs.core.windows.net/fsxx/products.csv',
            FORMAT = 'CSV',
            PARSER_VERSION='2.0'
        ) AS [result]
    ```

    يفتح هذا الرمز مجموعة سجلات من الملف النصي الذي قمت باستيراده ويسترد أول 100 سجل من البيانات.

3. في قائمة **الاتصال بـ**، تأكد من تحديد **"Built-in"** - يمثل هذا تجمّع SQL المُدمج الذي تم إنشاؤه باستخدام مساحة العمل الخاصة بك.
4. على شريط الأدوات، استخدم الزر **"&#9655; Run"** لتشغيل التعليمات البرمجية لـ SQL، ومراجعة النتائج، والتي يجب أن تبدو مشابهة لهذا:

    | C1 | c2 | c3 | c4 |
    | -- | -- | -- | -- |
    | ProductID | ProductName | الفئة | ListPrice |
    | 771 | Mountain-100 Silver, 38 | Mountain Bikes | 3399.9900 |
    | 772 | Mountain-100 Silver, 42 | Mountain Bikes | 3399.9900 |
    | ... | ... | ... | ... |

5. Note the results consist of four columns named C1, C2, C3, and C4; and that the first row in the results contains the names of the data fields. To fix this problem, add a HEADER_ROW = TRUE parameters to the OPENROWSET function as shown here (replacing <bpt id="p1">*</bpt>datalakexx<ept id="p1">*</ept> and <bpt id="p2">*</bpt>fsxx<ept id="p2">*</ept> with the names of your data lake storage account and file system), and then rerun the query:

    ```SQL
    SELECT
        TOP 100 *
    FROM
        OPENROWSET(
            BULK 'https://datalakexx.dfs.core.windows.net/fsxx/products.csv',
            FORMAT = 'CSV',
            PARSER_VERSION='2.0',
            HEADER_ROW = TRUE
        ) AS [result]
    ```

    الآن تبدو النتائج كما يلي:

    | ProductID | ProductName | الفئة | ListPrice |
    | -- | -- | -- | -- |
    | 771 | Mountain-100 Silver, 38 | Mountain Bikes | 3399.9900 |
    | 772 | Mountain-100 Silver, 42 | Mountain Bikes | 3399.9900 |
    | ... | ... | ... | ... |

6. تعديل الاستعلام كما يلي (استبدال *datalakexx* و*fsxx* بأسماء حساب تخزين مستودع البيانات ونظام الملفات):

    ```SQL
    SELECT
        Category, COUNT(*) AS ProductCount
    FROM
        OPENROWSET(
            BULK 'https://datalakexx.dfs.core.windows.net/fsxx/products.csv',
            FORMAT = 'CSV',
            PARSER_VERSION='2.0',
            HEADER_ROW = TRUE
        ) AS [result]
    GROUP BY Category;
    ```

7. تشغيل الاستعلامات المعدّلة التي يجب أن يعرض مجموعة النتائج التي تحتوي على عدد المنتجات في كل فئة، مثل هذا:

    | الفئة | عدد المنتجات |
    | -- | -- |
    | Bib-Shorts | 3 |
    | Bike Racks | 1 |
    | ... | ... |

8. In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane for <bpt id="p2">**</bpt>SQL Script 1<ept id="p2">**</ept>, change the <bpt id="p3">**</bpt>Name<ept id="p3">**</ept> to <bpt id="p4">**</bpt>Count Products by Category<ept id="p4">**</ept>. Then in the toolbar, select <bpt id="p1">**</bpt>Publish<ept id="p1">**</ept> to save the script.

9. أغلق جزء البرنامج النصي **"Count Products by Category"**.

10. في استوديو Synapse، حدد الصفحة **"Develop"** ولاحظ أنه تم حفظ البرنامج النصي SQL **عدد منتجات المنشورة حسب الفئة** هناك.

11. Select the <bpt id="p1">**</bpt>Count Products by Category<ept id="p1">**</ept> SQL script to reopen it. Then ensure that the script is connected to the <bpt id="p1">**</bpt>Built-in<ept id="p1">**</ept> SQL pool and run it to retrieve the product counts.

12. في جزء **"Results"** حدد طريقة عرض **"Chart"** ثم حدد الإعدادات التالية للتخطيط:
    - **نوع المخطط**: عمود
    - **فئة العمود**: الفئة
    - **أعمدة وسيلة الإيضاح (السلسلة)**: عدد المنتجات
    - **موقف وسيلة الإيضاح**: أسفل - وسط
    - **تسمية وسيلة الإيضاح**: *اتركه فارغاً*
    - **القيمة الصغرى لوسيلة الإيضاح (السلسلة)**: *اتركه فارغاً*
    - **القيمة الكبرى لوسيلة الإيضاح (السلسلة)**: *اتركه فارغاً*
    - **تسمية الفئة**: *اتركه فارغاً*

    يجب أن يشبه المخطط الناتج هذا:

    ![صورة تَعرض طريقة عرض مخطط بياني لعدد المنتجات](images/column-chart.png)

## <a name="use-a-spark-pool-to-analyze-data"></a>استخدام تجمع Spark لتحليل البيانات

While SQL is a common language for querying structured datasets, many data analysts find languages like Python useful to explore and prepare data for analysis. In Azure Synapse Analytics, you can run Python (and other) code in a <bpt id="p1">*</bpt>Spark pool<ept id="p1">*</ept>; which uses a distributed data processing engine based on Apache Spark.

1. في استوديو Synapse، حدد صفحة **"Manage"**.
2. حدد علامة التبويب **"Apache Spark pools"** ثم استخدم رمز **&#65291، جديد** لإنشاء تجمّع Spark جديد بالإعدادات التالية:
    - **اسم وعاء Apache Spark **: spark
    - **حجم عقدة المجموعة**: الذاكرة محسنة
    - **حجم العقدة**: صغير (4 vCores / 32 GB)
    - **تحجيم تلقائي**: ُممكّن
    - **عدد العقد** 3----3
3. مراجعة وإنشاء تجمّع Spark ثم انتظر حتى عملية التوزيع (التي قد تستغرق بضع دقائق).
4. When the Spark pool has been deployed, in Synapse Studio, on the <bpt id="p1">**</bpt>Data<ept id="p1">**</ept> page, browse to the file system for your Synapse workspace. Then right-click <bpt id="p1">**</bpt>products.csv<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New notebook<ept id="p2">**</ept>, and select <bpt id="p3">**</bpt>Load to DataFrame<ept id="p3">**</ept>.
5. في جزء **"Notebook 1"** الذي يفتح، في القائمة **"Attach to"** حدد تجمع **"spark"** المُنشأ مسبقاً وتأكد من تعيين **اللغة** إلى **PySpark (Python)**.
6. راجع التعليمات البرمجية في الخلية الأولى (والوحيدة) في دفتر الملاحظات، والتي يجب أن تبدو كما يلي:

    ```Python
    %%pyspark
    df = spark.read.load('abfss://fsxx@datalakexx.dfs.core.windows.net/products.csv', format='csv'
    ## If header exists uncomment line below
    ##, header=True
    )
    display(df.limit(10))
    ```

7.                  **تلميح**: تأكد من أنك تعمل في الدليل الذي يحتوي على اشتراكك - المُشار إليه في أعلى اليمين أسفل معرّف مستخدمك.

    > **ملاحظة**: في حالة حدوث خطأ بسبب عدم توفر Python Kernel بعد، أعد تشغيل الخلية.

8. في نهاية المطاف، يجب أن تظهر النتائج أسفل الخلية، ويجب أن تكون مشابهة لهذا:

    | _c0_ | _c1_ | _c2_ | _c3_ |
    | -- | -- | -- | -- |
    | ProductID | ProductName | الفئة | ListPrice |
    | 771 | Mountain-100 Silver, 38 | Mountain Bikes | 3399.9900 |
    | 772 | Mountain-100 Silver, 42 | Mountain Bikes | 3399.9900 |
    | ... | ... | ... | ... |

9. إلغاء اتصال خط *header=True* (لأن الملف products.csv يحتوي على رؤوس الأعمدة في السطر الأول)، بحيث تبدو التعليمات البرمجية الخاصة بك كما يلي:

    ```Python
    %%pyspark
    df = spark.read.load('abfss://fsxx@datalakexx.dfs.core.windows.net/products.csv', format='csv'
    ## If header exists uncomment line below
    , header=True
    )
    display(df.limit(10))
    ```

10. أعد تشغيل الخلية وتحقق من أن النتائج تبدو كما يلي:

    | ProductID | ProductName | الفئة | ListPrice |
    | -- | -- | -- | -- |
    | 771 | Mountain-100 Silver, 38 | Mountain Bikes | 3399.9900 |
    | 772 | Mountain-100 Silver, 42 | Mountain Bikes | 3399.9900 |
    | ... | ... | ... | ... |

    لاحظ أن تشغيل الخلية مرة أخرى يستغرق وقتاً أقل، لأن تجمع Spark قد بدأ بالفعل.

11. ضمن النتائج، استخدم رمز **"التعليمة &#65291;"** لإضافة خلية تعليمة برمجية جديدة إلى دفتر الملاحظات.
12. في خلية التعليمات البرمجية الفارغة الجديدة، أضف التعليمات البرمجية التالية:

    ```Python
    df_counts = df.groupBy(df.Category).count()
    display(df_counts)
    ```

13. حدد " **&#9655; Run**" الموجود على اليسار لتشغيل خلية التعليمات البرمجية الجديدة، وراجع النتائج التي يجب أن تبدو مشابهة لهذا:

    | الفئة | العدد |
    | -- | -- |
    | سماعة الرأس | 3 |
    | عجلات | 14 |
    | ... | ... |

14. إذا لم تكن كذلك، حدد رمز المستخدم وبدّل الدليل.

    ![صورة تعرض عرض المخطط البياني لعدد الفئات](images/bar-chart.png)

15. أغلق جزء **Notebook 1** وتجاهل التغييرات.

## <a name="delete-azure-resources"></a>حذف موارد Azure

إذا انتهيت من استكشاف Azure Synapse Analytics، يجب حذف الموارد التي أنشأتها لتجنب تكاليف Azure غير الضرورية.

1. أغلق علامة التبويب مستعرض Studio browser ثم العودة إلى مدخل Microsoft Azure.
2. في مدخل Microsoft Azure، في الصفحة ⁧**الرئيسية**⁩، حدّد ⁧ **"Resource groups"⁦⁩⁧**⁩.
3. حدد مجموعة الموارد لمساحة عمل Synapse Analytics (وليس مجموعة الموارد المدارة)، وتحقق من أنها تحتوي على مساحة عمل Synapse وحساب التخزين وتجمّع Spark لمساحة العمل.
4. في أعلى صفحة **"Overview"** لمجموعة الموارد، حدد **"Delete resource group"**.
5. أدخل اسم مجموعة الموارد لتأكيد رغبتك في حذفه، ثم حدد **"Delete"**.

    بعد بضع دقائق، سيتم حذف مساحة عمل Azure Synapse ومساحة العمل المُدارة المقترنة بها.
