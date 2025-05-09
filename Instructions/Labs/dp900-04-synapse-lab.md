<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><markdown-accessiblity-table data-catalyst=""><table tabindex="0">
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
  <td><div dir="rtl">استكشاف تحليلات البيانات في Azure باستخدام Azure Synapse Analytics</div></td>
  <td><div dir="rtl">Explore fundamentals of large-scale data warehousing</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف تحليلات البيانات في Azure باستخدام Azure Synapse Analytics</h1><a id="user-content-استكشاف-تحليلات-البيانات-في-azure-باستخدام-azure-synapse-analytics" class="anchor" aria-label="Permalink: استكشاف تحليلات البيانات في Azure باستخدام Azure Synapse Analytics" href="#استكشاف-تحليلات-البيانات-في-azure-باستخدام-azure-synapse-analytics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا الإجراء، ستقوم بتوفير وظيفة مساحة عمل Azure Synapse Analytics في اشتراكك في Azure، واستخدامها لمعالجة البيانات وتحريها.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>30</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير مساحة عمل Azure Synapse Analytics</h2><a id="user-content-توفير-مساحة-عمل-azure-synapse-analytics" class="anchor" aria-label="Permalink: توفير مساحة عمل Azure Synapse Analytics" href="#توفير-مساحة-عمل-azure-synapse-analytics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لاستخدام Azure Synapse Analytics، يجب توفير مورد مساحة عمل Azure Synapse Analytics في اشتراك Azure.</p>
