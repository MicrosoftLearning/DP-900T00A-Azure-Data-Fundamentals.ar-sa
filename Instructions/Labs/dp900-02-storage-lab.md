---
lab:
  title: استكشاف تخزين Azure
  module: Explore Azure Storage for non-relational data
---

# <a name="explore-azure-storage"></a>استكشاف تخزين Azure

في هذا التمرين، ستقوم بتوفير حساب Azure Storage في اشتراكك في Azure، واستكشاف الطرق المختلفة التي يمكنك استخدامها لتخزين البيانات.

سيستغرق إكمال هذا التمرين المعملي **15** دقيقة.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="provision-an-azure-storage-account"></a>توفير حساب Azure Storage

تتمثل الخطوة الأولى في استخدام Azure Storage في توفير حساب Azure Storage في اشتراكك في Azure.

1. إذا لم تكن فعلت ذلك، فسجّل الدخول إلى [مدخل Microsoft Azure](https://portal.azure.com?azure-portal=true).
1. On the Azure portal home page, select <bpt id="p1">**</bpt>&amp;#65291; Create a resource<ept id="p1">**</ept> from the upper left-hand corner and search for <bpt id="p2">*</bpt>Storage account<ept id="p2">*</ept>. Then in the resulting <bpt id="p1">**</bpt>Storage account<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Create<ept id="p2">**</ept>.
1. أدخل القيم التالية في الصفحة **إنشاء حساب تخزين**:
    - <bpt id="p1">**</bpt>Subscription<ept id="p1">**</ept>: If you're using a sandbox, select <bpt id="p2">*</bpt>Concierge Subscription<ept id="p2">*</ept>. Otherwise, select your Azure subscription.
    - **Resource group**: إذا كنت تستخدم بيئة الاختبار المعزولة، فحدد مجموعة الموارد الموجودة (والتي سيكون لها اسم مثل *learn-xxxx...* ). وإلا، أنشئ مجموعة موارد جديدة وامنحها الاسم الذي تختاره.
    - **اسم حساب التخزين**: أدخل اسماً فريداً لحساب التخزين باستخدام الأحرف الصغيرة والأرقام.
    - **Region**: حدد أي موقع متاح.
    - **الأداء**: *قياسي*
    - **التكرار**: *التخزين المتكرر محلياً (LRS)*

1. Select <bpt id="p1">**</bpt>Next: Advanced &gt;<ept id="p1">**</ept> and view the advanced configuration options. In particular, note that this is where you can enable hierarchical namespace to support Azure Data Lake Storage Gen2. Leave this option <bpt id="p1">**</bpt><bpt id="p2">&lt;u&gt;</bpt>unselected<ept id="p2">&lt;/u&gt;</ept><ept id="p1">**</ept> (you'll enable it later), and then select <bpt id="p3">**</bpt>Next: Networking &gt;<ept id="p3">**</ept> to view the networking options for your storage account.
1. Select <bpt id="p1">**</bpt>Next: Data protection &gt;<ept id="p1">**</ept> and then in the <bpt id="p2">**</bpt>Recovery<ept id="p2">**</ept> section, <bpt id="p3">&lt;u&gt;</bpt>de<ept id="p3">&lt;/u&gt;</ept>select all of the <bpt id="p4">**</bpt>Enable soft delete...<ept id="p4">**</ept> options. These options retain deleted files for subsequent recovery, but can cause issues later when you enable hierarchical namespace.
1. تابع عبر صفحات  **Next >** المتبقية دون تغيير أي من الإعدادات الافتراضية، ثم في صفحة "**Review + Create**"، انتظر حتى يُتحقق من صحة ما حددت، وحدد "**Create**" لإنشاء حساب Azure Storage.
1. Wait for deployment to complete. Then go to the resource that was deployed.

## <a name="explore-blob-storage"></a>استكشاف تخزين كائن ثنائي كبير الحجم

الآن بعد أن أصبح لديك حساب Azure Storage، يمكنك إنشاء حاوية لبيانات الكائن الثنائي كبير الحجم.

1. قم بتنزيل ملف JSON [product1.json](https://aka.ms/product1.json?azure-portal=true) من `https://aka.ms/product1.json` واحفظه على جهاز الكمبيوتر (يمكنك حفظه في أي مجلد - ستقوم بتحميله إلى تخزين كائن ثنائي كبير الحجم لاحقاً).

    *إذا تم عرض ملف JSON في المتصفح، فاحفظ الصفحة كـ **product1.json**.*

1. في صفحة مدخل Microsoft Azure لحاوية التخزين، على الجانب الأيسر، في القسم **Data storage**، حدد **Containers**.
1. في صفحة "**Containers**"، حدد " **&#65291; Container**" وأضف حاوية جديدة باسم **data** ذات مستوى وصول عام "**Private (no anonymous access)** ".
1. عند إنشاء الحاوية **data**، تحقق من إدراجها في الصفحة **Containers**.
1. In the pane on the left side, in the top section, select **Storage browser **. This page provides a browser-based interface that you can use to work with the data in your storage account.
1. في صفحة متصفح موقع التخزين، حدد **Blob containers** وتحقق من إدراج الحاوية **data**.
1. حدد حاوية **data**، ولاحظ أنها فارغة.
1. حدد " **&#65291; Add Directory**" واقرأ المعلومات عن المجلدات قبل إنشاء دليل جديد باسم **products**.
1. في "مستكشف التخزين"، تحقق من أن طريقة العرض الحالية تعرض محتويات المجلد "**products**" الذي أنشأته للتو - لاحظ أن "breadcrumbs" أعلى الصفحة تعكس المسار **Blob containers > data > products**.
1. في مسارات التنقل، حدد **data** للتبديل إلى الحاوية **data**، ولاحظ أنها <u>لا</u> تحتوي على مجلد باسم **products**.

    Folders in blob storage are virtual, and only exist as part of the path of a blob. Since the <bpt id="p1">**</bpt>products<ept id="p1">**</ept> folder contained no blobs, it isn't really there!

1. استخدم الزر " **&#10514; Upload**" لفتح اللوحة "**Upload blob**".
1. In the <bpt id="p1">**</bpt>Upload blob<ept id="p1">**</ept> panel, select the <bpt id="p2">**</bpt>product1.json<ept id="p2">**</ept> file you saved on your local computer previously. Then in the <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept> section, in the <bpt id="p2">**</bpt>Upload to folder<ept id="p2">**</ept> box, enter <bpt id="p3">**</bpt>product_data<ept id="p3">**</ept> and select the <bpt id="p4">**</bpt>Upload<ept id="p4">**</ept> button.
1. أغلق اللوحة **Upload blob** إذا كانت لا تزال مفتوحة، وتحقق من إنشاء المجلد الظاهري **product_data** في الحاوية **data**.
1. حدد المجلد **product_data** وتحقق من أنه يحتوي على الكائن الثنائي كبير الحجم **product1.json** الذي قمت بتحميله.
1. على الجانب الأيسر، في القسم **Data storage**، حدد **Containers**.
1. افتح الحاوية **data**، وتحقق من إدراج المجلد **product_data** الذي أنشأته.
1. Select the <bpt id="p1">**</bpt>&amp;#x2027;&amp;#x2027;&amp;#x2027;<ept id="p1">**</ept> icon at the right-end of the folder, and note that it doesn't display any options. Folders in a flat namespace blob container are virtual, and can't be managed.
1. استخدم الأيقونة **X** أعلى يمين الصفحة **data** لإغلاق الصفحة والعودة إلى الصفحة **Containers**.

## <a name="explore-azure-data-lake-storage-gen2"></a>Explore Azure Data Lake Storage Gen2

Azure Data Lake Store Gen2 support enables you to use hierarchical folders to organize and manage access to blobs. It also enables you to use Azure blob storage to host distributed file systems for common big data analytics platforms.

1. قم بتنزيل ملف JSON [product2.json](https://aka.ms/product2.json?azure-portal=true) من `https://aka.ms/product2.json` واحفظه على جهاز الكمبيوتر في نفس المجلد حيث قمت بتنزيل **product1.json** مسبقاً - ستقوم بتحميله إلى تخزين كائن ثنائي كبير الحجم لاحقاً).
1. في صفحة مدخل Microsoft Azure لحساب التخزين، على الجانب الأيسر، مرر لأسفل إلى القسم "**Settings**"، وحدد "**Data Lake Gen2 upgrade**".
1. في الصفحة الرئيسية لمدخل Microsoft Azure، حدد " **&#65291; Create a resource**" من الزاوية العلوية اليسرى وابحث عن "*Storage account*".
1. عند اكتمال الترقية، في الجزء الموجود على الجانب الأيسر، في القسم العلوي، حدد "**Storage browser**" وانتقل مرة أخرى إلى جذر حاوية الكائن الثنائي كبير الحجم **data**، التي لا تزال تحتوي على المجلد "**product_data**".
1. حدد المجلد **product_data**، وتحقق من أنه لا يزال يحتوي على ملف **product1.json** الذي قمت بتحميله مسبقاً.
1. استخدم الزر " **&#10514; Upload**" لفتح اللوحة "**Upload blob**".
1. ثم في صفحة **حساب التخزين** الناتجة، حدد **"Create"**.
1. أغلق اللوحة **Upload blob** إذا كانت لا تزال مفتوحة، وتحقق من أن المجلد **product_data** يحتوي الآن على الملف **product2.json.**
1. على الجانب الأيسر، في القسم **Data storage**، حدد **Containers**.
1. افتح الحاوية **data**، وتحقق من إدراج المجلد **product_data** الذي أنشأته.
1. حدد الرمز " **&#x2027;&#x2027;&#x2027;** " في أقصى يمين المجلد، ولاحظ أنه يمكنك تنفيذ مهام التكوين على مستوى المجلد مع تمكين مساحة أسماء الهرمية، بما في ذلك إعادة تسمية المجلدات وأذونات الإعداد.
1. استخدم الأيقونة **X** أعلى يمين الصفحة **data** لإغلاق الصفحة والعودة إلى الصفحة **Containers**.

## <a name="explore-azure-files"></a>استكشاف Azure Files

يوفر Azure Files طريقة لإنشاء مشاركات الملفات المستندة إلى السحابة.

1. في صفحة مدخل Microsoft Azure لحاوية التخزين الخاصة بك، على الجانب الأيسر، في قسم **Data storage**، حدد **File shares**.
1. في صفحة "File shares"، حدد " **&#65291; File share**" وأضف مشاركة ملف جديدة باسم **files** باستخدام الطبقة "**Transaction optimized**".
1. في **File shares**، افتح مشاركة **الملفات** الجديدة.
1. At the top of the page, select <bpt id="p1">**</bpt>Connect<ept id="p1">**</ept>. Then in the <bpt id="p1">**</bpt>Connect<ept id="p1">**</ept> pane, note that there are tabs for common operating systems (Windows, Linux, and macOS) that contain scripts you can run to connect to the shared folder from a client computer.
1. أغلق الجزء **Connect** ثم أغلق الصفحة **files** للعودة إلى الصفحة **File shares** على حساب Azure storage.

## <a name="explore-azure-tables"></a>استكشاف Azure Tables

توفر Azure Tables مخزن المفاتيح/القيم للتطبيقات التي تحتاج إلى تخزين قيم البيانات، ولكنها لا تحتاج إلى الوظائف الكاملة وبنية قاعدة البيانات الارتباطية.

1. في صفحة مدخل Microsoft Azure لحاوية التخزين الخاصة بك، على الجانب الأيسر، في القسم **Data storage**، حدد **Tables**.
1. في صفحة "**Tables**"، حدد " **&#65291; Table**" وأنشئ جدولاً جديداً باسم **products**.
1. بعد إنشاء الجدول **products**، في الجزء على الجانب الأيسر، في القسم العلوي، حدد "**Storage browser**".
1. في مستكشف التخزين، حدد **Tables** وتحقق من إدراج الجدول **products**.
1. حدد الجدول **products**.
1. في صفحة "**product**"، حدد " **&#65291; Add entity**".
1. في اللوحة **Add entity**، أدخل القيم الرئيسية التالية:
    - **PartitionKey**: 1
    - **RowKey**: 1
1. حدد **Add property**، وقم بإنشاء خاصية جديدة بالقيم التالية:

    |اسم الخاصية | النوع | القيمة |
    | ------------ | ---- | ----- |
    | الاسم | سلسلة | عنصر واجهة المستخدم |

1. أضف خاصية ثانية بالقيم التالية:

    |اسم الخاصية | النوع | القيمة |
    | ------------ | ---- | ----- |
    | Price | مزدوج | 2.99 |

1. حدد **Insert** لإدراج صف للكيان الجديد في الجدول.
1. في متصفح التخزين، تحقق من إضافة صف إلى الجدول **products**، ومن إنشاء عمود **طابع زمني** للإشارة إلى آخر تعديل للصف.
1. أضف كياناً آخر إلى الجدول **products** بالخصائص التالية:

    |اسم الخاصية | النوع | القيمة |
    | ------------ | ---- | ----- |
    | PartitionKey | سلسلة | 1 |
    | RowKey | سلسلة | 2 |
    | الاسم | سلسلة | Kniknak |
    | Price | مزدوج | 1.99 |
    | إيقاف | منطقي | صواب |

1. بعد إدراج الكيان الجديد، تحقق من عرض صف يحتوي على المنتج الذي تم إيقافه في الجدول.

    You have manually entered data into the table using the storage browser interface. In a real scenario, application developers can use the Azure Storage Table API to build applications that read and write values to tables, making it a cost effective and scalable solution for NoSQL storage.

> **تلميح**: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Storage.
