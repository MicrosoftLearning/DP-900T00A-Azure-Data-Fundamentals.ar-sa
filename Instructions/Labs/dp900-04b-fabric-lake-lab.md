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
  <td><div dir="rtl">استكشاف تحليلات البيانات في Microsoft Fabric</div></td>
  <td><div dir="rtl">Explore fundamentals of large-scale data analytics</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف تحليلات البيانات في Microsoft Fabric</h1><a id="user-content-استكشاف-تحليلات-البيانات-في-microsoft-fabric" class="anchor" aria-label="Permalink: استكشاف تحليلات البيانات في Microsoft Fabric" href="#استكشاف-تحليلات-البيانات-في-microsoft-fabric"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، ستستكشف استيعاب البيانات وتحليلاتها في Microsoft Fabric Lakehouse.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>25</strong> دقيقة.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: ستحتاج إلى ترخيص Microsoft Fabric لإكمال هذا التمرين. راجع <a href="https://learn.microsoft.com/fabric/get-started/fabric-trial" rel="nofollow">بدء استخدام Fabric</a> للحصول على تفاصيل حول كيفية تمكين ترخيص تجريبي مجاني لـ Fabric. ستحتاج إلى حساب Microsoft الخاص بـ <em>المؤسسة التعليمية</em> أو <em>العمل</em> للقيام بذلك. إذا لم يكن لديك حساب، فيمكنك <a href="https://www.microsoft.com/microsoft-365/business/compare-more-office-365-for-business-plans" rel="nofollow">التسجيل للحصول على إصدار تجريبي من Microsoft Office 365 E3 أو إصدار أحدث</a>.</p>
