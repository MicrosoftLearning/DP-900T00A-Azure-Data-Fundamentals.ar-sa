---
lab:
  title: استكشاف Azure Synapse Data Explorer
  module: Explore fundamentals of real-time analytics
---

# <a name="explore-azure-synapse-data-explorer"></a>استكشاف Azure Synapse Data Explorer

في هذا التمرين، ستستخدم Azure Synapse Data Explorer لتحليل بيانات التسلسل الزمني.

سيستغرق إكمال هذا التمرين المعملي **25** دقيقة.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="provision-a-synapse-analytics-workspace"></a>توفير مساحة عمل Synapse Analytics

> **تلميح**: إذا كنت تمتلك Azure Synapse Workspace من التمرين السابق، فتخطَّ هذا القسم وانتقل مباشرة إلى قسم **[إنشاء تجمّع Data Explorer](#create-a-data-explorer-pool)** .

1. افتح مدخل Microsoft Azure على [https://portal.azure/com](https://portal.azure.com?azure-portal=true)، وقم بتسجيل الدخول باستخدام حساب Microsoft المقترن باشتراك Azure.

    > <bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: Ensure you are working in the directory containing your subscription - indicated at the top right under your user ID. If not, select the user icon and switch directory.

1. في مدخل Microsoft Azure، في صفحة **"Home"**، استخدم **&#65291; إنشاء رمز مورد** لإنشاء مورد جديد.
1. ابحث عن *Azure Synapse Analytics*، وإنشاء مورد **Azure Synapse Analytics** جديد باستخدام الإعدادات التالية:
    - **الاشتراك**: *اشتراكك في Azure*
        - **Resource group**: *إنشاء مجموعة موارد جديدة ذات اسم فريد مثل "synapse-rg"*
        - **مجموعة الموارد المُدارة**: *أدخل اسماً مناسباً، على سبيل المثال "synapse-managed-rg"*.
    - **اسم مساحة العمل**: *أدخل اسم مساحة عمل فريدة، على سبيل المثال "synapse-ws-<your_name>*.
    - **المنطقة**: *اختر أي منطقة متوفرة*.
    - **حدد "Data Lake Storage Gen 2"**: من الاشتراك
        - **اسم الحساب**: *إنشاء حساب جديد باسم فريد، على سبيل المثال "<your_name> datalake"*.
        - **اسم نظام الملفات**: *إنشاء نظام ملفات جديد باسم فريد، على سبيل المثال "fs<your_name>"*.

    > <bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: A Synapse Analytics workspace requires two resource groups in your Azure subscription; one for resources you explicitly create, and another for managed resources used by the service. It also requires a Data Lake storage account in which to store data, scripts, and other artifacts.

1. عند إدخال هذه التفاصيل، حدد **"Review + create"**، ثم حدد **"Create"** لإنشاء مساحة العمل.
1. انتظر حتى يتم إنشاء مساحة العمل - قد يستغرق ذلك خمس دقائق أو نحو ذلك.
1. عند اكتمال التوزيع انتقل إلى مجموعة الموارد التي تم إنشاؤها ولاحظ أنه يحتوي على مساحة عمل Synapse Analytics وحساب تخزين مستودع البيانات.
1. حدد مساحة عمل Synapse، وفي صفحة **"Overview"** الخاصة بها، في بطاقة **"Open Synapse Studio"**، حدد **"Open"** لفتح Synapse Studio في علامة تبويب متصفح جديدة. Synapse Studio هي واجهة قائمة على الويب يمكنك استخدامها للعمل مع مساحة عمل Synapse Analytics.
1. على الجانب الأيسر من Synapse Studio، استخدم الرمز **&rsaquo;&rsaquo;** لتوسيع القائمة - ما يكشف عن الصفحات المختلفة داخل Synapse Studio التي ستستخدمها لإدارة الموارد وتنفيذ مهام تحليل البيانات

## <a name="create-a-data-explorer-pool"></a>إنشاء تجمع Data Explorer

1. في استوديو Synapse، حدد صفحة **"Manage"**.
1. حدد علامة التبويب "**Data Explorer pools**"، ثم استخدم رمز " **&#65291; New**" لإنشاء تجمّع جديد بالإعدادات التالية:
    - **اسم تجمع Data Explorer**: dxpool
    - **حمل العمل**: الحوسبة المحسّنة
    - **الحجم**: صغير جدا (2 ذاكرة أساسية)
1. حدد "**Next: Additional Settings >** " ومكّن الإعداد "**Streaming ingestion**" - ما يمكّن Data Explorer من استيعاب بيانات جديدة من مصدر دفق مثل مراكز الأحداث.
1. حدد **Review and create** لإنشاء تجمّع Data Explorer، ثم انتظر حتى يتم توزيعه (والذي قد يستغرق 15 دقيقة أو أكثر - ستتغير الحالة من *Creating* إلى *Online*).

## <a name="create-a-database-and-ingest-data"></a>إنشاء قاعدة بيانات واستيعاب البيانات

1. في Synapse Studio، حدد الصفحة **Data**.
1. تأكد من تحديد علامة التبويب "**Workspace**"، وإذا لزم الأمر، فحدد الرمز " **&#8635;** " في أعلى الجزء الأيسر من الصفحة لتحديث طريقة العرض بحيث تُدرج "**Data Explorer databases**".
1. قم بتوسيع **قواعد بيانات Data Explorer** وتحقق من إدراج **dxpool**.
1. في الجزء "**Data**"، استخدم الرمز " **&#65291;** " لإنشاء "**Data Explorer database**" جديدة في التجمّع "**dxpool**" باسم **iot-data**.
1. أثناء انتظار إنشاء قاعدة البيانات، نزّل **devices.csv** من [https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/streaming/data/devices.csv](https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/streaming/data/devices.csv?azure-portal=true)، واحفظه في أي مجلد على جهاز الكمبيوتر المحلي.
1. في Synapse Studio، انتظر حتى يتم إنشاء قاعدة البيانات إذا لزم الأمر، ثم في القائمة **...** لقاعدة البيانات **iot-data** الجديدة، حدد **Open in Azure Data Explorer**.
1. في علامة تبويب المتصفح الجديد الذي يحتوي على Azure Data Explorer، في علامة التبويب **Data**، حدد **Ingest new data**.
1. في الصفحة **Destination**، حدد الإعدادات التالية:
    - **نظام المجموعة**: *تجمّع Data Explorer **dxpool** في مساحة عمل Azure Synapse*
    - **قاعدة البيانات**: iot-data
    - **الجدول**: أنشئ جدولاً جديداً يسمى **devices**
1. حدد **Next: Source** وفي الصفحة **Source** حدد الخيارات التالية:
    - **Source type**: File
    - **Files**: قم بتحميل الملف **devices.csv** من جهاز الكمبيوتر المحلي.
1. حدد **Next: Schema** وفي الصفحة **Schema**، تأكد من صحة الإعدادات التالية:
    - **Compression type**: Uncompressed
    - **Data format**: CSV
    - **Ignore the first record**:  تحديد
    - **Mapping**: devices_mapping
1. Ensure the column data types have been correctly identified as <bpt id="p1">*</bpt>Time (datetime)<ept id="p1">*</ept>, <bpt id="p2">*</bpt>Device (string)<ept id="p2">*</ept>, and <bpt id="p3">*</bpt>Value (long)<ept id="p3">*</ept>). Then select <bpt id="p1">**</bpt>Next: Start Ingestion<ept id="p1">**</ept>.
1. عند اكتمال الاستيعاب، حدد **Close**.
1. في Azure Data Explorer، ضمن علامة التبويب **Query**، تأكد من تحديد قاعدة بيانات **iot-data**، ثم أدخل الاستعلام التالي في جزء الاستعلام.

    ```kusto
    devices
    ```

1. في شريط الأدوات، حدد " **&#9655; Run**" لتشغيل الاستعلام وراجع النتائج، والتي يجب أن تبدو مشابهة لهذا:

    | الوقت | جهاز | القيمة |
    | --- | --- | --- |
    | 2022-01-01T00:00:00Z | Dev1 | 7 |
    | 2022-01-01T00:00:01Z | Dev2 | 4 |
    | ... | ... | ... |

    في حالة تطابق النتائج مع هذا، تكون قد نجحت في إنشاء جدول **devices** من البيانات الموجودة في الملف.

    > <bpt id="p1">**</bpt>Tip<ept id="p1">**</ept>: In this example, you imported a very small amount of batch data from a file, which is fine for the purposes of this exercise. In reality, you can use Data Explorer to analyze much larger volumes of data; and since you enabled stream ingestion, you could also have configured Data Explorer to ingest data into the table from a streaming source such as Azure Event Hubs.

## <a name="use-kusto-query-language-to-query-the-table-in-synapse-studio"></a>استخدام لغة الاستعلام Kusto للاستعلام عن الجدول في Synapse Studio

1. أغلق علامة تبويب مستعرض Azure Data Explorer وارجع إلى علامة التبويب التي تحتوي على Synapse Studio.
1. On the <bpt id="p1">**</bpt>Data<ept id="p1">**</ept> page, expand the <bpt id="p2">**</bpt>iot-data<ept id="p2">**</ept> database and its <bpt id="p3">**</bpt>Tables<ept id="p3">**</ept> folder. Then in the <bpt id="p1">**</bpt>...<ept id="p1">**</ept> menu for the <bpt id="p2">**</bpt>devices<ept id="p2">**</ept> table, select <bpt id="p3">**</bpt>New KQL Script<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>Take 1000 rows<ept id="p4">**</ept>.
1. Review the generated query and its results. The query should contain the following code:

    ```kusto
    devices
    | take 1000
    ```

    تحتوي نتائج الاستعلام على أول 1000 صف من البيانات.

1. تغيير الاستعلام كما يلي:

    ```kusto
    devices
    | where Device == 'Dev1'
    ```

1. Select <bpt id="p1">**</bpt>&amp;#9655; Run<ept id="p1">**</ept> to run the query. Then review the results, which should contain only the rows for the <bpt id="p1">*</bpt>Dev1<ept id="p1">*</ept> device.

1. تغيير الاستعلام كما يلي:

    ```kusto
    devices
    | where Device == 'Dev1'
    | where Time > datetime(2022-01-07)
    ```

1. شغّل الاستعلام وراجع النتائج، التي يجب أن تحتوي فقط على صفوف الجهاز *Dev1* بعد السابع من يناير 2022.

1. تغيير الاستعلام كما يلي:

    ```kusto
    devices
    | where Time between (datetime(2022-01-01 00:00:00) .. datetime(2022-07-01 23:59:59))
    | summarize AvgVal = avg(Value) by Device
    | sort by Device asc
    ```

1. شغّل الاستعلام وراجع النتائج، التي يجب أن تحتوي على متوسط قيمة الجهاز المسجلة بين 1 يناير و7 يناير 2022 بترتيب تصاعدي لاسم الجهاز.

1. أغلق علامة التبويب استعلام KQL، مع تجاهل التغييرات.

## <a name="delete-azure-resources"></a>حذف موارد Azure

الآن بعد الانتهاء من استكشاف Azure Synapse Analytics، يجب حذف الموارد التي أنشأتها لتجنب تكاليف Azure غير الضرورية.

1. أغلق علامة تبويب مستعرض Synapse Studio دون حفظ أية تغييرات، ثم عد إلى مدخل Azure.
1. في مدخل Microsoft Azure، في الصفحة ⁧**الرئيسية**⁩، حدّد ⁧ **"Resource groups"⁦⁩⁧**⁩.
1. حدد مجموعة الموارد لمساحة عمل Synapse Analytics (وليس مجموعة الموارد المُدارة)، وتحقق من أنها تحتوي على مساحة عمل Synapse وحساب التخزين وتجمّع Data Explorer لمساحة العمل الخاصة بك (إذا أكملت التمرين السابق، فستحتوي أيضاً على تجمّع Spark).
1. في أعلى صفحة **"Overview"** لمجموعة الموارد، حدد **"Delete resource group"**.
1. أدخل اسم مجموعة الموارد لتأكيد رغبتك في حذفه، ثم حدد **"Delete"**.

    بعد بضع دقائق، سيتم حذف مساحة عمل Azure Synapse ومساحة العمل المُدارة المقترنة بها.