<ol dir="rtl">
<li>
<p dir="rtl">افتح مدخل Microsoft Azure على <a href="https://portal.azure.com?azure-portal=true" rel="nofollow">https://portal.azure.com</a>، وقم بتسجيل الدخول باستخدام حساب Microsoft المقترن باشتراك Azure.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: تأكد من أنك تعمل في الدليل الذي يحتوي على اشتراكك - المُشار إليه في أعلى اليمين أسفل معرّف مستخدمك. إذا لم تكن كذلك، حدد رمز المستخدم وبدّل الدليل.</p>
</blockquote>
</li>
<li>
<p dir="rtl">في مدخل Microsoft Azure، في صفحة <strong>"Home"</strong>، استخدم <strong>＋ إنشاء رمز مورد</strong> لإنشاء مورد جديد.</p>
</li>
<li>
<p dir="rtl">ابحث عن <em>Azure Synapse Analytics</em>، وإنشاء مورد <strong>Azure Synapse Analytics</strong> جديد باستخدام الإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>Subscription</strong>: <em>اشتراكك في Azure</em>
<ul dir="rtl">
<li><strong>Resource group</strong>: <em>إنشاء مجموعة موارد جديدة ذات اسم فريد مثل "synapse-rg"</em></li>
<li><strong>مجموعة الموارد المُدارة</strong>: <em>أدخل اسماً مناسباً، على سبيل المثال "synapse-managed-rg"</em>.</li>
</ul>
</li>
<li><strong>Workspace name</strong>: <em>أدخل اسماً فريداً لمساحة العمل، على سبيل المثال "synapse-ws-&lt;your_name&gt;"</em>.</li>
<li><strong>«المنطقة»</strong>: <em>حدد أيا من المناطق التالية</em>:
<ul dir="rtl">
<li>شرق أستراليا</li>
<li>Central US</li>
<li>East US 2</li>
<li>أوروبا الشمالية</li>
<li>South Central US</li>
<li>جنوب شرق آسيا</li>
<li>جنوب المملكة المتحدة</li>
<li>أوروبا الغربية</li>
<li>غرب الولايات المتحدة</li>
<li>WestUS 2</li>
</ul>
</li>
<li><strong>حدد "Data Lake Storage Gen 2"</strong>: من الاشتراك
<ul dir="rtl">
<li><strong>اسم الحساب</strong>: <em>إنشاء حساب جديد باسم فريد، على سبيل المثال "&lt;your_name&gt; datalake"</em>.</li>
<li><strong>اسم نظام الملفات</strong>: <em>إنشاء نظام ملفات جديد باسم فريد، على سبيل المثال "fs&lt;your_name&gt;"</em>.</li>
</ul>
</li>
</ul>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: تتطلب مساحة عمل Synapse Analytics مجموعتين من الموارد في اشتراك Azure، مجموعة للموارد التي تُنشئها صراحةً وأخرى للموارد المُدارة التي تستخدمها الخدمة. كما يتطلب حساب تخزين مستودع بيانات لتخزين البيانات والبرامج النصية والبيانات الاصطناعية الأخرى.</p>
</blockquote>
</li>
<li>
<p dir="rtl">عند إدخال هذه التفاصيل، حدد <strong>"Review + create"</strong>، ثم حدد <strong>"Create"</strong> لإنشاء مساحة العمل.</p>
</li>
<li>
<p dir="rtl">انتظر حتى يتم إنشاء مساحة العمل - قد يستغرق ذلك خمس دقائق أو نحو ذلك.</p>
</li>
<li>
<p dir="rtl">عند اكتمال التوزيع انتقل إلى مجموعة الموارد التي تم إنشاؤها ولاحظ أنه يحتوي على مساحة عمل Synapse Analytics وحساب تخزين مستودع البيانات.</p>
</li>
<li>
<p dir="rtl">حدد مساحة عمل Synapse، وفي صفحة <strong>"Overview"</strong> الخاصة بها، في بطاقة <strong>"Open Synapse Studio"</strong>، حدد <strong>"Open"</strong> لفتح Synapse Studio في علامة تبويب متصفح جديدة. Synapse Studio هي واجهة قائمة على الويب يمكنك استخدامها للعمل مع مساحة عمل Synapse Analytics.</p>
</li>
<li>
<p dir="rtl">على الجانب الأيسر من استوديو Synapse، استخدم الرمز <strong>››</strong> لتوسيع القائمة - وهذا يكشف عن الصفحات المختلفة داخل Synapse Studio التي ستستخدمها لإدارة الموارد وتنفيذ مهام تحليل البيانات، كما هو موضح هنا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/synapse-studio.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/synapse-studio.png" alt="صورة توضح قائمة Synapse Studio المُوسّعة لإدارة الموارد وتنفيذ مهام تحليلات البيانات" style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استيعاب البيانات</h2><a id="user-content-استيعاب-البيانات" class="anchor" aria-label="Permalink: استيعاب البيانات" href="#استيعاب-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">واحدة من المهام الرئيسية التي يمكنك القيام بها مع Azure Synapse Analytics هي تحديد <em>البنية الأساسية لبرنامج ربط العمليات التجارية</em> التي تنقل (وإذا لزم الأمر، تُحوّل) البيانات من مجموعة واسعة من المصادر إلى مساحة العمل الخاصة بك للتحليل.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في Synapse Studio، في الصفحة <strong>Home</strong>، حدد <strong>Ingest</strong> لفتح أداة <strong>Copy Data</strong>.</p>
</li>
<li>
<p dir="rtl">في أداة Copy Data، في خطوة <strong>"Properties"</strong>، تأكد من تحديد <strong>"Built-in copy task"</strong> و <strong>"Run once now"</strong>، ثم انقر فوق <strong>"Next &gt;"</strong>.</p>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Source"</strong> في الخطوة الفرعية <strong>"Dataset"</strong> حدد الإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>Source type</strong>: الكل</li>
<li><strong>الاتصال</strong>: <em>أنشئ اتصالًا جديدًا، وفي جزء <strong>إتصال جديد</strong> الذي يظهر، في علامة التبويب <strong>البروتوكول العام</strong>، حدد <strong>HTTP</strong>. ثم تابع وأنشئ اتصالًا بملف بيانات باستخدام الإعدادات التالية:</em>
<ul dir="rtl">
<li><strong>"Name"</strong>: منتجات شركة مغامرة</li>
<li><strong>"Description"</strong>: قائمة المنتجات عبر HTTP</li>
<li><strong>"Connect via integration runtime"</strong>: AutoResolveIntegrationRuntime</li>
<li><strong>"Base URL"</strong>: <code>https://raw.githubusercontent.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/master/Azure-Synapse/products.csv</code></li>
<li><strong>"Server Certificate Validation"</strong>: تمكين</li>
<li><strong>"Authentication type"</strong>: مجهول</li>
</ul>
</li>
</ul>
</li>
<li>
<p dir="rtl">بعد إنشاء الاتصال، على الخطوة الفرعية <strong>"Source/Dataset"</strong> تأكد من تحديد الإعدادات التالية، ثم حدد <strong>"Next &gt;"</strong>:</p>
<ul dir="rtl">
<li><strong>"Source/Dataset"</strong>: <em>اتركه فارغاً</em></li>
<li><strong>طريقة الطلب</strong>: GET</li>
<li><strong>عناوين إضافية</strong>: <em>اتركه فارغاً</em></li>
<li><strong>نسخة ثنائية</strong>: غير مُحدد</li>
<li><strong>مُهلة الطلب</strong>: <em>اتركه فارغاً</em></li>
<li><strong>أقصى الاتصالات المتزامنة</strong>: <em>اتركه فارغاً</em></li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Source"</strong> في الخطوة الفرعية <strong>"Configuration"</strong> حدد <strong>"Preview data"</strong> لرؤية معاينة بيانات المنتج التي سيتم استيعابها في البنية الأساسية لبرنامج ربط العمليات التجارية، ثم أغلق المعاينة.</p>
</li>
<li>
<p dir="rtl">بعد معاينة البيانات، في خطوة <strong>"Source/Configuration"</strong> الفرعية تأكد من تحديد الإعدادات التالية، ثم حدد <strong>"Next &gt;"</strong>:</p>
<ul dir="rtl">
<li><strong>File format</strong>: DelimitedText</li>
<li><strong>عمود محدِّد</strong>: فاصلة (،)</li>
<li><strong>صف محدِّد</strong>: موجز الخط (\n)</li>
<li><strong>"First row as header"</strong>: محدَّد</li>
<li><strong>"Compression type"</strong>: بلا</li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Destination"</strong> في الخطوة الفرعية <strong>"Dataset"</strong> حدد الإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>Destination type</strong>: Azure Data Lake Storage Gen 2</li>
<li><strong>Connection</strong>: <em>حدد الاتصال الموجود بمخزن مستودع البيانات (تم إنشاء هذا لك عند إنشاء مساحة العمل).</em></li>
</ul>
</li>
<li>
<p dir="rtl">بعد تحديد الاتصال، في الخطوة "<strong>Destination/Dataset</strong>" تأكد من تحديد الإعدادات التالية، ثم حدد "<strong>Next &gt;</strong>":</p>
<ul dir="rtl">
<li><strong>مسار الملف</strong>: <em>استعرض للوصول إلى مجلد نظام الملفات</em></li>
<li><strong>اسم الملف</strong>: منتجات.csv</li>
<li><strong>سلوك النسخ</strong>: بلا</li>
<li><strong>أقصى الاتصالات المتزامنة</strong>: <em>اتركه فارغاً</em></li>
<li><strong>حجم الكتلة (ميغا بايت)</strong>: <em>اتركه فارغاً</em></li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Destination"</strong> في الخطوة الفرعية <strong>"Configuration"</strong> تأكد من تحديد الخصائص التالية. ثم حدد <strong>"Next &gt;"</strong>:</p>
<ul dir="rtl">
<li><strong>File format</strong>: DelimitedText</li>
<li><strong>عمود محدِّد</strong>: فاصلة (،)</li>
<li><strong>صف محدِّد</strong>: موجز الخط (\n)</li>
<li><strong>"Add header to file"</strong>: مُحدَّد</li>
<li><strong>"Compression type"</strong>: بلا</li>
<li><strong>"Max rows per file"</strong>: <em>اتركه فارغاً</em></li>
<li><strong>"File name prefix"</strong>: <em>اتركه فارغاً</em></li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Settings"</strong> أدخل الإعدادات التالية ثم انقر فوق <strong>"Next &gt;"</strong>:</p>
<ul dir="rtl">
<li><strong>اسم المهمة</strong>: نسخ المنتجات</li>
<li><strong>وصف المهمة</strong> نسخ بيانات المنتجات</li>
<li><strong>التسامح مع الخطأ</strong>: <em>اتركه فارغاً</em></li>
<li><strong>تمكين التسجيل</strong>: إلغاء التحديد</li>
<li><strong>تمكين التشغيل المرحلي</strong>: إلغاء التحديد</li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Review and finish"</strong> في الخطوة الفرعية <strong>"Review"</strong> اقرأ الملخص ثم انقر فوق <strong>"Next &gt;"</strong>.</p>
</li>
<li>
<p dir="rtl">في خطوة <strong>"Deployment"</strong> الفرعية، انتظر البنية الأساسية لبرنامج ربط العمليات التجارية لتُوزّع، ثم انقر فوق <strong>"Finish"</strong>.</p>
</li>
<li>
<p dir="rtl">في Synapse Studio، حدد صفحة "<strong>Monitor</strong>"، وفي علامة التبويب "<strong>Pipeline runs</strong>"، انتظر حتى اكتمال البنية الأساسية لبرنامج ربط العمليات التجارية "<strong>Copy products</strong>" بحالة "<strong>Succeeded</strong>" (يمكنك استخدام الزر "<strong>↻ Refresh</strong>" في صفحة "Pipeline runs" لتحديث الحالة).</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>"Data"</strong> حدد علامة التبويب <strong>"Linked"</strong> ثم قم بتوسيع التدرج الهرمي <strong>Azure Data Lake Storage Gen 2</strong> حتى تشاهد تخزين الملف لمساحة عمل Synapse. ثم حدد تخزين الملف للتحقق من نسخ ملف اسمه <strong>products.csv</strong> إلى هذا الموقع، كما هو موضح هنا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/synapse-storage.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/synapse-storage.png" alt="صورة توضح عرض Synapse Studio الموسع لتدرج Azure Data Lake Storage Gen 2 الهرمي مع تخزين الملفات لمساحة عمل Synapse" style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام تجمع SQL لتحليل البيانات</h2><a id="user-content-استخدام-تجمع-sql-لتحليل-البيانات" class="anchor" aria-label="Permalink: استخدام تجمع SQL لتحليل البيانات" href="#استخدام-تجمع-sql-لتحليل-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن قمت باستيعاب بعض البيانات في مساحة العمل الخاصة بك، يمكنك استخدام Synapse Analytics للاستعلام عنها وتحليلها. واحدة من الطرق الأكثر شيوعاً للاستعلام عن البيانات هي استخدام SQL، وفي Synapse Analytics يمكنك استخدام <em>تجمّع SQL</em> لتشغيل التعليمات البرمجية لـ SQL.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في Synapse Studio، انقر بزر الماوس الأيمن فوق ملف <strong>"products.csv"</strong> في تخزين الملفات لمساحة عمل Synapse، أشر إلى <strong>البرنامج النصي SQL الجديد</strong>وحدد <strong>"Select TOP 100 rows"</strong>.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>SQL Script 1</strong> الذي يفتح، راجع التعليمات البرمجية لـ SQL التي تم إنشاؤها، والتي يجب أن تكون مشابهة لهذا:</p>
</li>
<div class="highlight highlight-source-sql notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"><span class="pl-c">--</span> This is auto-generated code</span>
<span class="pl-k">SELECT</span>
    TOP <span class="pl-c1">100</span> <span class="pl-k">*</span>
