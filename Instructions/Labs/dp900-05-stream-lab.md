---
lab:
  title: استكشاف Azure Stream Analytics
  module: Explore fundamentals of real-time analytics
---

# <a name="explore-azure-stream-analytics"></a>استكشاف Azure Stream Analytics

في هذا الإجراء، ستقوم بتوفير وظيفة Azure Stream Analytics في اشتراكك في Azure، واستخدامها لمعالجة دفق من البيانات في الوقت الفعلي.

سيستغرق إكمال هذا التمرين المعملي **15** دقيقة.

## <a name="before-you-start"></a>قبل البدء

ستحتاج إلى [اشتراك Azure](https://azure.microsoft.com/free) حيث تمتلك وصول على المستوى الإداري.

## <a name="create-azure-resources"></a>إنشاء موارد Azure

1. سجل الدخول إلى اشتراكك في Azure في [مدخل Microsoft Azure](https://portal.azure.com) باستخدام بيانات اعتماد اشتراك Azure.

1. Use the <bpt id="p1">**</bpt>[<ph id="ph1">\&gt;</ph>_]<ept id="p1">**</ept> button to the right of the search bar at the top of the page to create a new Cloud Shell in the Azure portal, selecting a <bpt id="p2">***</bpt>Bash<ept id="p2">***</ept> environment and creating storage if prompted. The cloud shell provides a command line interface in a pane at the bottom of the Azure portal, as shown here:

    ![مدخل Microsoft Azure مع جزء shell سحابي](./images/cloud-shell.png)

1. في Azure Cloud Shell، أدخل الأمر التالي لتنزيل الملفات التي ستحتاجها لهذا التمرين.

    ```bash
    git clone https://github.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals dp-900
    ```

1. انتظر حتى يكتمل الأمر، ثم أدخل الأمر التالي لتغيير الدليل الحالي إلى المجلد الذي يحتوي على الملفات الخاصة بهذا التمرين.

    ```bash
    cd dp-900/streaming
    ```

1. أدخل الأمر التالي لتشغيل برنامج نصي يقوم بإنشاء موارد Azure التي ستحتاجها في هذا التمرين.

    ```bash
    bash setup.sh
    ```

    انتظر ريثما يتم تشغيل البرنامج النصي وتنفيذ الإجراءات التالية:

    1. تثبيت ملحقات Azure CLI اللازمة لإنشاء الموارد (*يمكنك تجاهل أي تحذيرات حول الملحقات التجريبية*)
    1. تحديد مجموعة موارد Azure المتوفرة لهذا التمرين.
    1. إنشاء مورد *مركز Azure IoT*، والذي سيتم استخدامه لتلقي دفق بيانات من جهاز محاكاة.
    1. إنشاء *حساب Azure Storage*، والذي سيتم استخدامه لتخزين البيانات المعالجة.
    1. إنشاء وظيفة *Azure Stream Analytics*، والتي ستقوم بمعالجة بيانات الجهاز الواردة في الوقت الفعلي، وكتابة النتائج إلى حساب التخزين.

## <a name="explore-the-azure-resources"></a>استكشاف موارد Azure

1. In the <bpt id="p1">[</bpt>Azure portal<ept id="p1">](https://portal.azure.com?azure-portal=true)</ept>, on the home page, select <bpt id="p2">**</bpt>Resource groups<ept id="p2">**</ept> to see the resource groups in your subscription. This should include the <bpt id="p1">**</bpt>learn*xxxxxxxxxxxxxxxxx...<ept id="p1">**</ept>* resource group identified by the setup script.
2. حدد مجموعة الموارد "**learn*xxxxxxxxxxxxxxxxx...** *"، وراجع الموارد التي تحتوي عليها، والتي ينبغي أن تشمل:
    - *مركز IoT* يسمى **iothub*xxxxxxxxxxxxx***، والذي يستخدم لتلقي بيانات الجهاز الواردة.
    - *حساب تخزين* يسمى **store*xxxxxxxxxxxx***، الذي ستتم كتابة نتائج معالجة البيانات إليه.
    - *وظيفة Stream Analytics* المسماة *stream*xxxxxxxxxxxxx***، والتي سيتم استخدامها لمعالجة بيانات الدفق.

    إذا لم يتم سرد هذه الموارد الثلاثة، فانقر فوق زر **&#8635; Refresh** حتى تظهر.

    > **ملاحظة**: إذا كنت تستخدم بيئة الاختبار المعزولة للتعلم، فقد تحتوي مجموعة الموارد أيضاً على *حساب تخزين* ثانٍ باسم **cloudshell*xxxxxxxx***، والذي يُستخدم لتخزين البيانات لـ Azure Cloud Shell الذي استخدمته لتشغيل البرنامج النصي للإعداد.

3. حدد وظيفة **stream*xxxxxxxxxxxxx*** Stream Analytics، واعرض المعلومات على صفحة **النظرة العامة** الخاصة به، مع ملاحظة التفاصيل التالية:
    - The job has one <bpt id="p1">*</bpt>input<ept id="p1">*</ept> named <bpt id="p2">**</bpt>iotinput<ept id="p2">**</ept>, and one <bpt id="p3">*</bpt>output<ept id="p3">*</ept> named <bpt id="p4">**</bpt>bloboutput<ept id="p4">**</ept>. These reference the IoT Hub and Storage account created by the setup script.
    - تحتوي الوظيفة على *استعلام*، يقرأ البيانات من إدخال **iotinput**، ويجمعها عن طريق حساب عدد الرسائل التي تتم معالجتها كل 10 ثوانٍ؛ وكتابة النتائج إلى إخراج **bloboutput**.

## <a name="use-the-resources-to-analyze-streaming-data"></a>استخدام الموارد لتحليل بيانات الدفق

1. في الجزء العلوي من صفحة **نظرة عامة** لوظيفة Stream Analytics، حدد زر **&#9655; Start**، ثم في جزء **Start job**، حدد **Start** لبدء المهمة.
2. انتظر إعلامًا بأن مهمة الدفق بدأت بنجاح.
3. قم بالتبديل مرة أخرى إلى Azure Cloud Shell، وأدخل الأمر التالي لمحاكاة جهاز يرسل البيانات إلى مركز IoT.

    ```
    bash iotdevice.sh
    ```

4. انتظر حتى تبدأ المحاكاة، والتي ستتم الإشارة إليها من خلال إخراج مثل هذا:

    ```
    Device simulation in progress: 6%|#    | 7/120 [00:08<02:21, 1.26s/it]
    ```

5. أثناء تشغيل المحاكاة، مرة أخرى في مدخل Azure، ارجع إلى الصفحة الخاصة بمجموعة الموارد "**learn*xxxxxxxxxxxxxxxxx...** *"، وحدد حساب التخزين "**store*xxxxxxxxxxxx***".
6. في الجزء الموجود على يسار جزء حساب التخزين، حدد علامة تبويب **"Containers"**.
7. افتح حاوية **البيانات**.
8. في حاوية **البيانات**، انتقل عبر التسلسل الهيكلي للمجلدات، والذي يتضمن مجلدًا للسنة الحالية، مع مجلدات فرعية للشهر واليوم والساعة.
9. في المجلد للساعة، حدد الملف الذي تم إنشاؤه، والذي يجب أن يكون له اسم مشابه لـ **0_xxxxxxxxxxxxxxxx.json**.
10. في صفحة الملف، حدد **Edit**، وراجع محتويات الملف؛ والتي يجب أن تتكون من سجل JSON لكل فترة 10 ثوانٍ، مع عرض عدد الرسائل المستلمة من أجهزة إنترنت الأشياء، مثل هذا:

    ```
    {"starttime":"2021-10-23T01:02:13.2221657Z","endtime":"2021-10-23T01:02:23.2221657Z","device":"iotdevice","messages":2}
    {"starttime":"2021-10-23T01:02:14.5366678Z","endtime":"2021-10-23T01:02:24.5366678Z","device":"iotdevice","messages":3}
    {"starttime":"2021-10-23T01:02:15.7413754Z","endtime":"2021-10-23T01:02:25.7413754Z","device":"iotdevice","messages":4}
    ...
    ```

11. استخدم زر **&#8635; Refresh** لتحديث الملف، مع ملاحظة أنه تتم كتابة نتائج إضافية إلى الملف، حيث تقوم وظيفة Stream Analytics بمعالجة بيانات الجهاز في الوقت الحقيقي حيث يتم دفقها من الجهاز إلى مركز إنترنت الأشياء.
12. ارجع إلى Azure Cloud Shell، وانتظر حتى تنتهي محاكاة الجهاز (يجب أن تعمل لمدة 3 دقائق تقريبًا).
13. مرة أخرى في مدخل Azure، قم بتحديث الملف مرة أخرى لمشاهدة المجموعة الكاملة من النتائج التي تم إنتاجها أثناء المحاكاة.
14. ارجع إلى مجموعة الموارد "**learn*xxxxxxxxxxxxxxxxx...** * "، وأعد فتح مهمة Stream Analytics "**stream*xxxxxxxxxxxxx***".
15. في أعلى صفحة وظيفة Stream Analytics، استخدم زر ** إيقاف&#11036;** لإيقاف المهمة، مع التأكيد عند المطالبة بذلك.

> **ملاحظة**: احذف مجموعة الموارد التي أنشأتها في هذا التمرين إذا انتهيت من استكشاف حل الدفق.
