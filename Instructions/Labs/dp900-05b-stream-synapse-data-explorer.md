<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><markdown-accessiblity-table data-catalyst=""><table>
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
  <td><div dir="rtl">استكشاف Azure Synapse Data Explorer</div></td>
  <td><div dir="rtl">Explore fundamentals of real-time analytics</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Synapse Data Explorer</h1><a id="user-content-استكشاف-azure-synapse-data-explorer" class="anchor" aria-label="Permalink: استكشاف Azure Synapse Data Explorer" href="#استكشاف-azure-synapse-data-explorer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: بسبب تغييرات المنتج، هناك بعض المشكلات المعروفة في قسم <strong>إنشاء قاعدة بيانات واستيعاب البيانات</strong> في هذا التمرين العملي. ونحن نعمل على معالجة هذه المشكلات.</p>
</blockquote>
<p dir="rtl">في هذا التمرين، ستستخدم Azure Synapse Data Explorer لتحليل بيانات التسلسل الزمني.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>25</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير مساحة عمل Synapse Analytics</h2><a id="user-content-توفير-مساحة-عمل-synapse-analytics" class="anchor" aria-label="Permalink: توفير مساحة عمل Synapse Analytics" href="#توفير-مساحة-عمل-synapse-analytics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: إذا كنت تمتلك Azure Synapse Workspace من التمرين السابق، فتخطَّ هذا القسم وانتقل مباشرة إلى قسم <strong><a href="#create-a-data-explorer-pool">إنشاء تجمّع Data Explorer</a></strong>.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">افتح مدخل Microsoft Azure على <a href="https://portal.azure.com?azure-portal=true" rel="nofollow">https://portal.azure/com</a>، وقم بتسجيل الدخول باستخدام حساب Microsoft المقترن باشتراك Azure.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: تأكد من أنك تعمل في الدليل الذي يحتوي على اشتراكك - المُشار إليه في أعلى اليمين أسفل معرّف المستخدم. إذا لم تكن كذلك، حدد رمز المستخدم وبدّل الدليل.</p>
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
<li><strong>اسم مساحة العمل</strong>: <em>أدخل اسم مساحة عمل فريدة، على سبيل المثال "synapse-ws-&lt;your_name&gt;</em>.</li>
<li><strong>المنطقة</strong>: <em>اختر أي منطقة متوفرة</em>.</li>
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
<p dir="rtl">على الجانب الأيسر من Synapse Studio، استخدم أيقونة <strong>››</strong> لتوسيع القائمة - ما يكشف عن الصفحات المختلفة داخل Synapse Studio التي ستستخدمها لإدارة الموارد وتنفيذ مهام تحليل البيانات</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء تجمع Data Explorer</h2><a id="user-content-إنشاء-تجمع-data-explorer" class="anchor" aria-label="Permalink: إنشاء تجمع Data Explorer" href="#إنشاء-تجمع-data-explorer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>في استوديو Synapse، حدد صفحة <strong>"Manage"</strong>.</li>
<li>حدد علامة التبويب "<strong>Data Explorer pools</strong>"، ثم استخدم رمز "<strong>＋ New</strong>" لإنشاء تجمّع جديد بالإعدادات التالية:
<ul dir="rtl">
<li><strong>اسم تجمع Data Explorer</strong>: dxpool</li>
<li><strong>حمل العمل</strong>: الحوسبة المحسّنة</li>
<li><strong>الحجم</strong>: صغير جدا (2 ذاكرة أساسية)</li>
</ul>
</li>
<li>حدد "<strong>Next: Additional Settings &gt;</strong>" ومكّن الإعداد "<strong>Streaming ingestion</strong>" - ما يمكّن Data Explorer من استيعاب بيانات جديدة من مصدر دفق مثل مراكز الأحداث.</li>
<li>حدد <strong>Review and create</strong> لإنشاء تجمّع Data Explorer، ثم انتظر حتى يتم توزيعه (والذي قد يستغرق 15 دقيقة أو أكثر - ستتغير الحالة من <em>Creating</em> إلى <em>Online</em>).</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء قاعدة بيانات واستيعاب البيانات</h2><a id="user-content-إنشاء-قاعدة-بيانات-واستيعاب-البيانات" class="anchor" aria-label="Permalink: إنشاء قاعدة بيانات واستيعاب البيانات" href="#إنشاء-قاعدة-بيانات-واستيعاب-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في Synapse Studio، حدد الصفحة <strong>Data</strong>.</p>
</li>
<li>
<p dir="rtl">تأكد من تحديد علامة التبويب "<strong>Workspace</strong>"، وإذا لزم الأمر، فحدد الرمز "<strong>↻</strong>" في أعلى الجزء الأيسر من الصفحة لتحديث طريقة العرض بحيث تُدرج "<strong>Data Explorer databases</strong>".</p>
</li>
<li>
<p dir="rtl">قم بتوسيع <strong>قواعد بيانات Data Explorer</strong> وتحقق من إدراج <strong>dxpool</strong>.</p>
</li>
<li>
<p dir="rtl">في الجزء "<strong>Data</strong>"، استخدم الرمز "<strong>＋</strong>" لإنشاء "<strong>Data Explorer database</strong>" جديدة في التجمّع "<strong>dxpool</strong>" باسم <strong>iot-data</strong>.</p>
</li>
<li>
<p dir="rtl">أثناء انتظار إنشاء قاعدة البيانات، نزّل <strong>devices.csv</strong> من <a href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/streaming/data/devices.csv?azure-portal=true">https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/streaming/data/devices.csv</a>، واحفظه في أي مجلد على جهاز الكمبيوتر المحلي.</p>
</li>
<li>
<p dir="rtl">في Synapse Studio، انتظر حتى يتم إنشاء قاعدة البيانات إذا لزم الأمر، ثم في القائمة <strong>...</strong> لقاعدة البيانات <strong>iot-data</strong> الجديدة، حدد <strong>Open in Azure Data Explorer</strong>.</p>
</li>
<li>
<p dir="rtl">في علامة تبويب المتصفح الجديد الذي يحتوي على Azure Data Explorer، في علامة التبويب <strong>Data</strong>، حدد <strong>Ingest new data</strong>.</p>
</li>
<li>
<p dir="rtl">في الصفحة <strong>Destination</strong>، حدد الإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>نظام المجموعة</strong>: <em>تجمّع Data Explorer <strong>dxpool</strong> في مساحة عمل Azure Synapse</em></li>
<li><strong>قاعدة البيانات</strong>: iot-data</li>
<li><strong>الجدول</strong>: أنشئ جدولاً جديداً يسمى <strong>devices</strong></li>
</ul>
</li>
<li>
<p dir="rtl">حدد <strong>Next: Source</strong> وفي الصفحة <strong>Source</strong> حدد الخيارات التالية:</p>
<ul dir="rtl">
<li><strong>Source type</strong>: File</li>
<li><strong>Files</strong>: قم بتحميل الملف <strong>devices.csv</strong> من جهاز الكمبيوتر المحلي.</li>
</ul>
</li>
<li>
<p dir="rtl">حدد <strong>Next: Schema</strong> وفي الصفحة <strong>Schema</strong>، تأكد من صحة الإعدادات التالية:</p>
<ul dir="rtl">
<li><strong>Compression type</strong>: Uncompressed</li>
<li><strong>Data format</strong>: CSV</li>
<li><strong>Ignore the first record</strong>:  تحديد</li>
<li><strong>Mapping</strong>: devices_mapping</li>
</ul>
</li>
<li>
<p dir="rtl">تأكد من تحديد أنواع بيانات الأعمدة بشكل صحيح على لتكون <em>Time (datetime)</em>، و<em>Device (string)</em>، و<em>Value (long)</em>). ثم حدد <strong>Next: Start Ingestion</strong>.</p>
</li>
<li>
<p dir="rtl">عند اكتمال الاستيعاب، حدد <strong>Close</strong>.</p>
</li>
<li>
<p dir="rtl">في Azure Data Explorer، ضمن علامة التبويب <strong>Query</strong>، تأكد من تحديد قاعدة بيانات <strong>iot-data</strong>، ثم أدخل الاستعلام التالي في جزء الاستعلام.</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>devices</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="devices" tabindex="0" role="button">
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
<p dir="rtl">في شريط الأدوات، حدد "<strong>▷ Run</strong>" لتشغيل الاستعلام وراجع النتائج، والتي يجب أن تبدو مشابهة لهذا:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>الوقت</th>
<th>الجهاز</th>
<th>القيمة‬</th>
</tr>
</thead>
<tbody>
<tr>
<td>2022-01-01T00:00:00Z</td>
<td>Dev1</td>
<td>7</td>
</tr>
<tr>
<td>2022-01-01T00:00:01Z</td>
<td>Dev2</td>
<td>4</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
<td>...</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
<p dir="rtl">في حالة تطابق النتائج مع هذا، تكون قد نجحت في إنشاء جدول <strong>devices</strong> من البيانات الموجودة في الملف.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: استوردت في هذا المثال مقدار ضئيل للغاية من البيانات الدُفعية من ملف، ولا بأس بذلك لأغراض هذا التمرين. في الواقع، يمكنك استخدام Data Explorer لتحليل كميات أكبر بكثير من البيانات، وبما أنك قمت بتمكين استيعاب البث، يمكنك أيضاً تكوين Data Explorer لاستيعاب البيانات في الجدول من مصدر دفق مثل مراكز الأحداث.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام لغة الاستعلام Kusto للاستعلام عن الجدول في Synapse Studio</h2><a id="user-content-استخدام-لغة-الاستعلام-kusto-للاستعلام-عن-الجدول-في-synapse-studio" class="anchor" aria-label="Permalink: استخدام لغة الاستعلام Kusto للاستعلام عن الجدول في Synapse Studio" href="#استخدام-لغة-الاستعلام-kusto-للاستعلام-عن-الجدول-في-synapse-studio"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">أغلق علامة تبويب مستعرض Azure Data Explorer وارجع إلى علامة التبويب التي تحتوي على Synapse Studio.</p>
</li>
<li>
<p dir="rtl">في الصفحة <strong>Data</strong>، قم بتوسيع قاعدة بيانات <strong>iot-data</strong> ومجلد <strong>Tables</strong> الخاص بها. ثم في القائمة <strong>...</strong> للجدول <strong>devices</strong>، حدد <strong>New KQL Script</strong> &gt; <strong>Take 1000 rows</strong>.</p>
</li>
<li>
<p dir="rtl">راجع الاستعلام الذي تم إنشاؤه ونتائجه. يجب أن يحتوي الاستعلام على التعليمات البرمجية التالية:</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>devices
| <span class="pl-k">take</span> <span class="pl-c1">1000</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="devices
| take 1000" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="rtl">تحتوي نتائج الاستعلام على أول 1000 صف من البيانات.</p>
</li>
<li>
<p dir="rtl">تغيير الاستعلام كما يلي:</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>devices
| <span class="pl-k">where</span> Device == <span class="pl-s">'Dev1'</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="devices
| where Device == 'Dev1'" tabindex="0" role="button">
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
<p dir="rtl">حدد "<strong>▷ Run</strong>" لتشغيل الاستعلام. ثم راجع النتائج، التي يجب أن تحتوي فقط على صفوف الجهاز <em>Dev1</em>.</p>
</li>
<li>
<p dir="rtl">تغيير الاستعلام كما يلي:</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>devices
| <span class="pl-k">where</span> Device == <span class="pl-s">'Dev1'</span>
| <span class="pl-k">where</span> Time &gt; <span class="pl-k">datetime</span>(<span class="pl-c1">2022</span>-<span class="pl-c1">01</span>-<span class="pl-c1">07</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="devices
| where Device == 'Dev1'
| where Time > datetime(2022-01-07)" tabindex="0" role="button">
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
<p dir="rtl">شغّل الاستعلام وراجع النتائج، التي يجب أن تحتوي فقط على صفوف الجهاز <em>Dev1</em> بعد السابع من يناير 2022.</p>
</li>
<li>
<p dir="rtl">تغيير الاستعلام كما يلي:</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>devices
| <span class="pl-k">where</span> Time <span class="pl-k">between</span> (<span class="pl-k">datetime</span>(<span class="pl-c1">2022</span>-<span class="pl-c1">01</span>-<span class="pl-c1">01</span> <span class="pl-c1">00</span>:<span class="pl-c1">00</span>:<span class="pl-c1">00</span>) .. <span class="pl-k">datetime</span>(<span class="pl-c1">2022</span>-<span class="pl-c1">07</span>-<span class="pl-c1">01</span> <span class="pl-c1">23</span>:<span class="pl-c1">59</span>:<span class="pl-c1">59</span>))
| <span class="pl-k">summarize</span> AvgVal = <span class="pl-c1">avg</span>(Value) <span class="pl-k">by</span> Device
| <span class="pl-k">sort</span> <span class="pl-k">by</span> Device <span class="pl-k">asc</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="devices
| where Time between (datetime(2022-01-01 00:00:00) .. datetime(2022-07-01 23:59:59))
| summarize AvgVal = avg(Value) by Device
| sort by Device asc" tabindex="0" role="button">
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
<p dir="rtl">شغّل الاستعلام وراجع النتائج، التي يجب أن تحتوي على متوسط قيمة الجهاز المسجلة بين 1 يناير و7 يناير 2022 بترتيب تصاعدي لاسم الجهاز.</p>
</li>
<li>
<p dir="rtl">أغلق علامة التبويب استعلام KQL، مع تجاهل التغييرات.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قم بحذف موارد Azure.</h2><a id="user-content-قم-بحذف-موارد-azure" class="anchor" aria-label="Permalink: قم بحذف موارد Azure." href="#قم-بحذف-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد الانتهاء من استكشاف Azure Synapse Analytics، يجب حذف الموارد التي أنشأتها لتجنب تكاليف Azure غير الضرورية.</p>
<ol dir="rtl">
<li>
<p dir="rtl">أغلق علامة تبويب مستعرض Synapse Studio دون حفظ أية تغييرات، ثم عد إلى مدخل Azure.</p>
</li>
<li>
<p dir="rtl">في مدخل Microsoft Azure، في الصفحة ⁧<strong>الرئيسية</strong>⁩، حدّد ⁧ <strong>"Resource groups"⁦⁩⁧</strong>⁩.</p>
</li>
<li>
<p dir="rtl">حدد مجموعة الموارد لمساحة عمل Synapse Analytics (وليس مجموعة الموارد المُدارة)، وتحقق من أنها تحتوي على مساحة عمل Synapse وحساب التخزين وتجمّع Data Explorer لمساحة العمل الخاصة بك (إذا أكملت التمرين السابق، فستحتوي أيضاً على تجمّع Spark).</p>
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
