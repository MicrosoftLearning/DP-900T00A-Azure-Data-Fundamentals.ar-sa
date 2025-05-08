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
  <td><div dir="rtl">استكشاف Spark Streaming في Azure Synapse Analytics</div></td>
  <td><div dir="rtl">Explore fundamentals of real-time analytics</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف Spark Streaming في Azure Synapse Analytics</h1><a id="user-content-استكشاف-spark-streaming-في-azure-synapse-analytics" class="anchor" aria-label="Permalink: استكشاف Spark Streaming في Azure Synapse Analytics" href="#استكشاف-spark-streaming-في-azure-synapse-analytics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، ستستخدم <em>Spark Structured Streaming</em> و<em>جداول دلتا</em> في Azure Synapse Analytics لمعالجة بيانات الدفق.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>15</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير مساحة عمل Synapse Analytics</h2><a id="user-content-توفير-مساحة-عمل-synapse-analytics" class="anchor" aria-label="Permalink: توفير مساحة عمل Synapse Analytics" href="#توفير-مساحة-عمل-synapse-analytics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لاستخدام Synapse Analytics، يجب توفير مورد مساحة عمل Synapse Analytics في اشتراك Azure.</p>
<ol dir="rtl">
<li>
<p dir="rtl">افتح مدخل Azure على <a href="https://portal.azure.com?azure-portal=true" rel="nofollow">مدخل Azure</a>، وقم بتسجيل الدخول باستخدام بيانات الاعتماد المقترنة باشتراك Azure الخاص بك.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: تأكد من أنك تعمل في الدليل الذي يحتوي على اشتراكك - المُشار إليه في أعلى اليمين أسفل معرف المستخدم. إذا لم تكن كذلك، حدد رمز المستخدم وبدّل الدليل.</p>
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
<p dir="rtl">على الجانب الأيسر من Synapse Studio، استخدم الرمز <strong>››</strong> لتوسيع القائمة - وهذا يكشف عن الصفحات المختلفة داخل Synapse Studio التي ستستخدمها لإدارة الموارد وتنفيذ مهام تحليل البيانات، كما هو موضح هنا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/synapse-studio.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/synapse-studio.png" alt="Synapse Studio" style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء تجمع Spark</h2><a id="user-content-إنشاء-تجمع-spark" class="anchor" aria-label="Permalink: إنشاء تجمع Spark" href="#إنشاء-تجمع-spark"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لاستخدام Spark لمعالجة بيانات الدفق، تحتاج إلى إضافة تجمع Spark إلى مساحة عمل Azure Synapse.</p>
<ol dir="rtl">
<li>في استوديو Synapse، حدد صفحة <strong>"Manage"</strong>.</li>
<li>حدد علامة التبويب <strong>"Apache Spark pools"</strong> ثم استخدم رمز <strong>&amp;#65291، جديد</strong> لإنشاء تجمّع Spark جديد بالإعدادات التالية:
<ul dir="rtl">
<li><strong>اسم تجمع Apache Spark</strong>: sparkpool</li>
<li><strong>حجم عقدة المجموعة</strong>: الذاكرة محسنة</li>
<li><strong>حجم العقدة</strong>: صغير (4 vCores / 32 GB)</li>
<li><strong>تحجيم تلقائي</strong>: ُممكّن</li>
<li><strong>عدد العقد</strong> 3----3</li>
</ul>
</li>
<li>راجع وأنشئ تجمع Spark ثم انتظر حتى يتم نشره (الأمر الذي قد يستغرق بضع دقائق).</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشاف معالجة الدفق</h2><a id="user-content-استكشاف-معالجة-الدفق" class="anchor" aria-label="Permalink: استكشاف معالجة الدفق" href="#استكشاف-معالجة-الدفق"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لاستكشاف معالجة الدفق باستخدام Spark، ستستخدم دفتر ملاحظات يحتوي على تعليمات برمجية وملاحظات Python لمساعدتك في تنفيذ بعض معالجات الدفق الأساسية باستخدام جداول دلتا وSpark Structured Streaming.</p>
<ol dir="rtl">
<li>قم بتنزيل دفتر ملاحظات <a href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/streaming/Spark%20Structured%20Streaming%20and%20Delta%20Tables.ipynb">Structured Streaming and Delta Tables.ipynb</a> على الكمبيوتر المحلي (إذا تم فتح دفتر الملاحظات كملف نصي في المستعرض، فاحفظه في مجلد محلي؛ مع الحرص على حفظه كـ <strong>Structured Streaming and Delta Tables.ipynb</strong>، وليس كملف ‎.txt)</li>
<li>في استوديو Synapse، حدد صفحة <strong>Manage</strong>.</li>
<li>في القائمة <strong>＋</strong>، حدد <strong>↤ Import</strong>، وحدد ملف <strong>Structured Streaming and Delta Tables.ipynb</strong> على الكمبيوتر المحلي.</li>
<li>اتبع الإرشادات الموجودة في دفتر الملاحظات لإرفاقها بتجمع Spark وتشغيل خلايا التعليمات البرمجية التي تحتوي عليها لاستكشاف طرق مختلفة لاستخدام Spark لمعالجة الدفق.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قم بحذف موارد Azure.</h2><a id="user-content-قم-بحذف-موارد-azure" class="anchor" aria-label="Permalink: قم بحذف موارد Azure." href="#قم-بحذف-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: يمكنك تخطي هذا القسم إذا كنت تنوي إكمال تمارين أخرى تستخدم Azure Synapse Analytics. وإلا، اتبع الخطوات أدناه لتجنب تكاليف Azure غير الضرورية.</p>
</blockquote>
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
