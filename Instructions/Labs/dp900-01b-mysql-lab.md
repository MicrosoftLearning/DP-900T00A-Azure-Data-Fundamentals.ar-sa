<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div dir="rtl"><markdown-accessiblity-table data-catalyst=""><table>
  <thead>
  <tr>
  <th>lab</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl"><table>
  <thead>
  <tr>
  <th>title</th>
  <th>module</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl">استكشاف Azure Database for MySQL</div></td>
  <td><div dir="rtl">Explore relational data in Azure</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Database for MySQL</h1><a id="user-content-استكشاف-azure-database-for-mysql" class="anchor" aria-label="Permalink: استكشاف Azure Database for MySQL" href="#استكشاف-azure-database-for-mysql"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستُوفّر في هذا التمرين مورد Azure Database for MySQL في اشتراك Azure.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>5</strong> دقائق.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير مورد Azure Database for MySQL</h2><a id="user-content-توفير-مورد-azure-database-for-mysql" class="anchor" aria-label="Permalink: توفير مورد Azure Database for MySQL" href="#توفير-مورد-azure-database-for-mysql"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستقوم في هذا التمرين بتوفير مورد Azure Database for MySQL.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في مدخل Microsoft Azure، حدد «<strong>＋ Create a resource</strong>» من الزاوية اليسرى العليا وابحث عن <em>Azure Database for MySQL</em>. ثم في صفحة نتائج <strong>Azure Database for MySQL</strong>، حدد «<strong>Create</strong>».</p>
</li>
<li>
<p dir="rtl">راجع خيارات Azure Database for MySQL المتوفرة. وبالنسبة إلى <strong>Resource type</strong>، حدد <strong>Flexible Server</strong> وحدد <strong>Create</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/mysql-options.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/mysql-options.png" alt="لقطة شاشة لخيارات توزيع Azure Database for MySQL" style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">أدخل القيم التالية في صفحة <strong>Create SQL Database</strong>:</p>
<ul dir="rtl">
<li><strong>الاشتراك</strong>: حدد اشتراك Azure الخاص بك.</li>
<li><strong>مجموعة الموارد</strong>: قم بإنشاء مجموعة موارد جديدة باسم من اختيارك.</li>
<li><strong>New Server</strong>: أدخل اسمًا مميزًا.</li>
<li><strong>Region</strong>: أي موقع متوفر بالقرب منك.</li>
<li><strong>MySQL Version</strong>: اتركه دون تغيير.</li>
<li><strong>Workload type</strong>: لمشاريع التطوير أو الهواية.</li>
<li><strong>Compute + storage</strong>: اتركه دون تغيير.</li>
<li><strong>Availability zone</strong>: اتركه دون تغيير.</li>
<li><strong>Enable high availability</strong>: اتركه دون تغيير.</li>
<li><strong>Admin username</strong>: اسمك</li>
<li><strong>Password</strong> و<strong>Confirm password</strong>: كلمة مرور معقدة مناسبة</li>
</ul>
</li>
<li>
<p dir="rtl">حدد <strong>Next: Networking</strong>.</p>
</li>
<li>
<p dir="rtl">ضمن "<strong>Firewall rules</strong>"، حدد "<strong>＋ Add current client IP address</strong>".</p>
</li>
<li>
<p dir="rtl">حدد "<strong>Review + Create</strong>"، ثم حدد "<strong>Create</strong>" لإنشاء قاعدة بيانات Azure MySQL.</p>
</li>
<li>
<p dir="rtl">يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى المورد الذي تم توزيعه، والذي يجب أن يبدو كما يلي:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/mysql-portal.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/mysql-portal.png" alt="لقطة شاشة لمدخل Azure تعرض صفحة &quot;Azure Database for MySQL&quot;." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">راجع خيارات إدارة مورد Azure Database for MySQL.</p>
</li>
</ol>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Database for MySQ.</p>
</blockquote>
</article></div>