</blockquote>
<p dir="rtl"><em>في المرة الأولى التي تستخدم فيها أي ميزات من ميزات Microsoft Fabric، قد تظهر المطالبات بالتلميحات. تجاهل هذه.</em></p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء مساحة عمل</h2><a id="user-content-إنشاء-مساحة-عمل" class="anchor" aria-label="Permalink: إنشاء مساحة عمل" href="#إنشاء-مساحة-عمل"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">قبل العمل مع البيانات في Fabric، قُم بإنشاء مساحة عمل مع تمكين الإصدار التجريبي لـ Fabric.</p>
<ol dir="rtl">
<li>
<p dir="rtl">سجل الدخول إلى <a href="https://app.fabric.microsoft.com" rel="nofollow">Microsoft Fabric</a> على <code>https://app.fabric.microsoft.com</code>.</p>
</li>
<li>
<p dir="rtl">في شريط القوائم، في الجزء السفلي الأيمن، قم بالتبديل إلى <strong>تجربة هندسة</strong> البيانات.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/fabric-switcher.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/fabric-switcher.png" alt="لقطة شاشة لقائمة مُبدّل التجربة." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في شريط القوائم على اليسار، حدد <strong>مساحات العمل</strong> (تبدو الأيقونة مشابهة لـ ).</p>
</li>
<li>
<p dir="rtl">أنشئ مساحة عمل جديدة باسم من اختيارك، مع تحديد وضع ترخيص في قسم <strong>المتقدمة</strong> يتضمن سعة Fabric (<em>الإصدار التجريبي</em> أو <em>Premium</em> أو <em>Fabric</em>).</p>
</li>
<li>
<p dir="rtl">عند فتح مساحة العمل الجديدة، يجب أن تكون فارغة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-workspace.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-workspace.png" alt="لقطة شاشة لمساحة عمل فارغة في Power BI." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء مستودع</h2><a id="user-content-إنشاء-مستودع" class="anchor" aria-label="Permalink: إنشاء مستودع" href="#إنشاء-مستودع"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن أصبح لديك مساحة عمل، حان الوقت لإنشاء مستودع بيانات لملفات البيانات الخاصة بك.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في الصفحة الرئيسية لمساحة العمل، قم بإنشاء Lakehouse** جديد **باسم من اختيارك.</p>
<p dir="rtl">بعد دقيقة أو نحو ذلك، سيتم إنشاء مستودعًا جديدًا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-lakehouse.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/new-lakehouse.png" alt="لقطة شاشة لمستودع جديد." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">أعرض المستودع الجديدة، ولاحظ أن جزء <strong>مُستكشف المستودع</strong> على اليسار يُمكنك من استعراض الجداول والملفات في المستودع:</p>
<ul dir="rtl">
<li>يحتوي مجلد <strong>الجداول</strong> على جداول يمكنك الاستعلام عنها باستخدام SQL. تستند الجداول في مستودع Microsoft Fabric إلى تنسيق ملف مصدر مفتوح <em>Delta Lake</em>، المستخدم عادة في Apache Spark.</li>
<li>يحتوي مجلد <strong>الملفات</strong> على ملفات بيانات في تخزين OneLake للمستودع غير المقترن بجداول دلتا المدارة. يمكنك أيضا إنشاء <em>اختصارات</em> في هذا المُجلد للإشارة إلى البيانات المخزنة خارجيًا.</li>
</ul>
<p dir="rtl">حاليًا، لا توجد جداول أو ملفات في المستودع.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استيعاب البيانات</h2><a id="user-content-استيعاب-البيانات" class="anchor" aria-label="Permalink: استيعاب البيانات" href="#استيعاب-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">طريقة بسيطة لاستيعاب البيانات هي استخدام نشاط <strong>نسخ البيانات</strong> في مسار لاستخراج البيانات من مصدر ونسخها إلى ملف في المستودع.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في <strong>الصفحة الرئيسية</strong> ل lakehouse، في <strong>قائمة Get data</strong> ، حدد <strong>New data pipeline</strong>، وأنشئ مسار بيانات جديدا باسم <strong>Ingest Data</strong>.</p>
</li>
<li>
<p dir="rtl">في <strong>معالج Copy Data</strong> ، في <strong>صفحة Choose a data source</strong> ، حدد <strong>Sample data</strong> ثم حدد مجموعة بيانات نموذج سيارة أجرة <strong>NYC - Green</strong> .</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/choose-data-source.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/choose-data-source.png" alt="لقطة شاشة لصفحة اختيار مصدر البيانات." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في <strong>صفحة الاتصال بمصدر</strong> البيانات، اعرض الجداول في مصدر البيانات. يجب أن يكون هناك جدول واحد يحتوي على تفاصيل رحلات سيارات الأجرة في مدينة نيويورك. ثُم حدد <strong>التالي</strong> للتقدم إلى صفحة <strong>اختيار وجهة البيانات</strong>.</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>اختيار وجهة البيانات</strong>، حدد مستودعك الحالي. بعد ذلك حدد <strong>التالي</strong>.</p>
</li>
<li>
<p dir="rtl">قُم بتعيين خيارات وجهة البيانات التالية، ثم حدد <strong>التالي</strong>:</p>
<ul dir="rtl">
<li><strong>المجلد الجذر</strong>: الجداول</li>
<li><strong>إعدادات التحميل</strong>: تحميل إلى جدول جديد</li>
<li><strong>اسم</strong> الجدول الوجهة: taxi_rides <em>(قد تحتاج إلى الانتظار حتى يتم عرض معاينة تعيينات الأعمدة قبل أن تتمكن من تغيير هذا)</em></li>
<li><strong>تعيينات الأعمدة</strong>: <em>اترك التعيينات الافتراضية كما هي</em></li>
<li><strong>تمكين التقسيم</strong>: <em>غير محدد</em></li>
</ul>
</li>
<li>
<p dir="rtl">في صفحة <strong>مراجعة + حفظ</strong>، تأكد من تحديد الخيار <strong>ابدأ بنقل البيانات على الفور</strong>، ثم حدد <strong>حفظ + تشغيل</strong>.</p>
<p dir="rtl">يتم إنشاء مسار جديد يحتوي على نشاط <strong>نسخ البيانات</strong>، كما هو موضح هنا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/copy-data-pipeline.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/copy-data-pipeline.png" alt="لقطة شاشة لمسار مع نشاط نسخ البيانات." style="max-width: 100%;"></a></p>
<p dir="rtl">عند بدء تشغيل المسار، يُمكنك مراقبة حالته في جزء <strong>الإخراج</strong> ضمن مُصمم المسار. استخدم الأيقونة <strong>&amp;8635؛</strong> (<em>تحديث</em>) لتحديث الحالة، وانتظر حتى يتم طلبها (والتي قد تستغرق 10 دقائق أو أكثر).</p>
</li>
<li>
<p dir="rtl">في شريط قائمة المركز على اليسار، حدد المستودع الخاص بك.</p>
</li>
<li>
<p dir="rtl">في <strong>الصفحة الرئيسية</strong> ، في <strong>جزء Lakehouse explorer</strong> ، في <strong>القائمة ...</strong> لعقدة <strong>Tables</strong> ، حدد <strong>Refresh</strong> ثم قم بتوسيع <strong>Tables</strong> للتحقق من <strong>إنشاء جدول taxi_rides</strong> .</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا كان الجدول الجديد مدرجا على أنه <em>غير معروف</em>، فاستخدم <strong>خيار القائمة Refresh</strong> لتحديث طريقة العرض.</p>
</blockquote>
</li>
<li>
<p dir="rtl"><strong>حدد الجدول taxi_rides</strong> لعرض محتوياته.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/dimProduct.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/dimProduct.png" alt="لقطة شاشة لجدول taxi_rides." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعلام عن البيانات في مستودع</h2><a id="user-content-الاستعلام-عن-البيانات-في-مستودع" class="anchor" aria-label="Permalink: الاستعلام عن البيانات في مستودع" href="#الاستعلام-عن-البيانات-في-مستودع"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن قُمت باستيعاب البيانات في جدول في مستودع، يُمكنك استخدام SQL للاستعلام عنها.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في الجزء العلوي الأيسر من صفحة Lakehouse، قم بالتبديل من <strong>طريقة عرض Lakehouse</strong> إلى <strong>نقطة</strong> نهاية تحليلات SQL ل lakehouse الخاص بك.</p>
</li>
<li>
<p dir="rtl">في شريط الأدوات، حدد <strong>استعلام SQL جديد</strong>. ثم أدخل كود SQL التالي في محرر الاستعلام:</p>
</li>
<div class="highlight highlight-source-sql notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">SELECT</span>  DATENAME(dw,lpepPickupDatetime) <span class="pl-k">AS</span> Day,
        <span class="pl-c1">AVG</span>(tripDistance) <span class="pl-k">As</span> AvgDistance
