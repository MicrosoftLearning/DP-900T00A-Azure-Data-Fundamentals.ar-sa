---
lab:
  title: استكشاف البيانات غير الارتباطية في Azure باستخدام Azure Cosmos DB
  module: Explore fundamentals of Azure Cosmos DB
---
# <a name="explore-non-relational-data-in-azure-with-azure-cosmos-db"></a>استكشاف البيانات غير الارتباطية في Azure باستخدام Azure Cosmos DB

في هذا التمرين، ستقوم بتوفير قاعدة بيانات Azure Cosmos DB في اشتراكك في Azure، واستكشاف الطرق المختلفة التي يمكنك استخدامها لتخزين البيانات غير العلائقية.

سيستغرق إكمال هذا التمرين المعملي **15** دقيقة.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="create-a-cosmos-db-account"></a>قم بإنشاء حساب Cosmos DB

To use Cosmos DB, you must provision a Cosmos DB account in your Azure subscription. In this exercise, you'll provision a Cosmos DB account that uses the core (SQL) API.

1. In the Azure portal, select <bpt id="p1">**</bpt>+ Create a resource<ept id="p1">**</ept> at the top left, and search for <bpt id="p2">*</bpt>Azure Cosmos DB<ept id="p2">*</ept>.  In the results, select <bpt id="p1">**</bpt>Azure Cosmos DB<ept id="p1">**</ept> and select  <bpt id="p2">**</bpt>Create<ept id="p2">**</ept>.
1. في تجانب **Core (SQL) - Recommended** حدد **Create**.
1. أدخل التفاصيل التالية، ثم حدد **Review + Create**: 
    - <bpt id="p1">**</bpt>Subscription<ept id="p1">**</ept>: If you're using a sandbox, select <bpt id="p2">*</bpt>Concierge Subscription<ept id="p2">*</ept>. Otherwise, select your Azure subscription.
    - **Resource group**: إذا كنت تستخدم بيئة الاختبار المعزولة، فحدد مجموعة الموارد الموجودة (والتي سيكون لها اسم مثل *learn-xxxx...* ). وإلا، أنشئ مجموعة موارد جديدة باسم من اختيارك.
    - **Account Name**: أدخل اسمًا فريدًا
    - **Location**: اختر أي موقع موصى به
    - **Capacity mode**: معدل النقل المقدم
    - **Apply Free-Tier Discount**: حدد تطبيق إذا كان ذلك متوفرًا
    - **Limit total account throughput**: غير محدد
1. عند التحقق من صحة التكوين، حدد **Create**.
1. Wait for deployment to complete. Then go to the deployed resource.

## <a name="create-a-sample-database"></a>إنشاء نموذج قاعدة البيانات

*خلال هذا الإجراء، أغلق أي تلميحات يتم عرضها في المدخل*.

1. في الصفحة الخاصة بحساب Cosmos DB الجديد، في الجزء n الأيسر، حدد **Data Explorer**.
1. في صفحة **Data Explorer**، حدد **Launch quick start**.
1. في علامة التبويب **New container**، راجع الإعدادات التي تم ملؤها مسبقا لقاعدة بيانات العينة، ثم حدد **OK**.
1. راقب الحالة في اللوحة الموجودة أسفل الشاشة حتى يتم إنشاء قاعدة بيانات **SampleDB** وحاوية **SampleContainer** (والتي قد تستغرق دقيقة أو نحو ذلك).

## <a name="view-and-create-items"></a>عرض العناصر وإنشائها

1. In the Data Explorer page, expand the <bpt id="p1">**</bpt>SampleDB<ept id="p1">**</ept> database and the <bpt id="p2">**</bpt>SampleContainer<ept id="p2">**</ept> container, and select <bpt id="p3">**</bpt>Items<ept id="p3">**</ept> to see a list of items in the container. The items represent addresses, each with a unique id and other properties.
1. حدد أيًا من العناصر الموجودة في القائمة للاطلاع على تمثيل JSON لبيانات العنصر.
1. في أعلى الصفحة، حدد **New Item** لإنشاء عنصر فارغ جديد.
1. قم بتعديل JSON للعنصر الجديد كما يلي، ثم حدد **Save**.

    ```json
    {
        "address": "1 Any St.",
        "id": "123456789"
    }
    ```

1. بعد حفظ العنصر الجديد، لاحظ إضافة خصائص بيانات تعريف إضافية تلقائيًا.

## <a name="query-the-database"></a>الاستعلام عن قاعدة البيانات

1. في الصفحة **Data Explorer**، حدد أيقونة **New SQL Query**.
1. في محرر الاستعلام SQL، راجع الاستعلام الافتراضي (`SELECT * FROM c`) واستخدم الزر `SELECT * FROM c` لتشغيله.
1. راجع النتائج، والتي تتضمن تمثيل JSON الكامل لجميع العناصر.
1. تغيير الاستعلام كما يلي:

    ```sql
    SELECT c.id, c.address
    FROM c
    WHERE CONTAINS(c.address, "Any St.")
    ```

1. استخدم الزر **Execute Query** لتشغيل الاستعلام الذي تمت مراجعته ومراجعة النتائج، والذي يتضمن كيانات JSON لأي عناصر مع حقل **address** يحتوي على النص "أي شارع".
1. أغلق محرر استعلام SQL، مع تجاهل التغييرات.

    You've seen how to create and query JSON entities in a Cosmos DB database by using the data explorer interface in the Azure portal. In a real scenario, an application developer would use one of the many programming language specific software development kits (SDKs) to call the core (SQL) API and work with data in the database.

> **تلميح**: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Cosmos DB.
