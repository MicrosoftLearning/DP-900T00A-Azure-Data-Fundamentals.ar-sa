---
title: التعليمات المستضافة عبر الإنترنت
permalink: index.html
layout: home
---

# أساسيات Azure Data Fundamentals

تم تصميم هذه التدريبات العملية لدعم محتوى التدريب على [Microsoft Learn](https://docs.microsoft.com/training/).

لإكمال هذه التمارين، ستحتاج إلى اشتراك Microsoft Azure حيث لديك أذونات إدارية. يمكنك التسجيل للحصول على نسخة تجريبية مجانية في [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| تدريب |
| --- |
{% للأنشطة في المعامل %}| [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
