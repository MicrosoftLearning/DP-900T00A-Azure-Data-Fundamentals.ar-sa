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
  <td><div dir="rtl">استكشاف أساسيات تصور البيانات باستخدام Power BI</div></td>
  <td><div dir="rtl">Explore fundamentals of data visualization</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف أساسيات تصور البيانات باستخدام Power BI</h1><a id="user-content-استكشاف-أساسيات-تصور-البيانات-باستخدام-power-bi" class="anchor" aria-label="Permalink: استكشاف أساسيات تصور البيانات باستخدام Power BI" href="#استكشاف-أساسيات-تصور-البيانات-باستخدام-power-bi"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، ستستخدم Microsoft Power BI Desktop لإنشاء نموذج بيانات وتقرير يحتوي على مرئيات بيانات تفاعلية.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>20</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">‏‏تثبيت Power BI Desktop</h2><a id="user-content-تثبيت-power-bi-desktop" class="anchor" aria-label="Permalink: ‏‏تثبيت Power BI Desktop" href="#تثبيت-power-bi-desktop"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">إذا لم يكن Microsoft Power BI Desktop مثبتاً بالفعل على جهاز الكمبيوتر الذي يعمل بنظام Windows، يمكنك تنزيله وتثبيته مجاناً.</p>
<ol dir="rtl">
<li>تنزيل مثبّت Power BI Desktop من <a href="https://aka.ms/power-bi-desktop?azure-portal=true" rel="nofollow">https://aka.ms/power-bi-desktop</a>.</li>
<li>عند تنزيل الملف، افتحه واستخدم معالج الإعداد لتثبيت Power BI Desktop على جهاز الكمبيوتر. قد يستغرق هذا التثبيت بضع دقائق.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استيراد البيانات</h2><a id="user-content-استيراد-البيانات" class="anchor" aria-label="Permalink: استيراد البيانات" href="#استيراد-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">افتح Power BI Desktop. يجب أن تبدو واجهة التطبيق مشابهة لما يلي:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/power-bi-start.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/power-bi-start.png" alt="لقطة شاشة تعرض شاشة بدء Power BI Desktop." style="max-width: 100%;"></a></p>
<p dir="rtl">أنت الآن جاهز لاستيراد البيانات للتقرير الخاص بك.</p>
</li>
<li>
<p dir="rtl">في شاشة الترحيب في Power BI Desktop، حدد <strong>Get data</strong>، ثم في قائمة مصادر البيانات، حدد <strong>Web</strong> ثم حدد <strong>Connect</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/web-source.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/web-source.png" alt="لقطة شاشة توضح كيفية تحديد مصدر بيانات الويب في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في مربع الحوار <strong>From web</strong>، أدخل عنوان URL التالي ثم حدد <strong>OK</strong>:</p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/power-bi/customers.csv
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/power-bi/customers.csv" tabindex="0" role="button">
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
<p dir="rtl">في مربع الحوار "Access Web content"، حدد "<strong>Connect</strong>".</p>
</li>
<li>
<p dir="rtl">تحقق من أن عنوان URL يفتح مجموعة بيانات تحتوي على بيانات العميل، كما هو موضح أدناه. ثم حدد <strong>Load</strong> لتحميل البيانات في نموذج البيانات للتقرير الخاص بك.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/customers.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/customers.png" alt="لقطة شاشة تعرض مجموعة بيانات لبيانات العملاء المعروضة في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في نافذة Power BI Desktop الرئيسية، في قائمة "Data" حدد "<strong>Get data</strong>" ثم حدد "<strong>Web</strong>":</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/get-data.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/get-data.png" alt="لقطة شاشة تعرض قائمة &quot;Get data&quot; في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في مربع الحوار <strong>From web</strong>، أدخل عنوان URL التالي ثم حدد <strong>OK</strong>:</p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/power-bi/products.csv
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/power-bi/products.csv" tabindex="0" role="button">
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
<p dir="rtl">في مربع الحوار، حدد "<strong>Load</strong>" لتحميل بيانات المنتج الموجودة بهذا الملف إلى نموذج البيانات.</p>
</li>
<li>
<p dir="rtl">كرر الخطوات الثلاث السابقة لاستيراد مجموعة بيانات ثالثة تحتوي على بيانات الطلب من عنوان URL التالي:</p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/power-bi/orders.csv
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/raw/master/power-bi/orders.csv" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشاف نموذج بيانات</h2><a id="user-content-استكشاف-نموذج-بيانات" class="anchor" aria-label="Permalink: استكشاف نموذج بيانات" href="#استكشاف-نموذج-بيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تم تحميل جداول البيانات الثلاثة التي قمت باستيرادها في نموذج بيانات، والذي ستقوم الآن باستكشافه وتحسينه.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في Power BI Desktop، في الجزء الأيسر، حدد علامة التبويب "<strong>Model</strong>"، ثم رتب الجداول في النموذج بحيث يمكنك رؤيتها. يمكنك إخفاء الأجزاء على الجانب الأيمن باستخدام الرمز <strong>&gt;&gt;</strong>:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/model-tab.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/model-tab.png" alt="لقطة شاشة تعرض علامة التبويب &quot;Model&quot; في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في جدول <strong>orders</strong>، حدد حقل <strong>Revenue</strong> ثم في جزء <strong>Properties</strong>، قم بتعيين خاصية <strong>Format</strong> الخاصة به إلى <strong>Currency</strong>:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/revenue-currency.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/revenue-currency.png" alt="لقطة شاشة توضح كيفية تعيين تنسيق &quot;Revenue&quot; إلى &quot;Currency&quot; في Power BI." style="max-width: 100%;"></a></p>
<p dir="rtl">ستضمن هذه الخطوة عرض قيم الإيرادات كعملة في تصورات التقرير.</p>
</li>
<li>
<p dir="rtl">في جدول "products"، انقر بزر الماوس الأيمن فوق حقل "<strong>Category</strong>" (أو افتح القائمة <strong>⋮</strong>) وحدد "<strong>Create hierarchy</strong>". تُنشئ هذه الخطوة تسلسلاً هرمياً يسمى "<strong>Category Hierarchy</strong>". قد تحتاج إلى توسيع جدول "<strong>products</strong>" أو التمرير لأسفل لمشاهدة ذلك - يمكنك أيضاً رؤيته في جزء "<strong>Fields</strong>":</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/category-hierarchy.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/category-hierarchy.png" alt="لقطة شاشة توضح كيفية إضافة &quot;Category Hierarchy&quot; في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في جدول "products"، انقر بزر الماوس الأيمن فوق الحقل "<strong>ProductName</strong>" (أو افتح القائمة <strong>⋮</strong>) وحدد "<strong>Add to hierarchy</strong> &gt; <strong>Category Hierarchy</strong>". يؤدي هذا إلى إضافة حقل <strong>ProductName</strong> إلى التسلسل الهرمي الذي قمت بإنشائه مسبقاً.</p>
</li>
<li>
<p dir="rtl">في جزء <strong>Fields</strong>، انقر بزر الماوس الأيمن فوق <strong>Category Hierarchy</strong> (أو افتح القائمة <strong>...</strong>) وحدد <strong>Rename</strong>. ثم أعد تسمية التسلسل الهرمي إلى <strong>Categorized Product</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/rename-hierarchy.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/rename-hierarchy.png" alt="لقطة شاشة توضح كيفية إعادة تسمية التسلسل الهرمي في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">على الحافة اليمنى، حدد <strong>علامة التبويب طريقة عرض</strong> الجدول، ثم في <strong>جزء البيانات</strong> ، حدد <strong>جدول العملاء</strong> .</p>
</li>
<li>
<p dir="rtl">حدد رأس العمود <strong>City</strong>، ثم عيّن الخاصية <strong>Data Category</strong> إلى <strong>City</strong>:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/data-category.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/data-category.png" alt="لقطة شاشة توضح كيفية تعيين &quot;data category&quot; في Power BI." style="max-width: 100%;"></a></p>
<p dir="rtl">ستضمن هذه الخطوة تفسير القيم الموجودة في هذا العمود على أنها أسماء مدن، ما قد يكون مفيداً إذا كنت تنوي تضمين تصورات المخطط.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء تقرير</h2><a id="user-content-إنشاء-تقرير" class="anchor" aria-label="Permalink: إنشاء تقرير" href="#إنشاء-تقرير"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">أنت الآن جاهز تقريباً لإنشاء تقرير. عليك أولاً التحقق من بعض الإعدادات للتأكد من تمكين جميع التصورات.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في القائمة <strong>File</strong>، حدد <strong>Options and Settings</strong>. ثم حدد <strong>Options</strong>، وفي قسم <strong>Security</strong>، تأكد من تمكين ** استخدام تصورات المخطط والمخطط المعبأ ** وحدد <strong>OK</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/set-options.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/set-options.png" alt="لقطة شاشة توضح كيفية تعيين خاصية &quot;Use Map and Filled Map visuals&quot; في PowerBI." style="max-width: 100%;"></a></p>
<p dir="rtl">تضمن هذه الخطوة إمكانية تضمين تصورات المخطط في التقارير.</p>
</li>
<li>
<p dir="rtl">على الحافة اليسرى، حدد علامة التبويب <strong>عرض التقرير</strong> واعرض واجهة تصميم التقرير.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/report-tab.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/report-tab.png" alt="لقطة شاشة تعرض علامة التبويب &quot;report&quot; في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في الشريط، أعلى سطح تصميم التقرير، حدد <strong>Text Box</strong> وأضف مربع نص يحتوي على النص <strong>Sales Report</strong> إلى التقرير. قم بتنسيق النص لجعله غامقاً بحجم خط 32.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/text-box.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/text-box.png" alt="لقطة شاشة توضح كيفية إضافة مربع نص في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">حدد أي منطقة فارغة في التقرير لإلغاء تحديد مربع النص. ثم في جزء <strong>البيانات</strong>، قم بتوسيع <strong>المنتجات</strong> وحدد حقل <strong>المنتجات المقسمة لفئات</strong>. تضيف هذه الخطوة جدولاً إلى التقرير.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/categorized-products-table.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/categorized-products-table.png" alt="لقطة شاشة توضح كيفية إضافة جدول &quot;categorized products&quot; إلى تقرير في Power BI." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">مع استمرار تحديد الجدول، في جزء <strong>البيانات</strong> قم بتوسيع <strong>الطلبات</strong> وحدد <strong>الإيرادات</strong>. يُضاف عمود "Revenue" إلى الجدول. قد تحتاج إلى توسيع حجم الجدول لرؤيته.</p>
<p dir="rtl">الإيرادات منسقة كعملة، كما حددت في النموذج. ومع ذلك، فإنك لم تحدد عدد المنازل العشرية، لذا فإن القيم تتضمن مقادير كسرية. لا يهم التصورات التي ستنشئها، حيث يمكنك الرجوع إلى علامة التبويب "<strong>Model</strong>" أو "<strong>Data</strong>" وتغيير المنازل العشرية إن أردت.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/revenue-column.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/revenue-column.png" alt="لقطة شاشة تعرض جدول &quot;categorized products&quot; مع عمود &quot;Revenue&quot; في التقرير." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">مع استمرار تحديد الجدول، في جزء <strong>Visualizations</strong>، حدد التصور <strong>المخطط البياني العمودي المكدس</strong>. تم تغيير الجدول إلى مخطط عمودي يعرض الإيرادات حسب الفئة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/stacked-column-chart.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/stacked-column-chart.png" alt="لقطة شاشة تعرض مخطط أعمدة مرصوفة لجدول &quot;categorized products&quot; مع عمود &quot;Revenue&quot; في التقرير." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">فوق المخطط البياني العمودي المحدد، حدد الرمز <strong>↓</strong> لتشغيل التنقل لأسفل. ثم في المخطط البياني، حدد العمود الثاني للتنقل ومعرفة إيرادات المنتجات الفردية في هذه الفئة. هذه الإمكانية ممكنة لأنك حددت تسلسلاً هرمياً للفئات والمنتجات.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/drill-down.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/drill-down.png" alt="لقطة شاشة تعرض مخطط بياني عمودي يمكن التنقل لأسفل به لرؤية المنتجات داخل الفئة." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">استخدم الرمز <strong>↑</strong> للعودة إلى مستوى الفئة. ثم حدد الرمز <strong>(</strong>↓<strong>)</strong> لإيقاف تشغيل ميزة التنقل لأسفل.</p>
</li>
<li>
<p dir="rtl">حدد منطقة فارغة من التقرير، ثم في جزء <strong>البيانات</strong>، حدد حقل <strong>الكمية</strong> في جدول <strong>الطلبات</strong> و<strong>الفئة</strong> في جدول <strong>المنتجات</strong>. ينتج عن هذه الخطوة مخطط بياني عمودي آخر يوضح حجم المبيعات حسب فئة المنتج.</p>
</li>
<li>
<p dir="rtl">مع تحديد مخطط العمود الجديد، في جزء <strong>Visualizations</strong>، حدد <strong>Pie chart</strong> ثم غيّر حجم المخطط البياني وضعه بجوار المخطط البياني لعمود الإيرادات حسب الفئة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/category-pie-chart.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/category-pie-chart.png" alt="لقطة شاشة تعرض مخططاً دائرياً يعرض حجم المبيعات حسب الفئة." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">حدد منطقة فارغة من التقرير، ثم في جزء <strong>البيانات</strong>، حدد حقل <strong>المدينة</strong> في جدول <strong>العملاء</strong> ثم حدد <strong>الإيرادات</strong> في جدول <strong>الأوامر</strong>. ما ينتج عنه خريطة توضح إيرادات المبيعات حسب المدينة. أعد ترتيب المرئيات وغيّر حجمها حسب الحاجة:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/revenue-map.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/revenue-map.png" alt="لقطة شاشة تعرض خريطة توضح الإيرادات حسب المدينة." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في المخطط، لاحظ أنه يمكنك السحب أو النقر المزدوج أو استخدام عجلة الماوس أو الضغط والسحب على شاشة اللمس للتفاعل. ثم حدد مدينة معينة، ولاحظ أنه تم تعديل التصورات الأخرى في التقرير لتمييز البيانات الخاصة بالمدينة المحددة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/selected-data.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/selected-data.png" alt="لقطة شاشة تعرض خريطة توضح الإيرادات حسب المدينة مع تمييز بيانات المدينة المحددة." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في القائمة <strong>ملف</strong>، حدد <strong>حفظ</strong>. ثم احفظ الملف باسم ملف .pbix مناسب. يمكنك فتح الملف واستكشاف نمذجة البيانات والتصور بشكل أكبر في وقت فراغك.</p>
</li>
</ol>
<p dir="rtl">إذا كان لديك اشتراك في <a href="https://www.powerbi.com/?azure-portal=true" rel="nofollow">خدمة Power BI</a>، يمكنك تسجيل الدخول إلى حسابك ونشر التقرير إلى مساحة عمل Power BI.</p>
</article></div>
