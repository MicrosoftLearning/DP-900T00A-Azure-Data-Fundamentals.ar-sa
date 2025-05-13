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
  <td><div dir="rtl">استكشاف التحليلات في الوقت الحقيقي في Microsoft Fabric</div></td>
  <td><div dir="rtl">Explore real-time analytics in Microsoft Fabric</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف التحليلات في الوقت الحقيقي في Microsoft Fabric</h1><a id="user-content-استكشاف-التحليلات-في-الوقت-الحقيقي-في-microsoft-fabric" class="anchor" aria-label="Permalink: استكشاف التحليلات في الوقت الحقيقي في Microsoft Fabric" href="#استكشاف-التحليلات-في-الوقت-الحقيقي-في-microsoft-fabric"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يوفر Microsoft Fabric التحليل الذكي في الوقت الحقيقي، ما يتيح لك إنشاء حلول تحليلية لتدفقات البيانات في الوقت الحقيقي. في هذا التمرين، ستستخدم قدرات التحليل الذكي في الوقت الحقيقي في Microsoft Fabric لاستيعاب وتحليل وتصور دفق البيانات في الوقت الحقيقي من شركة سيارات الأجرة.</p>
<p dir="rtl">يستغرق هذا التمرين المعملي حوالي <strong>30</strong> دقيقة لإكماله.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: تحتاج إلى مستأجر <a href="https://learn.microsoft.com/fabric/get-started/fabric-trial" rel="nofollow"> Microsoft Fabric لإكمال هذا </a>التمرين.</p>
</blockquote>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء مساحة عمل</h2><a id="user-content-إنشاء-مساحة-عمل" class="anchor" aria-label="Permalink: إنشاء مساحة عمل" href="#إنشاء-مساحة-عمل"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">قبل العمل مع البيانات في Fabric، تحتاج إلى إنشاء مساحة عمل مع تمكين سعة Fabric.</p>
<ol dir="rtl">
<li>
<p dir="rtl">انتقل إلى الصفحة<a href="https://app.fabric.microsoft.com/home?experience=fabric" rel="nofollow"> الرئيسية ل Microsoft Fabric</a> في <code>https://app.fabric.microsoft.com/home?experience=fabric</code> مستعرض، وسجل الدخول باستخدام بيانات اعتماد Fabric.</p>
</li>
<li>
<p dir="rtl">في شريط القوائم على اليسار، حدد <strong>مساحات العمل</strong> (تبدو الأيقونة مشابهة لـ ).</p>
</li>
<li>
<p dir="rtl">إنشاء مساحة عمل جديدة باسم من اختيارك، وتحديد وضع ترخيص يتضمن سعة Fabric (<em>الإصدار التجريبي</em> أو <em>Premium</em> أو <em>Fabric</em>).</p>
</li>
<li>
<p dir="rtl">عند فتح مساحة العمل الجديدة، يجب أن تكون فارغة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-workspace.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-workspace.png" alt="لقطة شاشة لمساحة عمل فارغة في Fabric." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء تدفق أحداث</h2><a id="user-content-إنشاء-تدفق-أحداث" class="anchor" aria-label="Permalink: إنشاء تدفق أحداث" href="#إنشاء-تدفق-أحداث"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">أنت الآن جاهز للعثور على البيانات في الوقت الحقيقي واستيعابها من مصدر دفق. للقيام بذلك، ستبدأ في Fabric Real-Time Hub.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: في المرة الأولى التي تستخدم فيها مركز الوقت الحقيقي، قد يتم عرض بعض <em>تلميحات بدء الاستخدام</em> . يمكنك إغلاق هذه.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">في شريط القوائم على اليسار، حدد <strong>مركز الوقت</strong> الحقيقي.</p>
<p dir="rtl">يوفر المركز في الوقت الحقيقي طريقة سهلة للعثور على مصادر البيانات المتدفقة وإدارتها.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/real-time-hub.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/real-time-hub.png" alt="لقطة شاشة لمركز في الوقت الحقيقي في Fabric." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في لوحة الوصل في الوقت الحقيقي، في <strong>قسم الاتصال ب</strong> ، حدد <strong>مصادر</strong> البيانات.</p>
</li>
<li>
<p dir="rtl">ابحث عن <strong>مصدر بيانات نموذج سيارة أجرة</strong> صفراء وحدد <strong>Connect</strong>. ثم في <strong>معالج الاتصال</strong> ، قم بتسمية المصدر <code>taxi</code> وتحرير اسم eventstream الافتراضي لتغييره إلى <code>taxi-data</code>. سيسمى الدفق الافتراضي المقترن بهذه البيانات تلقائيا باسم <em>taxi-data-stream</em>:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/name-eventstream.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/name-eventstream.png" alt="لقطة شاشة لمصدر أحداث جديد." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">حدد <strong>Next</strong> وانتظر حتى يتم إنشاء المصدر و eventstream، ثم حدد <strong>Open eventstream</strong>. سيعرض eventstream مصدر سيارة الأجرة **** <strong>وتيار</strong> بيانات سيارة الأجرة على لوحة التصميم:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-taxi-stream.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-taxi-stream.png" alt="لقطة شاشة للوحة eventstream." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء مركز أحداث</h2><a id="user-content-إنشاء-مركز-أحداث" class="anchor" aria-label="Permalink: إنشاء مركز أحداث" href="#إنشاء-مركز-أحداث"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ي استيعاب eventstream لبيانات الأسهم في الوقت الحقيقي، ولكنه لا يفعل أي شيء معها حاليا. دعونا ننشئ مركز أحداث حيث يمكننا تخزين البيانات الملتقطة في جدول.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في شريط القوائم على اليسار، حدد <strong>Create</strong>. في <em>صفحة New</em> ، ضمن <em>قسم Real-Time Inteligence</em> ، حدد <strong>Eventhouse</strong>. أعطه اسما فريدا من اختيارك.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا <strong>لم يكن الخيار إنشاء</strong> مثبتا على الشريط الجانبي، فستحتاج إلى تحديد خيار علامة الحذف (<strong>...</strong>) أولا.</p>
</blockquote>
<p dir="rtl">أغلق أي تلميحات أو مطالبات يتم عرضها حتى ترى eventhouse الجديدة الفارغة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/create-eventhouse.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/create-eventhouse.png" alt="لقطة شاشة لحدث جديد" style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في الجزء على اليسار، لاحظ أن eventhouse يحتوي على قاعدة بيانات KQL بنفس اسم eventhouse. يمكنك إنشاء جداول لبياناتك في الوقت الحقيقي في قاعدة البيانات هذه، أو إنشاء قواعد بيانات إضافية حسب الضرورة.</p>
</li>
<li>
<p dir="rtl">حدد قاعدة البيانات، ولاحظ أن هناك مجموعة* استعلام مقترنة*. يحتوي هذا الملف على بعض نماذج استعلامات KQL التي يمكنك استخدامها لبدء الاستعلام عن الجداول في قاعدة البيانات الخاصة بك.</p>
<p dir="rtl">ومع ذلك، لا توجد حاليا جداول للاستعلام. دعونا نحل هذه المشكلة عن طريق الحصول على البيانات من eventstream إلى جدول جديد.</p>
</li>
<li>
<p dir="rtl">في الصفحة الرئيسية لقاعدة بيانات KQL، حدد <strong>Get data</strong>.</p>
</li>
<li>
<p dir="rtl">بالنسبة لمصدر البيانات، حدد <strong>Eventstream</strong> &gt; <strong>Existing eventstream</strong>.</p>
</li>
<li>
<p dir="rtl">في <strong>جزء تحديد جدول</strong> وجهة أو إنشائه، أنشئ جدولا جديدا باسم <code>taxi</code>. ثم في <strong>جزء تكوين مصدر</strong> البيانات، حدد مساحة العمل الخاصة بك و <strong>eventstream بيانات</strong> سيارة الأجرة وقم بتسمية الاتصال <code>taxi-table</code>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/configure-destination.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/configure-destination.png" alt="لقطة شاشة لتكوين تحميل جدول من eventstream." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl"><strong>استخدم الزر التالي</strong> لإكمال الخطوات لفحص البيانات ثم إنهاء التكوين. ثم أغلق نافذة التكوين لمشاهدة eventhouse الخاص بك مع جدول الأسهم.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/eventhouse-with-table.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/eventhouse-with-table.png" alt="لقطة شاشة ل و eventhouse مع جدول." style="max-width: 100%;"></a></p>
<p dir="rtl">تم إنشاء الاتصال بين الدفق والجدول. لنتحقق من ذلك في eventstream.</p>
</li>
<li>
<p dir="rtl">في شريط القوائم على اليسار، حدد <strong>مركز الوقت</strong> الحقيقي ثم اعرض <strong>صفحة تدفقات</strong> البيانات الخاصة بي. في القائمة ...** لدفق** <strong>تدفق بيانات سيارة الأجرة، حدد Open eventstream.</strong></p>
<p dir="rtl">يعرض eventstream الآن وجهة للتدفق:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/eventstream-destination.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/eventstream-destination.png" alt="لقطة شاشة ل eventstream مع وجهة." style="max-width: 100%;"></a></p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: حدد الوجهة على لوحة التصميم، وإذا لم يتم عرض أي معاينة للبيانات أسفلها، فحدد <strong>تحديث</strong>.</p>
</blockquote>
<p dir="rtl">في هذا التمرين، قمت بإنشاء eventstream بسيط جدا يلتقط البيانات في الوقت الحقيقي ويحملها في جدول. في حل حقيقي، عادة ما تضيف تحويلات لتجميع البيانات عبر النوافذ الزمنية (على سبيل المثال، لتسجيل متوسط سعر كل سهم على مدى خمس دقائق).</p>
<p dir="rtl">الآن دعونا نستكشف كيف يمكنك الاستعلام عن البيانات الملتقطة وتحليلها.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعلام عن البيانات الملتقطة</h2><a id="user-content-الاستعلام-عن-البيانات-الملتقطة" class="anchor" aria-label="Permalink: الاستعلام عن البيانات الملتقطة" href="#الاستعلام-عن-البيانات-الملتقطة"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يلتقط eventstream بيانات أجرة سيارات الأجرة في الوقت الحقيقي ويحملها في جدول في قاعدة بيانات KQL. يمكنك الاستعلام عن هذا الجدول لمشاهدة البيانات الملتقطة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في شريط القوائم على اليسار، حدد قاعدة بيانات eventhouse.</p>
</li>
<li>
<p dir="rtl"><em>حدد مجموعة</em> الاستعلام لقاعدة البيانات الخاصة بك.</p>
</li>
<li>
<p dir="rtl">في جزء الاستعلام، قم بتعديل استعلام المثال الأول كما هو موضح هنا:</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>taxi
| <span class="pl-k">take</span> <span class="pl-c1">100</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="taxi
| take 100" tabindex="0" role="button">
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
<p dir="rtl">حدد رمز الاستعلام وقم بتشغيله لمشاهدة 100 صف من البيانات من الجدول.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/kql-stock-query.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/kql-stock-query.png" alt="لقطة شاشة لاستعلام KQL." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">راجع النتائج، ثم قم بتعديل الاستعلام لإظهار عدد سيارات الأجرة لكل ساعة:</p>
</li>
<div class="highlight highlight-source-kusto notranslate position-relative overflow-auto" dir="auto"><pre>taxi
| <span class="pl-k">summarize</span> PickupCount = <span class="pl-c1">count</span>() <span class="pl-k">by</span> <span class="pl-c1">bin</span>(<span class="pl-c1">todatetime</span>(tpep_pickup_datetime), <span class="pl-c1">1</span><span class="pl-c1">h</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="taxi
| summarize PickupCount = count() by bin(todatetime(tpep_pickup_datetime), 1h)" tabindex="0" role="button">
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
<p dir="rtl">قم بتمييز الاستعلام المعدل وتشغيله لمشاهدة النتائج.</p>
</li>
<li>
<p dir="rtl">انتظر بضع ثوان ثم قم بتشغيله مرة أخرى، مع ملاحظة أن عدد عمليات الاستلام يتغير مع إضافة بيانات جديدة إلى الجدول من الدفق في الوقت الفعلي.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف الموارد</h2><a id="user-content-تنظيف-الموارد" class="anchor" aria-label="Permalink: تنظيف الموارد" href="#تنظيف-الموارد"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، قمت بإنشاء مركز أحداث، واستيعاب البيانات في الوقت الحقيقي باستخدام eventstream، والاستعلام عن البيانات التي تم استيعابها في جدول قاعدة بيانات KQL، وإنشاء لوحة معلومات في الوقت الحقيقي لتصور البيانات في الوقت الفعلي، وتكوين تنبيه باستخدام المنشط.</p>
<p dir="rtl">إذا انتهيت من استكشاف التحليل الذكي في الوقت الحقيقي في Fabric، يمكنك حذف مساحة العمل التي أنشأتها لهذا التمرين.</p>
<ol dir="rtl">
<li>في الشريط على اليسار، حدد أيقونة مساحة العمل الخاصة بك.</li>
<li>في شريط الأدوات، حدد <strong>إعدادات</strong> مساحة العمل.</li>
<li>في <strong>القسم عام</strong> ، حدد <strong>إزالة مساحة</strong> العمل هذه.</li>
</ol>
</article></div>
