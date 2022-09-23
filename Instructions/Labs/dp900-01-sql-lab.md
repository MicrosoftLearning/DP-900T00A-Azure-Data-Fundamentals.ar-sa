---
lab:
  title: استكشاف Azure SQL Database
  module: Explore relational data in Azure
---

# <a name="explore-azure-sql-database"></a>استكشاف Azure SQL Database

في هذا التمرين، ستقوم بتوفير مورد قاعدة بيانات Azure SQL في اشتراكك في Azure، ثم استخدام SQL للاستعلام عن الجداول في قاعدة بيانات علائقية.

سيستغرق إكمال هذا التمرين المعملي **15** دقيقة.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="provision-an-azure-sql-database-resource"></a>توفير مورد Azure SQL Database

1. In the <bpt id="p1">[</bpt>Azure portal<ept id="p1">](https://portal.azure.com?azure-portal=true)</ept>, select <bpt id="p2">**</bpt>&amp;#65291; Create a resource<ept id="p2">**</ept> from the upper left-hand corner and search for <bpt id="p3">*</bpt>Azure SQL<ept id="p3">*</ept>. Then in the resulting <bpt id="p1">**</bpt>Azure SQL<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Create<ept id="p2">**</ept>.

1. راجع خيارات Azure SQL المتوفرة، ثم في إطار «**SQL databases**»، تأكد من تحديد «**Single database**»، وحدد «**Create**».

    ![لقطة شاشة من مدخل Microsoft Azure تعرض صفحة "Azure SQL".](images//azure-sql-portal.png)

1. أدخل القيم التالية في صفحة **Create SQL Database**:
    - **الاشتراك**: حدد اشتراك Azure الخاص بك.
    - **Resource group**: أنشئ مجموعة موارد جديدة وامنحها اسماً تختاره.
    - **اسم قاعدة البيانات**: *AdventureWorks*
    - <bpt id="p1">**</bpt>Server<ept id="p1">**</ept>:  Select <bpt id="p2">**</bpt>Create new<ept id="p2">**</ept> and create a new server with a unique name in any available location. Use <bpt id="p1">**</bpt>SQL authentication<ept id="p1">**</ept> and specify your name as the server admin login and a suitably complex password (remember the password - you'll need it later!)
    - **هل تريد استخدام تجمع مرن من SQL؟**: *No*
    - **Compute + storage**: اتركه دون تغيير
    - **تكرار تخزين النسخ الاحتياطي**: *Locally-redundant backup storage*

1. On the <bpt id="p1">**</bpt>Create SQL Database<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Next :Networking &gt;<ept id="p2">**</ept>, and on the <bpt id="p3">**</bpt>Networking<ept id="p3">**</ept> page, in the <bpt id="p4">**</bpt>Network connectivity<ept id="p4">**</ept> section, select <bpt id="p5">**</bpt>Public endpoint<ept id="p5">**</ept>. Then select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> for both options in the <bpt id="p2">**</bpt>Firewall rules<ept id="p2">**</ept> section to allow access to your database server from Azure services and your current client IP address.

1. حدد "**Next: Security >** " وعيّن الخيار "**Enable Microsoft Defender for SQL**" إلى "**Not now**".

1. حدد "**Next: Additional Settings >** "، وفي علامة التبويب "**Additional settings**" عيّن الخيار "**Use existing data**" إلى "**Sample**" (سيؤدي ذلك إلى إنشاء عينة قاعدة بيانات يمكنك استكشافها لاحقًا).

1. حدد "**Review + Create**"، ثم حدد "**Create**" لإنشاء قاعدة بيانات Azure SQL.

1. Wait for deployment to complete. Then go to the resource that was deployed, which should look like this:

    ![لقطة شاشة لمدخل Microsoft Azure تعرض صفحة "SQL Database".](images//sql-database-portal.png)

1. في الجزء على الجانب الأيسر من الصفحة، حدد «**Query editor (preview)**» ثم سجل الدخول باستخدام تسجيل دخول المسؤول وكلمة المرور اللذان حددتهما للخادم.
    
    *إذا ظهرت رسالة خطأ تفيد بأنه غير مسموح بعنوان IP للعميل، حدد الارتباط «**Allowlist IP ...**» في نهاية الرسالة للسماح بالوصول ومحاولة تسجيل الدخول مرة أخرى (أضفت سابقًا عنوان IP لعميل الكمبيوتر إلى قواعد جدار الحماية، ولكن قد يتصل محرر الاستعلام من عنوان مختلف اعتمادًا على تكوين الشبكة.)*
    
    يبدو محرر الاستعلام كما يلي:
    
    ![لقطة شاشة لمدخل Microsoft Azure تعرض محرر الاستعلام.](images//query-editor.png)

1. وسّع مجلد **Tables** لمشاهدة الجداول في قاعدة البيانات.

1. في جزء **Query 1**، أدخل عبارة SQL التالية:

    ```sql
    SELECT * FROM SalesLT.Product;
    ```

1. حدد " **&#9655; Run**" فوق الاستعلام لتشغيله وعرض النتائج، والتي يجب أن تشمل جميع الأعمدة لجميع الصفوف في الجدول "**SalesLT.Product**" كما هو موضح هنا:

    ![لقطة شاشة لمدخل Microsoft Azure تعرض محرر الاستعلام مع نتائج الاستعلام.](images//sql-query-results.png)

1. استبدل عبارة SELECT بالتعليمات البرمجية التالية، ثم حدد " **&#9655; Run**" لتشغيل الاستعلام الجديد ومراجعة النتائج (التي لا تتضمن إلا أعمدة "**ProductID**"، و"**Name**"، و"**ListPrice**"، و"**ProductCategoryID**"):

    ```sql
    SELECT ProductID, Name, ListPrice, ProductCategoryID
    FROM SalesLT.Product;
    ```

1. الآن حاول الاستعلام التالي الذي يستخدم JOIN للحصول على اسم الفئة من جدول **SalesLT.ProductCategory**:

    ```sql
    SELECT p.ProductID, p.Name AS ProductName,
            c.Name AS Category, p.ListPrice
    FROM SalesLT.Product AS p
    JOIN [SalesLT].[ProductCategory] AS c
        ON p.ProductCategoryID = c.ProductCategoryID;
    ```

1. أغلق جزء محرر الاستعلام، وتجاهل عمليات التحرير.

> **تلميح**: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure SQL Database.