<span class="pl-k">FROM</span>
    OPENROWSET(
        BULK <span class="pl-s"><span class="pl-pds">'</span>https://datalakexx.dfs.core.windows.net/fsxx/products.csv<span class="pl-pds">'</span></span>,
        FORMAT <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">'</span>CSV<span class="pl-pds">'</span></span>,
        PARSER_VERSION<span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">'</span>2.0<span class="pl-pds">'</span></span>
    ) <span class="pl-k">AS</span> [result]</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="-- This is auto-generated code
SELECT
    TOP 100 *
FROM
    OPENROWSET(
        BULK 'https://datalakexx.dfs.core.windows.net/fsxx/products.csv',
        FORMAT = 'CSV',
        PARSER_VERSION='2.0'
    ) AS [result]" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="rtl">يفتح هذا الرمز مجموعة سجلات من الملف النصي الذي قمت باستيراده ويسترد أول 100 سجل من البيانات.</p>
</li>
<li>
<p dir="rtl">في قائمة <strong>الاتصال بـ</strong>، تأكد من تحديد <strong>"Built-in"</strong> - يمثل هذا تجمّع SQL المُدمج الذي تم إنشاؤه باستخدام مساحة العمل الخاصة بك.</p>
</li>
<li>
<p dir="rtl">على شريط الأدوات، استخدم الزر <strong>"▷ Run"</strong> لتشغيل التعليمات البرمجية لـ SQL، ومراجعة النتائج، والتي يجب أن تبدو مشابهة لهذا:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>C1</th>
<th>c2</th>
<th>c3</th>
<th>c4</th>
</tr>
</thead>
<tbody>
<tr>
<td>معرّف المنتج</td>
<td>ProductName</td>
<td>الفئة</td>
<td>ListPrice</td>
</tr>
<tr>
<td>771</td>
<td>Mountain-100 Silver, 38</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>772</td>
<td>Mountain-100 Silver, 42</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">لاحظ أن النتائج تتكون من أربعة أعمدة تسمى C1 وC2 وC3 وC4؛ وأن الصف الأول في النتائج يحتوي على أسماء حقول البيانات. لحل هذه المشكلة، قم بإضافة معلمات HEADER_ROW = TRUE إلى الدالة OPENROWSET كما هو موضح هنا (استبدال <em>datalakexx</em> و<em>fsxx</em> بأسماء حساب تخزين مستودع البيانات ونظام الملفات)، ثم قم بإعادة تشغيل الاستعلام:</p>
</li>
<div class="highlight highlight-source-sql notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">SELECT</span>
    TOP <span class="pl-c1">100</span> <span class="pl-k">*</span>
