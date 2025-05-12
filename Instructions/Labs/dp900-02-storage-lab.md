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
  <td><div dir="rtl">استكشاف Azure Storage</div></td>
  <td><div dir="rtl">Explore Azure Storage for non-relational data</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Storage</h1><a id="user-content-استكشاف-azure-storage" class="anchor" aria-label="Permalink: استكشاف Azure Storage" href="#استكشاف-azure-storage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، ستقوم بتوفير حساب Azure Storage في اشتراكك في Azure، واستكشاف الطرق المختلفة التي يمكنك استخدامها لتخزين البيانات.</p>
<p dir="rtl">سيستغرق إكمال هذا التمرين المعملي <strong>15</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">قبل أن تبدأ</h2><a id="user-content-قبل-أن-تبدأ" class="anchor" aria-label="Permalink: قبل أن تبدأ" href="#قبل-أن-تبدأ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستحتاج إلى <a href="https://azure.microsoft.com/free" rel="nofollow">اشتراك Azure</a> حيث تمتلك وصول على المستوى الإداري.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">توفير حساب Azure Storage</h2><a id="user-content-توفير-حساب-azure-storage" class="anchor" aria-label="Permalink: توفير حساب Azure Storage" href="#توفير-حساب-azure-storage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">تتمثل الخطوة الأولى في استخدام Azure Storage في توفير حساب Azure Storage في اشتراكك في Azure.</p>
<ol dir="rtl">
<li>
<p dir="rtl">إذا لم تكن فعلت ذلك، فسجّل الدخول إلى <a href="https://portal.azure.com?azure-portal=true" rel="nofollow">مدخل Microsoft Azure</a>.</p>
</li>
<li>
<p dir="rtl">في الصفحة الرئيسية لمدخل Microsoft Azure، حدد "<strong>＋ Create a resource</strong>" من الزاوية العلوية اليسرى وابحث عن "<em>Storage account</em>". ثم في صفحة <strong>حساب التخزين</strong> الناتجة، حدد <strong>"Create"</strong>.</p>
</li>
<li>
<p dir="rtl">أدخل القيم التالية في الصفحة <strong>إنشاء حساب تخزين</strong>:</p>
<ul dir="rtl">
<li><strong>الاشتراك</strong>: حدد اشتراك Azure الخاص بك.</li>
<li><strong>مجموعة الموارد</strong>: قم بإنشاء مجموعة موارد جديدة باسم من اختيارك.</li>
<li><strong>اسم حساب التخزين</strong>: أدخل اسماً فريداً لحساب التخزين باستخدام الأحرف الصغيرة والأرقام.</li>
<li><strong>Region</strong>: حدد أي موقع متاح.</li>
<li><strong>الأداء</strong>: <em>قياسي</em></li>
<li><strong>التكرار</strong>: <em>التخزين المتكرر محلياً (LRS)</em></li>
</ul>
</li>
<li>
<p dir="rtl">حدد "<strong>Next: Advanced &gt;</strong>" واعرض خيارات التكوين المتقدمة. على وجه الخصوص، لاحظ أن هذا هو المكان الذي يمكنك فيه تمكين مساحة أسماء هرمية لدعم Azure Data Lake Storage Gen2. اترك هذا الخيار <strong>unselected</strong> (ستُمكنه لاحقاً)، ثم حدد "<strong>Next: Networking &gt;</strong>" لعرض خيارات الشبكة لحساب التخزين.</p>
</li>
<li>
<p dir="rtl">حدد "<strong>Next: Data protection &gt;</strong>" ثم في القسم "<strong>Recovery</strong>" ألغ تحديد جميع خيارات "<strong>Enable soft delete...</strong>". تحتفظ هذه الخيارات بالملفات المحذوفة للاسترداد اللاحق، ولكن يمكن أن تسبب مشكلات لاحقاً عند تمكين مساحة أسماء هرمية.</p>
</li>
<li>
<p dir="rtl">استمر عبر صفحات <strong>التالي &gt;</strong> المتبقية دون تغيير أي من الإعدادات الافتراضية، ثم في صفحة <strong>المراجعة</strong>، انتظر حتى يتم التحقق من صحة ما حددت، وحدد <strong>إنشاء</strong>" لإنشاء حساب Azure Storage.</p>
</li>
<li>
<p dir="rtl">يُرجى الانتظار لاكتمال التوزيع. ثم انتقل إلى المورد الذي تم توزيعه.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشاف تخزين كائن ثنائي كبير الحجم</h2><a id="user-content-استكشاف-تخزين-كائن-ثنائي-كبير-الحجم" class="anchor" aria-label="Permalink: استكشاف تخزين كائن ثنائي كبير الحجم" href="#استكشاف-تخزين-كائن-ثنائي-كبير-الحجم"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن أصبح لديك حساب Azure Storage، يمكنك إنشاء حاوية لبيانات الكائن الثنائي كبير الحجم.</p>
<ol dir="rtl">
<li>
<p dir="rtl">قم بتنزيل ملف JSON <a href="https://aka.ms/product1.json?azure-portal=true" rel="nofollow">product1.json</a> من <code>https://aka.ms/product1.json</code> واحفظه على جهاز الكمبيوتر (يمكنك حفظه في أي مجلد - ستقوم بتحميله إلى تخزين كائن ثنائي كبير الحجم لاحقاً).</p>
<p dir="rtl"><em>إذا تم عرض ملف JSON في المتصفح، فاحفظ الصفحة كـ <strong>product1.json</strong>.</em></p>
</li>
<li>
<p dir="rtl">في صفحة مدخل Microsoft Azure لحاوية التخزين، على الجانب الأيسر، في القسم <strong>Data storage</strong>، حدد <strong>Containers</strong>.</p>
</li>
<li>
<p dir="rtl">في <strong>صفحة Containers</strong> ، حدد <strong>&amp;65291; حاوية</strong> وإضافة حاوية جديدة باسم <strong>البيانات</strong> بمستوى وصول مجهول خاص <strong>(بدون وصول مجهول)</strong>.</p>
</li>
<li>
<p dir="rtl">عند إنشاء الحاوية <strong>data</strong>، تحقق من إدراجها في الصفحة <strong>Containers</strong>.</p>
</li>
<li>
<p dir="rtl">في الجزء الموجود على الجانب الأيسر، في القسم العلوي، حدد <strong>Storage browser</strong>. توفر هذه الصفحة واجهة تستند إلى المتصفح يمكنك استخدامها للعمل مع البيانات في حساب التخزين الخاص بك.</p>
</li>
<li>
<p dir="rtl">في صفحة متصفح موقع التخزين، حدد <strong>Blob containers</strong> وتحقق من إدراج الحاوية <strong>data</strong>.</p>
</li>
<li>
<p dir="rtl">حدد حاوية <strong>data</strong>، ولاحظ أنها فارغة.</p>
</li>
<li>
<p dir="rtl">حدد "<strong>＋ Add Directory</strong>" واقرأ المعلومات عن المجلدات قبل إنشاء دليل جديد باسم <strong>products</strong>.</p>
</li>
<li>
<p dir="rtl">في مستعرض التخزين، تحقق من أن طريقة العرض الحالية تُظهر محتويات مجلد <strong>المنتجات</strong> الذي أنشأته للتو - لاحظ أن "فتات التنقل" في أعلى الصفحة تعكس مسار <strong>حاويات Blob&gt; البيانات&gt; المنتجات</strong>.</p>
</li>
<li>
<p dir="rtl">في مسارات التنقل، حدد <strong>data</strong> للتبديل إلى الحاوية <strong>data</strong>، ولاحظ أنها لا تحتوي على مجلد باسم <strong>products</strong>.</p>
<p dir="rtl">المجلدات الموجودة في تخزين كائن ثنائي كبير الحجم مجلدات ظاهرية، ولا توجد إلا كجزء من مسار الكائن الثنائي كبير الحجم. نظراً لأن المجلد <strong>products</strong> لا يحتوي على كائنات ثنائية كبيرة الحجم، فهو ليس موجوداً حقاً!</p>
</li>
<li>
<p dir="rtl">استخدم الزر "<strong>⤒ Upload</strong>" لفتح اللوحة "<strong>Upload blob</strong>".</p>
</li>
<li>
<p dir="rtl">في اللوحة <strong>Upload blob</strong>، حدد الملف <strong>product1.json</strong> الذي حفظته على جهاز الكمبيوتر المحلي مسبقاً. ثم في القسم <strong>Advanced</strong>، في المربع <strong>Upload to folder</strong>، أدخل <strong>product_data</strong> وحدد الزر <strong>Upload</strong>.</p>
</li>
<li>
<p dir="rtl">أغلق اللوحة <strong>Upload blob</strong> إذا كانت لا تزال مفتوحة، وتحقق من إنشاء المجلد الظاهري <strong>product_data</strong> في الحاوية <strong>data</strong>.</p>
</li>
<li>
<p dir="rtl">حدد المجلد <strong>product_data</strong> وتحقق من أنه يحتوي على الكائن الثنائي كبير الحجم <strong>product1.json</strong> الذي قمت بتحميله.</p>
</li>
<li>
<p dir="rtl">على الجانب الأيسر، في القسم <strong>Data storage</strong>، حدد <strong>Containers</strong>.</p>
</li>
<li>
<p dir="rtl">افتح الحاوية <strong>data</strong>، وتحقق من إدراج المجلد <strong>product_data</strong> الذي أنشأته.</p>
</li>
<li>
<p dir="rtl">حدد الأيقونة " <strong>‧‧‧</strong>" في أقصى يمين المجلد، ولاحظ أنه لا يعرض أي خيارات. المجلدات الموجودة في حاوية كائن ثنائي كبير الحجم لمساحة اسم ثابت هي مجلدات ظاهرية، ولا يمكن إدارتها.</p>
</li>
<li>
<p dir="rtl">استخدم الأيقونة <strong>X</strong> أعلى يمين الصفحة <strong>data</strong> لإغلاق الصفحة والعودة إلى الصفحة <strong>Containers</strong>.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">Explore Azure Data Lake Storage Gen2</h2><a id="user-content-explore-azure-data-lake-storage-gen2" class="anchor" aria-label="Permalink: Explore Azure Data Lake Storage Gen2" href="#explore-azure-data-lake-storage-gen2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يتيح لك دعم Azure Data Lake Store Gen2 استخدام المجلدات الهرمية لتنظيم الوصول إلى الكائنات الثنائية كبيرة الحجم وإدارته. كما أنه يُمكّنك من استخدام تخزين كائن ثنائي كبير الحجم من Azure لاستضافة أنظمة الملفات الموزعة لمنصات تحليلات البيانات الضخمة الشائعة.</p>
<ol dir="rtl">
<li>قم بتنزيل <a href="https://aka.ms/product2.json?azure-portal=true" rel="nofollow">ملف JSON product2.json</a> من <code>https://aka.ms/product2.json</code> واحفظه على الكمبيوتر في نفس المجلد حيث قمت بتنزيل <strong>product1.json</strong> مسبقا - ستقوم بتحميله إلى تخزين blob لاحقا.</li>
<li>في صفحة مدخل Microsoft Azure لحساب التخزين، على الجانب الأيسر، مرر لأسفل إلى القسم "<strong>Settings</strong>"، وحدد "<strong>Data Lake Gen2 upgrade</strong>".</li>
<li>في الصفحة <strong>Data Lake Gen2 upgrade</strong>، وسّع الصفحة وأكمل جميع الخطوات لترقية حساب التخزين لتمكين مساحة أسماء هرمية ودعم Azure Data Lake Storage Gen 2. قد يستغرق هذا بعض الوقت.</li>
<li>عند اكتمال الترقية، في الجزء الموجود على الجانب الأيسر، في القسم العلوي، حدد "<strong>Storage browser</strong>" وانتقل مرة أخرى إلى جذر حاوية الكائن الثنائي كبير الحجم <strong>data</strong>، التي لا تزال تحتوي على المجلد "<strong>product_data</strong>".</li>
<li>حدد المجلد <strong>product_data</strong>، وتحقق من أنه لا يزال يحتوي على ملف <strong>product1.json</strong> الذي قمت بتحميله مسبقاً.</li>
<li>استخدم الزر "<strong>⤒ Upload</strong>" لفتح اللوحة "<strong>Upload blob</strong>".</li>
<li>في اللوحة <strong>Upload blob</strong>، حدد ملف <strong>product2.json</strong> الذي حفظته على الكمبيوتر المحلي. حدد الزر ⁧<strong>Upload</strong>⁩.</li>
<li>أغلق اللوحة <strong>Upload blob</strong> إذا كانت لا تزال مفتوحة، وتحقق من أن المجلد <strong>product_data</strong> يحتوي الآن على الملف <strong>product2.json.</strong></li>
<li>على الجانب الأيسر، في القسم <strong>Data storage</strong>، حدد <strong>Containers</strong>.</li>
<li>افتح الحاوية <strong>data</strong>، وتحقق من إدراج المجلد <strong>product_data</strong> الذي أنشأته.</li>
<li>حدد الرمز "<strong>‧‧‧</strong>" في أقصى يمين المجلد، ولاحظ أنه يمكنك تنفيذ مهام التكوين على مستوى المجلد مع تمكين مساحة أسماء الهرمية، بما في ذلك إعادة تسمية المجلدات وأذونات الإعداد.</li>
<li>استخدم الأيقونة <strong>X</strong> أعلى يمين الصفحة <strong>data</strong> لإغلاق الصفحة والعودة إلى الصفحة <strong>Containers</strong>.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Files</h2><a id="user-content-استكشاف-azure-files" class="anchor" aria-label="Permalink: استكشاف Azure Files" href="#استكشاف-azure-files"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يوفر Azure Files طريقة لإنشاء مشاركات الملفات المستندة إلى السحابة.</p>
<ol dir="rtl">
<li>في صفحة مدخل Microsoft Azure لحاوية التخزين الخاصة بك، على الجانب الأيسر، في قسم <strong>Data storage</strong>، حدد <strong>File shares</strong>.</li>
<li>في صفحة "File shares"، حدد "<strong>＋ File share</strong>" وأضف مشاركة ملف جديدة باسم <strong>files</strong> باستخدام الطبقة "<strong>Transaction optimized</strong>".</li>
<li>حدد <strong>التالي: &gt;</strong> النسخ الاحتياطي وتعطيل النسخ الاحتياطي. ثم حدد <strong>«Review + create»</strong>.</li>
<li>في <strong>File shares</strong>، افتح مشاركة <strong>الملفات</strong> الجديدة.</li>
<li>في أعلى الصفحة، حدد <strong>Connect</strong>. ثم في الجزء <strong>Connect</strong>، لاحظ أن هناك علامات تبويب لأنظمة التشغيل الشائعة (Windows وLinux وmacOS) تحتوي على برامج نصية يمكنك تشغيلها للاتصال بالمجلد المشترك من كمبيوتر عميل.</li>
<li>أغلق الجزء <strong>Connect</strong> ثم أغلق الصفحة <strong>files</strong> للعودة إلى الصفحة <strong>File shares</strong> على حساب Azure storage.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استكشاف Azure Tables</h2><a id="user-content-استكشاف-azure-tables" class="anchor" aria-label="Permalink: استكشاف Azure Tables" href="#استكشاف-azure-tables"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">توفر Azure Tables مخزن المفاتيح/القيم للتطبيقات التي تحتاج إلى تخزين قيم البيانات، ولكنها لا تحتاج إلى الوظائف الكاملة وبنية قاعدة البيانات الارتباطية.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في صفحة مدخل Microsoft Azure لحاوية التخزين الخاصة بك، على الجانب الأيسر، في القسم <strong>Data storage</strong>، حدد <strong>Tables</strong>.</p>
</li>
<li>
<p dir="rtl">في صفحة "<strong>Tables</strong>"، حدد "<strong>＋ Table</strong>" وأنشئ جدولاً جديداً باسم <strong>products</strong>.</p>
</li>
<li>
<p dir="rtl">بعد إنشاء الجدول <strong>products</strong>، في الجزء على الجانب الأيسر، في القسم العلوي، حدد "<strong>Storage browser</strong>".</p>
</li>
<li>
<p dir="rtl">في مستكشف التخزين، حدد <strong>Tables</strong> وتحقق من إدراج الجدول <strong>products</strong>.</p>
</li>
<li>
<p dir="rtl">حدد الجدول <strong>products</strong>.</p>
</li>
<li>
<p dir="rtl">في صفحة "<strong>product</strong>"، حدد "<strong>＋ Add entity</strong>".</p>
</li>
<li>
<p dir="rtl">في اللوحة <strong>Add entity</strong>، أدخل القيم الرئيسية التالية:</p>
<ul dir="rtl">
<li><strong>PartitionKey</strong>: 1</li>
<li><strong>RowKey</strong>: 1</li>
</ul>
</li>
<li>
<p dir="rtl">حدد <strong>Add property</strong>، وقم بإنشاء خاصية جديدة بالقيم التالية:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>اسم الخاصية</th>
<th>نوع</th>
<th>القيمة‬</th>
</tr>
</thead>
<tbody>
<tr>
<td>الاسم</td>
<td>السلسلة‬</td>
<td>عنصر واجهة المستخدم</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">أضف خاصية ثانية بالقيم التالية:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>اسم الخاصية</th>
<th>نوع</th>
<th>القيمة‬</th>
</tr>
</thead>
<tbody>
<tr>
<td>السعر</td>
<td>مزدوج</td>
<td>2.99</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">حدد <strong>Insert</strong> لإدراج صف للكيان الجديد في الجدول.</p>
</li>
<li>
<p dir="rtl">في متصفح التخزين، تحقق من إضافة صف إلى الجدول <strong>products</strong>، ومن إنشاء عمود <strong>طابع زمني</strong> للإشارة إلى آخر تعديل للصف.</p>
</li>
<li>
<p dir="rtl">أضف كياناً آخر إلى الجدول <strong>products</strong> بالخصائص التالية:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>اسم الخاصية</th>
<th>نوع</th>
<th>القيمة‬</th>
</tr>
</thead>
<tbody>
<tr>
<td>PartitionKey</td>
<td>السلسلة‬</td>
<td>1</td>
</tr>
<tr>
<td>RowKey</td>
<td>السلسلة‬</td>
<td>2</td>
</tr>
<tr>
<td>الاسم</td>
<td>السلسلة‬</td>
<td>Kniknak</td>
</tr>
<tr>
<td>السعر</td>
<td>مزدوج</td>
<td>1.99</td>
</tr>
<tr>
<td>إيقاف</td>
<td>Boolean</td>
<td>صحيح</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">بعد إدراج الكيان الجديد، تحقق من عرض صف يحتوي على المنتج الذي تم إيقافه في الجدول.</p>
<p dir="rtl">لقد قمت بإدخال البيانات يدوياً في الجدول باستخدام واجهة متصفح التخزين. في سيناريو حقيقي، يمكن لمطوري التطبيقات استخدام واجهة برمجة تطبيقات Azure Storage Table لإنشاء تطبيقات تقرأ القيم وتكتبها إلى الجداول، ما يجعلها حلاً فعالاً من حيث التكلفة وقابلاً للتطوير لتخزين NoSQL.</p>
</li>
</ol>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: يمكنك حذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف Azure Storage.</p>
</blockquote>
</article></div>
