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
  <td><div dir="rtl">استكشاف Azure Stream Analytics</div></td>
  <td><div dir="rtl">Explore fundamentals of real-time analytics</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Stream Analytics</h1><a id="user-content-استكشاف-azure-stream-analytics" class="anchor" aria-label="Permalink: استكشاف Azure Stream Analytics" href="#استكشاف-azure-stream-analytics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا الإجراء، ستقوم بتوفير وظيفة Azure Stream Analytics في اشتراكك في Azure، واستخدامها لمعالجة دفق من البيانات في الوقت الفعلي.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>15</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء موارد Azure</h2><a id="user-content-إنشاء-موارد-azure" class="anchor" aria-label="Permalink: إنشاء موارد Azure" href="#إنشاء-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">سجل الدخول إلى اشتراكك في Azure في <a href="https://portal.azure.com" rel="nofollow">مدخل Microsoft Azure</a> باستخدام بيانات اعتماد اشتراك Azure.</p>
</li>
<li>
<p dir="rtl">استخدم الزر <strong>[&gt;_]</strong> الموجود على يسار شريط البحث في أعلى الصفحة لإنشاء Cloud Shell جديد في مدخل Microsoft Azure، وتحديد بيئة <em><strong>Bash</strong></em> وإنشاء مساحة تخزين إذا طلب منك ذلك. يوفر shell السحابي واجهة سطر أوامر في جزء أسفل مدخل Microsoft Azure، كما هو موضح هنا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/cloud-shell.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/cloud-shell.png" alt="مدخل Microsoft Azure مع جزء shell سحابي" style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في Azure Cloud Shell، أدخل الأمر التالي لتنزيل الملفات التي ستحتاجها لهذا التمرين.</p>
</li>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>git clone https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals dp-900</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals dp-900" tabindex="0" role="button">
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
<p dir="rtl">انتظر حتى يكتمل الأمر، ثم أدخل الأمر التالي لتغيير الدليل الحالي إلى المجلد الذي يحتوي على الملفات الخاصة بهذا التمرين.</p>
</li>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c1">cd</span> dp-900/streaming</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd dp-900/streaming" tabindex="0" role="button">
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
<p dir="rtl">أدخل الأمر التالي لتشغيل برنامج نصي يقوم بإنشاء موارد Azure التي ستحتاجها في هذا التمرين.</p>
</li>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>bash setup.sh</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="bash setup.sh" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<blockquote>
<p dir="rtl">تجاهل أي رسائل تحذير حول التغييرات المستقبلية والميزات التجريبية.</p>
</blockquote>
<p dir="rtl">انتظر ريثما يتم تشغيل البرنامج النصي وتنفيذ الإجراءات التالية:</p>
<ol dir="rtl">
<li>تثبيت ملحقات Azure CLI اللازمة لإنشاء الموارد (<em>يمكنك تجاهل أي تحذيرات حول الملحقات التجريبية</em>)</li>
<li>تحديد مجموعة موارد Azure المتوفرة لهذا التمرين.</li>
<li>إنشاء مورد <em>مركز Azure IoT</em>، والذي سيتم استخدامه لتلقي دفق بيانات من جهاز محاكاة.</li>
<li>إنشاء <em>حساب Azure Storage</em>، والذي سيتم استخدامه لتخزين البيانات المعالجة.</li>
<li>إنشاء وظيفة <em>Azure Stream Analytics</em>، والتي ستقوم بمعالجة بيانات الجهاز الواردة في الوقت الفعلي، وكتابة النتائج إلى حساب التخزين.</li>
</ol>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشاف موارد Azure</h2><a id="user-content-استكشاف-موارد-azure" class="anchor" aria-label="Permalink: استكشاف موارد Azure" href="#استكشاف-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في <a href="https://portal.azure.com?azure-portal=true" rel="nofollow">مدخل Microsoft Azure</a>، في الصفحة الرئيسية، حدد <strong>"Resource groups"</strong> لعرض مجموعات الموارد في اشتراكك. ينبغي أن يشمل مجموعة موارد<strong>learn<em>xxxxxxxxxxxxxxxxx...</em></strong> التي عرّفها برنامج الإعداد النصي.</p>
</li>
<li>
<p dir="rtl">حدد مجموعة الموارد "<strong>learn<em>xxxxxxxxxxxxxxxxx...</em></strong>"، وراجع الموارد التي تحتوي عليها، والتي ينبغي أن تشمل:</p>
<ul dir="rtl">
<li><em>مركز IoT</em> يسمى <strong>iothub<em>xxxxxxxxxxxxx</em></strong>، والذي يستخدم لتلقي بيانات الجهاز الواردة.</li>
<li><em>حساب تخزين</em> يسمى <strong>store<em>xxxxxxxxxxxx</em></strong>، الذي ستتم كتابة نتائج معالجة البيانات إليه.</li>
<li><em>وظيفة Stream Analytics</em> المسماة <em>stream</em>xxxxxxxxxxxxx***، والتي سيتم استخدامها لمعالجة بيانات الدفق.</li>
</ul>
<p dir="rtl">إذا لم يتم سرد هذه الموارد الثلاثة، فانقر فوق زر <strong>↻ Refresh</strong> حتى تظهر.</p>
</li>
<li>
<p dir="rtl">حدد وظيفة <strong>stream<em>xxxxxxxxxxxxx</em></strong> Stream Analytics، واعرض المعلومات على صفحة <strong>النظرة العامة</strong> الخاصة به، مع ملاحظة التفاصيل التالية:</p>
<ul dir="rtl">
<li>تحتوي الوظيفة على <em>إدخال</em> واحد يسمى <strong>iotinput</strong>، و<em>مخرج</em> واحد يسمى <strong>bloboutput</strong>. وتشير هذه إلى IoT Hub وحساب Storage الذي تم إنشاؤه بواسطة برنامج الإعداد النصي.</li>
<li>تحتوي الوظيفة على <em>استعلام</em>، يقرأ البيانات من إدخال <strong>iotinput</strong>، ويجمعها عن طريق حساب عدد الرسائل التي تتم معالجتها كل 10 ثوانٍ؛ وكتابة النتائج إلى إخراج <strong>bloboutput</strong>.</li>
</ul>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام الموارد لتحليل بيانات الدفق</h2><a id="user-content-استخدام-الموارد-لتحليل-بيانات-الدفق" class="anchor" aria-label="Permalink: استخدام الموارد لتحليل بيانات الدفق" href="#استخدام-الموارد-لتحليل-بيانات-الدفق"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في الجزء العلوي من صفحة <strong>نظرة عامة</strong> لوظيفة Stream Analytics، حدد زر <strong>▷ Start</strong>، ثم في جزء <strong>Start job</strong>، حدد <strong>Start</strong> لبدء المهمة.</p>
</li>
<li>
<p dir="rtl">انتظر إعلامًا بأن مهمة الدفق بدأت بنجاح.</p>
</li>
<li>
<p dir="rtl">قم بالتبديل مرة أخرى إلى Azure Cloud Shell، وأدخل الأمر التالي لمحاكاة جهاز يرسل البيانات إلى مركز IoT.</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>bash iotdevice.sh
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="bash iotdevice.sh" tabindex="0" role="button">
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
<p dir="rtl">انتظر حتى تبدأ المحاكاة، والتي ستتم الإشارة إليها من خلال إخراج مثل هذا:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>Device simulation in progress: 6%|#    | 7/120 [00:08&lt;02:21, 1.26s/it]
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="Device simulation in progress: 6%|#    | 7/120 [00:08<02:21, 1.26s/it]" tabindex="0" role="button">
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
<p dir="rtl">أثناء تشغيل المحاكاة، مرة أخرى في مدخل Azure، ارجع إلى الصفحة الخاصة بمجموعة الموارد "<strong>learn<em>xxxxxxxxxxxxxxxxx...</em></strong>"، وحدد حساب التخزين "<strong>store<em>xxxxxxxxxxxx</em></strong>".</p>
</li>
<li>
<p dir="rtl">في الجزء الموجود على يسار جزء حساب التخزين، حدد علامة تبويب <strong>"Containers"</strong>.</p>
</li>
<li>
<p dir="rtl">افتح حاوية <strong>البيانات</strong>.</p>
</li>
<li>
<p dir="rtl">في حاوية <strong>البيانات</strong>، انتقل عبر التسلسل الهيكلي للمجلدات، والذي يتضمن مجلدًا للسنة الحالية، مع مجلدات فرعية للشهر واليوم والساعة.</p>
</li>
<li>
<p dir="rtl">في المجلد للساعة، لاحظ الملف الذي تم إنشاؤه، الذي يجب أن يكون له اسم مشابه للاسم <strong>0_xxxxxxxxxxxxxxxx.json</strong>.</p>
</li>
<li>
<p dir="rtl">في القائمة <strong>...</strong> للملف (على يمين تفاصيل الملف)، حدد <strong>View/edit</strong>، وراجع محتويات الملف؛ التي يجب أن تتكون من سجل JSON لكل 10 ثوانٍ، مع إظهار عدد الرسائل المستلمة من أجهزة إنترنت الأشياء، مثل هذا:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>{"starttime":"2021-10-23T01:02:13.2221657Z","endtime":"2021-10-23T01:02:23.2221657Z","device":"iotdevice","messages":2}
{"starttime":"2021-10-23T01:02:14.5366678Z","endtime":"2021-10-23T01:02:24.5366678Z","device":"iotdevice","messages":3}
{"starttime":"2021-10-23T01:02:15.7413754Z","endtime":"2021-10-23T01:02:25.7413754Z","device":"iotdevice","messages":4}
...
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="{&quot;starttime&quot;:&quot;2021-10-23T01:02:13.2221657Z&quot;,&quot;endtime&quot;:&quot;2021-10-23T01:02:23.2221657Z&quot;,&quot;device&quot;:&quot;iotdevice&quot;,&quot;messages&quot;:2}
{&quot;starttime&quot;:&quot;2021-10-23T01:02:14.5366678Z&quot;,&quot;endtime&quot;:&quot;2021-10-23T01:02:24.5366678Z&quot;,&quot;device&quot;:&quot;iotdevice&quot;,&quot;messages&quot;:3}
{&quot;starttime&quot;:&quot;2021-10-23T01:02:15.7413754Z&quot;,&quot;endtime&quot;:&quot;2021-10-23T01:02:25.7413754Z&quot;,&quot;device&quot;:&quot;iotdevice&quot;,&quot;messages&quot;:4}
..." tabindex="0" role="button">
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
<p dir="rtl">استخدم زر <strong>↻ Refresh</strong> لتحديث الملف، مع ملاحظة أنه تتم كتابة نتائج إضافية إلى الملف، حيث تقوم وظيفة Stream Analytics بمعالجة بيانات الجهاز في الوقت الحقيقي حيث يتم دفقها من الجهاز إلى مركز إنترنت الأشياء.</p>
</li>
<li>
<p dir="rtl">ارجع إلى Azure Cloud Shell، وانتظر حتى تنتهي محاكاة الجهاز (يجب أن تعمل لمدة 3 دقائق تقريبًا).</p>
</li>
<li>
<p dir="rtl">مرة أخرى في مدخل Azure، قم بتحديث الملف مرة أخرى لمشاهدة المجموعة الكاملة من النتائج التي تم إنتاجها أثناء المحاكاة.</p>
</li>
<li>
<p dir="rtl">ارجع إلى مجموعة الموارد "<strong>learn<em>xxxxxxxxxxxxxxxxx...</em></strong> "، وأعد فتح مهمة Stream Analytics "<strong>stream<em>xxxxxxxxxxxxx</em></strong>".</p>
</li>
<li>
<p dir="rtl">في أعلى صفحة وظيفة Stream Analytics، استخدم زر ** إيقاف⬜** لإيقاف المهمة، مع التأكيد عند المطالبة بذلك.</p>
</li>
</ol>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: احذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف حل الدفق.</p>
</blockquote>
</article></div>