<span class="pl-k">FROM</span>
    OPENROWSET(
        BULK <span class="pl-s"><span class="pl-pds">'</span>https://datalakexx.dfs.core.windows.net/fsxx/products.csv<span class="pl-pds">'</span></span>,
        FORMAT <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">'</span>CSV<span class="pl-pds">'</span></span>,
        PARSER_VERSION<span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">'</span>2.0<span class="pl-pds">'</span></span>,
        HEADER_ROW <span class="pl-k">=</span> TRUE
    ) <span class="pl-k">AS</span> [result]</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="SELECT
    TOP 100 *
FROM
    OPENROWSET(
        BULK 'https://datalakexx.dfs.core.windows.net/fsxx/products.csv',
        FORMAT = 'CSV',
        PARSER_VERSION='2.0',
        HEADER_ROW = TRUE
    ) AS [result]" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="rtl">الآن تبدو النتائج كما يلي:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>معرّف المنتج</th>
<th>ProductName</th>
<th>الفئة</th>
<th>ListPrice</th>
</tr>
</thead>
<tbody>
<tr>
<td>771</td>
<td>Mountain-100 Silver, 38</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>772</td>
<td>Mountain-100 Silver, 42</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">تعديل الاستعلام كما يلي (استبدال <em>datalakexx</em> و<em>fsxx</em> بأسماء حساب تخزين مستودع البيانات ونظام الملفات):</p>
</li>
<div class="highlight highlight-source-sql notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">SELECT</span>
    Category, <span class="pl-c1">COUNT</span>(<span class="pl-k">*</span>) <span class="pl-k">AS</span> ProductCount
