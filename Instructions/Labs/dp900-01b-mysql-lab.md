---
lab:
  title: استكشاف Azure Database for MySQL
  module: Explore relational data in Azure
---

# استكشاف Azure Database for MySQL

ستُوفّر في هذا التمرين مورد Azure Database for MySQL في اشتراك Azure.

سيستغرق إكمال هذا التمرين المعملي **5** دقائق.

## قبل أن تبدأ

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## توفير مورد Azure Database for MySQL

ستقوم في هذا التمرين بتوفير مورد Azure Database for MySQL.

1. في مدخل Microsoft Azure، حدد «**&#65291; Create a resource**» من الزاوية اليسرى العليا وابحث عن *Azure Database for MySQL*. ثم في صفحة نتائج **Azure Database for MySQL**، حدد «**Create**».

1. راجع خيارات Azure Database for MySQL المتوفرة. وبالنسبة إلى **Resource type**، حدد **Flexible Server** وحدد **Create**.

    ![لقطة شاشة لخيارات توزيع Azure Database for MySQL](images/mysql-options.png)

1. أدخل القيم التالية في صفحة **Create SQL Database**:
    - **الاشتراك**: حدد اشتراك Azure الخاص بك.
    - **مجموعة الموارد**: قم بإنشاء مجموعة موارد جديدة باسم من اختيارك.
    - **New Server**: أدخل اسمًا مميزًا.
    - **Region**: أي موقع متوفر بالقرب منك.
    - **MySQL Version**: اتركه دون تغيير.
    - **Workload type**: لمشاريع التطوير أو الهواية.
    - **Compute + storage**: اتركه دون تغيير.
    - **Availability zone**: اتركه دون تغيير.
    - **Enable high availability**: اتركه دون تغيير.
    - **Admin username**: اسمك
    - **Password** و**Confirm password**: كلمة مرور معقدة مناسبة

1. حدد **Next: Networking**.

1. ضمن "**Firewall rules**"، حدد "**&#65291; Add current client IP address**".

1. حدد "**Review + Create**"، ثم حدد "**Create**" لإنشاء قاعدة بيانات Azure MySQL.

1. يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى المورد الذي تم توزيعه، والذي يجب أن يبدو كما يلي:

    ![لقطة شاشة لمدخل Azure تعرض صفحة "Azure Database for MySQL".](images/mysql-portal.png)

1. راجع خيارات إدارة مورد Azure Database for MySQL.

> **تلميح**: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Database for MySQ.
