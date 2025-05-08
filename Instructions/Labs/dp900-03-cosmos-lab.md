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
  <td><div dir="rtl">استكشاف Azure Cosmos DB</div></td>
  <td><div dir="rtl">Explore fundamentals of Azure Cosmos DB</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Cosmos DB</h1><a id="user-content-استكشاف-azure-cosmos-db" class="anchor" aria-label="Permalink: استكشاف Azure Cosmos DB" href="#استكشاف-azure-cosmos-db"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، ستقوم بتوفير قاعدة بيانات Azure Cosmos DB في اشتراكك في Azure، واستكشاف الطرق المختلفة التي يمكنك استخدامها لتخزين البيانات غير العلائقية.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>15</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قم بإنشاء حساب Cosmos DB</h2><a id="user-content-قم-بإنشاء-حساب-cosmos-db" class="anchor" aria-label="Permalink: قم بإنشاء حساب Cosmos DB" href="#قم-بإنشاء-حساب-cosmos-db"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لاستخدام Cosmos DB، يجب عليك توفير حساب Cosmos DB في اشتراك Azure الخاص بك. في هذا التمرين، ستوفر حساب Cosmos DB يستخدم Azure Cosmos DB لـ NoSQL.</p>
<ol dir="rtl">
<li>في مدخل Azure، حدد <strong>+ Create a resource</strong> في أعلى اليسار، وابحث عن <em>Azure Cosmos DB</em>.  في النتائج، حدد "<strong>Azure Cosmos DB</strong>" وحدد "<strong>Create</strong>".</li>
<li>في اللوحة <strong>Azure Cosmos DB لـ NoSQL</strong>، حدد <strong>Create</strong>.</li>
<li>أدخل التفاصيل التالية، ثم حدد <strong>Review + Create</strong>:
<ul dir="rtl">
<li><strong>Subscription</strong>: إذا كنت تستخدم بيئة الاختبار المعزولة، حدد <em>Concierge Subscription</em>. وإن لم يكن كذلك، حدد اشتراكك في Azure.</li>
<li><strong>Resource group</strong>: إذا كنت تستخدم بيئة الاختبار المعزولة، فحدد مجموعة الموارد الموجودة (والتي سيكون لها اسم مثل <em>learn-xxxx...</em>). وإلا، أنشئ مجموعة موارد جديدة باسم من اختيارك.</li>
<li><strong>Account Name</strong>: أدخل اسمًا فريدًا</li>
<li><strong>Location</strong>: اختر أي موقع موصى به</li>
<li><strong>Capacity mode</strong>: معدل النقل المقدم</li>
<li><strong>Apply Free-Tier Discount</strong>: حدد تطبيق إذا كان ذلك متوفرًا</li>
<li><strong>Limit total account throughput</strong>: غير محدد</li>
</ul>
</li>
<li>عند التحقق من صحة التكوين، حدد <strong>Create</strong>.</li>
<li>يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى المورد الموزع.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء نموذج قاعدة البيانات</h2><a id="user-content-إنشاء-نموذج-قاعدة-البيانات" class="anchor" aria-label="Permalink: إنشاء نموذج قاعدة البيانات" href="#إنشاء-نموذج-قاعدة-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl"><em>خلال هذا الإجراء، أغلق أي تلميحات يتم عرضها في المدخل</em>.</p>
<ol dir="rtl">
<li>في الصفحة الخاصة بحساب Cosmos DB الجديد، في الجزء n الأيسر، حدد <strong>Data Explorer</strong>.</li>
<li>في صفحة <strong>Data Explorer</strong>، حدد <strong>Launch quick start</strong>.</li>
<li>في علامة التبويب <strong>New container</strong>، راجع الإعدادات التي تم ملؤها مسبقا لقاعدة بيانات العينة، ثم حدد <strong>OK</strong>.</li>
<li>راقب الحالة في اللوحة الموجودة أسفل الشاشة حتى يتم إنشاء قاعدة بيانات <strong>SampleDB</strong> وحاوية <strong>SampleContainer</strong> (والتي قد تستغرق دقيقة أو نحو ذلك).</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">عرض العناصر وإنشائها</h2><a id="user-content-عرض-العناصر-وإنشائها" class="anchor" aria-label="Permalink: عرض العناصر وإنشائها" href="#عرض-العناصر-وإنشائها"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في الصفحة Data Explorer، قم بتوسيع قاعدة بيانات <strong>SampleDB</strong> وحاوية <strong>SampleContainer</strong>، وحدد <strong>Items</strong> لرؤية قائمة بالعناصر الموجودة في الحاوية. تمثل العناصر بيانات المنتج، ولكل منها مُعرّف فريد وخصائص أخرى.</p>
</li>
<li>
<p dir="rtl">حدد أيًا من العناصر الموجودة في القائمة للاطلاع على تمثيل JSON لبيانات العنصر.</p>
</li>
<li>
<p dir="rtl">في أعلى الصفحة، حدد <strong>New Item</strong> لإنشاء عنصر فارغ جديد.</p>
</li>
<li>
<p dir="rtl">قم بتعديل JSON للعنصر الجديد كما يلي، ثم حدد <strong>Save</strong>.</p>
</li>
<div class="highlight highlight-source-json notranslate position-relative overflow-auto" dir="auto"><pre>{
    <span class="pl-ent">"name"</span>: <span class="pl-s"><span class="pl-pds">"</span>Road Helmet,45<span class="pl-pds">"</span></span>,
    <span class="pl-ent">"id"</span>: <span class="pl-s"><span class="pl-pds">"</span>123456789<span class="pl-pds">"</span></span>,
    <span class="pl-ent">"categoryID"</span>: <span class="pl-s"><span class="pl-pds">"</span>123456789<span class="pl-pds">"</span></span>,
    <span class="pl-ent">"SKU"</span>: <span class="pl-s"><span class="pl-pds">"</span>AB-1234-56<span class="pl-pds">"</span></span>,
    <span class="pl-ent">"description"</span>: <span class="pl-s"><span class="pl-pds">"</span>The product called <span class="pl-cce">\"</span>Road Helmet,45<span class="pl-cce">\"</span> <span class="pl-pds">"</span></span>,
    <span class="pl-ent">"price"</span>: <span class="pl-c1">48.74</span>
}</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="{
    &quot;name&quot;: &quot;Road Helmet,45&quot;,
    &quot;id&quot;: &quot;123456789&quot;,
    &quot;categoryID&quot;: &quot;123456789&quot;,
    &quot;SKU&quot;: &quot;AB-1234-56&quot;,
    &quot;description&quot;: &quot;The product called \&quot;Road Helmet,45\&quot; &quot;,
    &quot;price&quot;: 48.74
}" tabindex="0" role="button">
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
<p dir="rtl">بعد حفظ العنصر الجديد، لاحظ إضافة خصائص بيانات تعريف إضافية تلقائيًا.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعلام عن قاعدة البيانات</h2><a id="user-content-الاستعلام-عن-قاعدة-البيانات" class="anchor" aria-label="Permalink: الاستعلام عن قاعدة البيانات" href="#الاستعلام-عن-قاعدة-البيانات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">في الصفحة <strong>Data Explorer</strong>، حدد أيقونة <strong>New SQL Query</strong>.</p>
</li>
<li>
<p dir="rtl">في محرر الاستعلام SQL، راجع الاستعلام الافتراضي (<code>SELECT * FROM c</code>) واستخدم الزر <strong>Execute Query</strong> لتشغيله.</p>
</li>
<li>
<p dir="rtl">راجع النتائج، والتي تتضمن تمثيل JSON الكامل لجميع العناصر.</p>
</li>
<li>
<p dir="rtl">تغيير الاستعلام كما يلي:</p>
</li>
<div class="highlight highlight-source-sql notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">SELECT</span> <span class="pl-k">*</span>
<span class="pl-k">FROM</span> c
<span class="pl-k">WHERE</span> CONTAINS(<span class="pl-c1">c</span>.<span class="pl-c1">name</span>,<span class="pl-s"><span class="pl-pds">"</span>Helmet<span class="pl-pds">"</span></span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="SELECT *
FROM c
WHERE CONTAINS(c.name,&quot;Helmet&quot;)" tabindex="0" role="button">
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
<p dir="rtl">استخدم زر <strong>تنفيذ الاستعلام</strong> لتشغيل الاستعلام المعدل ومراجعة النتائج، والتي تتضمن كيانات JSON لأي عناصر تحتوي على حقل <strong>اسم</strong> يحتوي على النص "Helmet".</p>
</li>
<li>
<p dir="rtl">أغلق محرر استعلام SQL، مع تجاهل التغييرات.</p>
<p dir="rtl">لقد رأيت كيفية إنشاء كيانات JSON والاستعلام عنها في قاعدة بيانات Cosmos DB باستخدام واجهة مستكشف البيانات في مدخل Azure. في سيناريو حقيقي، سيستخدم مطور تطبيقات واحدة من العديد من مجموعات تطوير البرامج (SDKs) الخاصة بلغة البرمجة لاستدعاء واجهة برمجة التطبيقات NoSQL والعمل مع البيانات الموجودة في قاعدة البيانات.</p>
</li>
</ol>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Cosmos DB.</p>
</blockquote>
</article></div>
