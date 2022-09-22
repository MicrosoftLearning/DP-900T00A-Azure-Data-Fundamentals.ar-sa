---
lab:
  title: استكشاف Azure Database for PostgreSQL
  module: Explore relational data in Azure
---

# <a name="explore-azure-database-for-postgresql"></a>استكشاف Azure Database for PostgreSQL

ستُوفّر في هذا التمرين مورد Azure Database for PostgreSQL في اشتراك Azure.

سيستغرق إكمال هذا التمرين المعملي **5** دقائق.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="provision-an-azure-database-for-postgresql-resource"></a>توفير مورد Azure Database for PostgreSQL

ستقوم في هذا التمرين بتوفير مورد Azure Database for PostgreSQL.

1. In the Azure portal, select <bpt id="p1">**</bpt>&amp;#65291; Create a resource<ept id="p1">**</ept> from the upper left-hand corner and search for <bpt id="p2">*</bpt>Azure Database for PostgreSQL<ept id="p2">*</ept>. Then in the resulting <bpt id="p1">**</bpt>Azure Database for PostgreSQL<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Create<ept id="p2">**</ept>.

1. راجع خيارات Azure Database for PostgreSQL المتوفرة، ثم من إطار «**Single server**»، حدد «**Create**».

    ![لقطة شاشة لخيارات توزيع Azure Database for PostgreSQL](images/postgresql-options.png)

1. أدخل القيم التالية في صفحة **Create SQL Database**:
    - **الاشتراك**: حدد اشتراك Azure الخاص بك.
    - **Resource group**: أنشئ مجموعة موارد جديدة وامنحها اسماً تختاره.
    - **New Server**: أدخل اسمًا مميزًا.
    - **Region**: حدد منطقة قريبة منك.
    - **PostgreSQL version**: اتركه دون تغيير.
    - **Workload type**: حدد "**Development**".
    - **Compute + storage**: اتركه دون تغيير.
    - **Availability zone**: اتركه دون تغيير.
    - **Enable high availability**: اتركه دون تغيير.
    - **Admin username**: اكتب اسمك.
    - **Password** و**Confirm password**: كلمة مرور معقدة مناسبة.

1. حدد **Next: Networking**.

1. ضمن "**Firewall rules**"، حدد " **&#65291; Add current client IP address**".

1. حدد "**Review + Create**"، ثم حدد "**Create**" لإنشاء قاعدة بيانات Azure PostgreSQL.

1. Wait for deployment to complete. Then go to the resource that was deployed, which should look like this:

    ![لقطة شاشة لمدخل Azure تعرض صفحة "Azure Database for PostgreSQL".](images/postgresql-portal.png)

1. راجع خيارات إدارة مورد Azure Database for PostreSQL.

> **تلميح**: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Database for PostreSQL.