<span class="pl-k">FROM</span>
    OPENROWSET(
        BULK <span class="pl-s"><span class="pl-pds">'</span>https://datalakexx.dfs.core.windows.net/fsxx/products.csv<span class="pl-pds">'</span></span>,
        FORMAT <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">'</span>CSV<span class="pl-pds">'</span></span>,
        PARSER_VERSION<span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">'</span>2.0<span class="pl-pds">'</span></span>,
        HEADER_ROW <span class="pl-k">=</span> TRUE
    ) <span class="pl-k">AS</span> [result]
<span class="pl-k">GROUP BY</span> Category;</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="SELECT
    Category, COUNT(*) AS ProductCount
FROM
    OPENROWSET(
        BULK 'https://datalakexx.dfs.core.windows.net/fsxx/products.csv',
        FORMAT = 'CSV',
        PARSER_VERSION='2.0',
        HEADER_ROW = TRUE
    ) AS [result]
GROUP BY Category;" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">تشغيل الاستعلامات المعدّلة التي يجب أن يعرض مجموعة النتائج التي تحتوي على عدد المنتجات في كل فئة، مثل هذا:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>الفئة</th>
<th>عدد المنتجات</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bib-Shorts</td>
<td>3</td>
</tr>
<tr>
<td>Bike Racks</td>
<td>1</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">في جزء <strong>"Properties"</strong> لـ <strong>البرنامج النصي 1 SQL</strong>، قم بتغيير <strong>الاسم</strong> إلى <strong>عدد المنتجات حسب الفئة</strong>. ثم في شريط الأدوات، حدد <strong>"Publish"</strong> لحفظ البرنامج النصي.</p>
</li>
<li>
<p dir="rtl">أغلق جزء البرنامج النصي <strong>"Count Products by Category"</strong>.</p>
</li>
<li>
<p dir="rtl">في استوديو Synapse، حدد الصفحة <strong>"Develop"</strong> ولاحظ أنه تم حفظ البرنامج النصي SQL <strong>عدد منتجات المنشورة حسب الفئة</strong> هناك.</p>
</li>
<li>
<p dir="rtl">حدد البرنامج النصي SQL <strong>"Count Products by Category"</strong> لإعادة فتحه. ثم تأكد من أن البرنامج النصي متصل بتجمّع SQL <strong>المُضمن</strong> وتشغيله لاسترداد عدد المنتجات.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>"Results"</strong> حدد طريقة عرض <strong>"Chart"</strong> ثم حدد الإعدادات التالية للتخطيط:</p>
<ul dir="rtl">
<li><strong>نوع المخطط</strong>: عمود</li>
<li><strong>فئة العمود</strong>: الفئة</li>
<li><strong>أعمدة وسيلة الإيضاح (السلسلة)</strong>: عدد المنتجات</li>
<li><strong>موقف وسيلة الإيضاح</strong>: أسفل - وسط</li>
<li><strong>تسمية وسيلة الإيضاح</strong>: <em>اتركه فارغاً</em></li>
<li><strong>القيمة الصغرى لوسيلة الإيضاح (السلسلة)</strong>: <em>اتركه فارغاً</em></li>
<li><strong>القيمة الكبرى لوسيلة الإيضاح (السلسلة)</strong>: <em>اتركه فارغاً</em></li>
<li><strong>تسمية الفئة</strong>: <em>اتركه فارغاً</em></li>
</ul>
<p dir="rtl">يجب أن يشبه المخطط الناتج هذا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/column-chart.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/column-chart.png" alt="صورة تَعرض طريقة عرض مخطط بياني لعدد المنتجات" style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام تجمع Spark لتحليل البيانات</h2><a id="user-content-استخدام-تجمع-spark-لتحليل-البيانات" class="anchor" aria-label="Permalink: استخدام تجمع Spark لتحليل البيانات" href="#استخدام-تجمع-spark-لتحليل-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في حين أن SQL هي لغة شائعة للاستعلام عن مجموعات البيانات المُنظمة، يجد العديد من محللي البيانات لغات مثل Python مفيدة لاستكشاف وإعداد البيانات للتحليل. في تحليلات Azure Synapse، يمكنك تشغيل رمز Python (وغيره) في <em>تجمّع Spark</em>؛ الذي يستخدم محرك معالجة البيانات الموزعة على أساس Apache Spark.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في استوديو Synapse، حدد صفحة <strong>"Manage"</strong>.</p>
</li>
<li>
<p dir="rtl">حدد علامة التبويب <strong>"Apache Spark pools"</strong> ثم استخدم رمز <strong>&amp;#65291، جديد</strong> لإنشاء تجمّع Spark جديد بالإعدادات التالية:</p>
<ul dir="rtl">
<li>**اسم وعاء Apache Spark **: spark</li>
<li><strong>حجم عقدة المجموعة</strong>: الذاكرة محسنة</li>
<li><strong>حجم العقدة</strong>: صغير (4 vCores / 32 GB)</li>
<li><strong>تحجيم تلقائي</strong>: ُممكّن</li>
<li><strong>عدد العقد</strong> 3----3</li>
</ul>
</li>
<li>
<p dir="rtl">مراجعة وإنشاء تجمّع Spark ثم انتظر حتى عملية التوزيع (التي قد تستغرق بضع دقائق).</p>
</li>
<li>
<p dir="rtl">عند توزيع تجمّع Spark في Synapse Studio على صفحة <strong>"Data"</strong> استعرض للوصول إلى نظام الملفات لمساحة عمل Synapse. ثم انقر بزر الماوس الأيمن فوق <strong>"products.csv"</strong>، أشر إلى <strong>"New notebook"</strong>، وحدد <strong>"Load to DataFrame"</strong>.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>"Notebook 1"</strong> الذي يفتح، في القائمة <strong>"Attach to"</strong> حدد تجمع <strong>"spark"</strong> المُنشأ مسبقاً وتأكد من تعيين <strong>اللغة</strong> إلى <strong>PySpark (Python)</strong>.</p>
</li>
<li>
<p dir="rtl">راجع التعليمات البرمجية في الخلية الأولى (والوحيدة) في دفتر الملاحظات، والتي يجب أن تبدو كما يلي:</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c1">%</span><span class="pl-c1">%</span><span class="pl-s1">pyspark</span>
<span class="pl-s1">df</span> <span class="pl-c1">=</span> <span class="pl-s1">spark</span>.<span class="pl-c1">read</span>.<span class="pl-c1">load</span>(<span class="pl-s">'abfss://fsxx@datalakexx.dfs.core.windows.net/products.csv'</span>, <span class="pl-s1">format</span><span class="pl-c1">=</span><span class="pl-s">'csv'</span>
<span class="pl-c">## If header exists uncomment line below</span>
<span class="pl-c">##, header=True</span>
)
<span class="pl-en">display</span>(<span class="pl-s1">df</span>.<span class="pl-c1">limit</span>(<span class="pl-c1">10</span>))</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="%%pyspark
df = spark.read.load('abfss://fsxx@datalakexx.dfs.core.windows.net/products.csv', format='csv'
## If header exists uncomment line below
##, header=True
)
display(df.limit(10))" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">حدد "<strong>▷ Run</strong>" الموجود يسار الخلية البرمجية لتشغيله، وانتظر النتائج. في المرة الأولى التي تقوم فيها بتشغيل خلية في دفتر ملاحظات، يتم بدء تشغيل تجمّع Spark - لذلك قد يستغرق الأمر دقيقة أو نحو ذلك لإرجاع أي نتائج.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: في حالة حدوث خطأ بسبب عدم توفر Python Kernel بعد، أعد تشغيل الخلية.</p>
</blockquote>
</li>
<li>
<p dir="rtl">في نهاية المطاف، يجب أن تظهر النتائج أسفل الخلية، ويجب أن تكون مشابهة لهذا:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th><em>c0</em></th>
<th><em>c1</em></th>
<th><em>c2</em></th>
<th><em>c3</em></th>
</tr>
</thead>
<tbody>
<tr>
<td>معرّف المنتج</td>
<td>ProductName</td>
<td>الفئة</td>
<td>ListPrice</td>
</tr>
<tr>
<td>771</td>
<td>Mountain-100 Silver, 38</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>772</td>
<td>Mountain-100 Silver, 42</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">إلغاء اتصال خط <em>header=True</em> (لأن الملف products.csv يحتوي على رؤوس الأعمدة في السطر الأول)، بحيث تبدو التعليمات البرمجية الخاصة بك كما يلي:</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c1">%</span><span class="pl-c1">%</span><span class="pl-s1">pyspark</span>
<span class="pl-s1">df</span> <span class="pl-c1">=</span> <span class="pl-s1">spark</span>.<span class="pl-c1">read</span>.<span class="pl-c1">load</span>(<span class="pl-s">'abfss://fsxx@datalakexx.dfs.core.windows.net/products.csv'</span>, <span class="pl-s1">format</span><span class="pl-c1">=</span><span class="pl-s">'csv'</span>
<span class="pl-c">## If header exists uncomment line below</span>
, <span class="pl-s1">header</span><span class="pl-c1">=</span><span class="pl-c1">True</span>
)
<span class="pl-en">display</span>(<span class="pl-s1">df</span>.<span class="pl-c1">limit</span>(<span class="pl-c1">10</span>))</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="%%pyspark
df = spark.read.load('abfss://fsxx@datalakexx.dfs.core.windows.net/products.csv', format='csv'
## If header exists uncomment line below
, header=True
)
display(df.limit(10))" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">أعد تشغيل الخلية وتحقق من أن النتائج تبدو كما يلي:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>معرّف المنتج</th>
<th>ProductName</th>
<th>الفئة</th>
<th>ListPrice</th>
</tr>
</thead>
<tbody>
<tr>
<td>771</td>
<td>Mountain-100 Silver, 38</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>772</td>
<td>Mountain-100 Silver, 42</td>
<td>Mountain Bikes</td>
<td>3399.9900</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<p dir="rtl">لاحظ أن تشغيل الخلية مرة أخرى يستغرق وقتاً أقل، لأن تجمع Spark قد بدأ بالفعل.</p>
</li>
<li>
<p dir="rtl">ضمن النتائج، استخدم رمز <strong>"التعليمة ＋"</strong> لإضافة خلية تعليمة برمجية جديدة إلى دفتر الملاحظات.</p>
</li>
<li>
<p dir="rtl">في خلية التعليمات البرمجية الفارغة الجديدة، أضف التعليمات البرمجية التالية:</p>
</li>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-s1">df_counts</span> <span class="pl-c1">=</span> <span class="pl-s1">df</span>.<span class="pl-c1">groupBy</span>(<span class="pl-s1">df</span>.<span class="pl-c1">Category</span>).<span class="pl-c1">count</span>()
<span class="pl-en">display</span>(<span class="pl-s1">df_counts</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="df_counts = df.groupBy(df.Category).count()
display(df_counts)" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">حدد "<strong>▷ Run</strong>" الموجود على اليسار لتشغيل خلية التعليمات البرمجية الجديدة، وراجع النتائج التي يجب أن تبدو مشابهة لهذا:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>الفئة</th>
<th>عدد</th>
</tr>
</thead>
<tbody>
<tr>
<td>سماعة الرأس</td>
<td>3</td>
</tr>
<tr>
<td>العجلات</td>
<td>14</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">في إخراج النتائج للخلية، حدد طريقة عرض <strong>المخطط</strong>. يجب أن يشبه المخطط الناتج هذا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/bar-chart.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/bar-chart.png" alt="صورة تعرض عرض المخطط البياني لعدد الفئات" style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">أغلق جزء <strong>Notebook 1</strong> وتجاهل التغييرات.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قم بحذف موارد Azure.</h2><a id="user-content-قم-بحذف-موارد-azure" class="anchor" aria-label="Permalink: قم بحذف موارد Azure." href="#قم-بحذف-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">إذا انتهيت من استكشاف Azure Synapse Analytics، يجب حذف الموارد التي أنشأتها لتجنب تكاليف Azure غير الضرورية.</p>
<ol dir="rtl">
<li>
<p dir="rtl">أغلق علامة التبويب مستعرض Studio browser ثم العودة إلى مدخل Microsoft Azure.</p>
</li>
<li>
<p dir="rtl">في مدخل Microsoft Azure، في الصفحة ⁧<strong>الرئيسية</strong>⁩، حدّد ⁧ <strong>"Resource groups"⁦⁩⁧</strong>⁩.</p>
</li>
<li>
<p dir="rtl">حدد مجموعة الموارد لمساحة عمل Synapse Analytics (وليس مجموعة الموارد المدارة)، وتحقق من أنها تحتوي على مساحة عمل Synapse وحساب التخزين وتجمّع Spark لمساحة العمل.</p>
</li>
<li>
<p dir="rtl">في أعلى صفحة <strong>"Overview"</strong> لمجموعة الموارد، حدد <strong>"Delete resource group"</strong>.</p>
</li>
<li>
<p dir="rtl">أدخل اسم مجموعة الموارد لتأكيد رغبتك في حذفه، ثم حدد <strong>"Delete"</strong>.</p>
<p dir="rtl">بعد بضع دقائق، سيتم حذف مساحة عمل Azure Synapse ومساحة العمل المُدارة المقترنة بها.</p>
</li>
</ol>
</article></div>
