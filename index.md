---
title: تعليمات مستضافة عبر الإنترنت
permalink: index.html
layout: home
ms.openlocfilehash: 928f59a9cdc6a3f70d5ad651fb1b5a45b405cee8
ms.sourcegitcommit: 1117342052bce0bbd5a703bd1f763862b9129807
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/16/2022
ms.locfileid: "140682420"
---
# <a name="azure-data-fundamentals-exercises"></a>أساسيات Azure Data Fundamentals

استخدم الروابط أدناه لإكمال التدريبات المعملية العملية لدورة Microsoft التدريبية [AI-900 *Microsoft Azure Data Fundamentals*](https://docs.microsoft.com/learn/certifications/courses/dp-900t00).

لإكمال هذه التمارين، ستحتاج إلى اشتراك Microsoft Azure. إذا لم يزودك مدربك بواحد، فيمكنك التسجيل للحصول على نسخة تجريبية مجانية على [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| الوحدة النمطية | التمرين المعملي |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