<span class="pl-k">FROM</span> taxi_rides
<span class="pl-k">GROUP BY</span> DATENAME(dw,lpepPickupDatetime)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="SELECT  DATENAME(dw,lpepPickupDatetime) AS Day,
        AVG(tripDistance) As AvgDistance
FROM taxi_rides
GROUP BY DATENAME(dw,lpepPickupDatetime)" tabindex="0" role="button">
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
<p dir="rtl"><strong>حدد &amp;9655; قم بتشغيل</strong> الزر لتشغيل الاستعلام ومراجعة النتائج، والتي يجب أن تتضمن متوسط مسافة الرحلة لكل يوم من أيام الأسبوع.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/sql-query.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/sql-query.png" alt="لقطة شاشة لاستعلام SQL." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تصور البيانات في مستودع</h2><a id="user-content-تصور-البيانات-في-مستودع" class="anchor" aria-label="Permalink: تصور البيانات في مستودع" href="#تصور-البيانات-في-مستودع"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تنظم مستودعات Microsoft Fabric Lakehouse كافة الجداول في نموذج بيانات دلالية، والذي يمكنك استخدامه لإنشاء تصورات وتقارير.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في أسفل يسار الصفحة، ضمن <strong>جزء Explorer</strong> ، حدد <strong>علامة التبويب Model</strong> لمشاهدة نموذج البيانات للجداول في lakehouse (يتضمن ذلك جداول النظام بالإضافة <strong>إلى جدول taxi_rides</strong> ).</p>
</li>
<li>
<p dir="rtl">في شريط الأدوات، حدد <strong>New report</strong> لإنشاء تقرير جديد استنادا <strong>إلى taxi_rides</strong>.</p>
</li>
<li>
<p dir="rtl">في مُصمم التقرير:</p>
<ol dir="rtl">
<li>
<p dir="rtl">في <strong>جزء البيانات</strong> ، قم بتوسيع <strong>الجدول taxi_rides</strong> وحدد <strong>حقلي lpepPickupDatetime</strong> و <strong>passengerCount</strong> .</p>
</li>
<li>
<p dir="rtl">في <strong>جزء المرئيات، حدد مرئيات المخطط</strong> الخطي. ثم تأكد من أن <strong>المحور</strong> س يحتوي على <strong>حقل lpepPickupDatetime</strong> وأن <strong>المحور ص</strong> يحتوي على <strong>مجموع عدد الركاب</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/fabric-report.png"><img src="https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals.ar-sa/blob/main/Instructions/Labs/images/fabric-report.png" alt="لقطة شاشة لتقرير Power BI." style="max-width: 100%;"></a></p>
</li>
</ol>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يُمكنك استخدام أيقونات <strong>&gt;&gt;</strong> لإخفاء أجزاء مُصمم التقرير لرؤية التقرير بشكل أكثر وضوحًا.</p>
</blockquote>
</li>
<li>
<p dir="rtl">في <strong>القائمة ملف</strong>، حدد <strong>حفظ</strong> لحفظ التقرير كتقرير **** سيارات الأجرة في مساحة عمل Fabric.</p>
<p dir="rtl">يمكنك العثور على التقرير في صفحة مساحة العمل الخاصة بك في مدخل Microsoft Fabric.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف الموارد</h2><a id="user-content-تنظيف-الموارد" class="anchor" aria-label="Permalink: تنظيف الموارد" href="#تنظيف-الموارد"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">إذا انتهيت من استكشاف Microsoft Fabric، يمكنك حذف مساحة العمل التي أنشأتها لهذا التمرين.</p>
<ol dir="rtl">
<li>في الشريط على اليسار، حدد أيقونة مساحة العمل لعرض كافة العناصر التي تحتوي عليها.</li>
<li>في القائمة <strong>...</strong> على شريط الأدوات، حدد <strong>إعدادات مساحة العمل</strong>.</li>
<li>في قسم <strong>الأخرى</strong>، حدد <strong>إزالة مساحة العمل هذه</strong>.</li>
</ol>
</article></div>
