---
layout: post_ar
title: "تعلم البرمجة بلغة بايثون - الدرس الثامن: أنواع البيانات في بايثون وتحويلها"
date: 2020-04-04
categories: [دورة-تعلم-البرمجة-بلغة-بايثون] 
tags: [بايثون, برمجة, لغات-برمجة, تعلم-البرمجة, البرمجة-للمبتدئين, تعلم-البرمجة-بالعربي]
postlang: arabic 
permalink: "/ar/:year/learn-programming-with-python-1-8-arabic"
sharing-img: "/assets/images/2020/pyc-8-1.png"
---

![تعلم البرمجة بلغة بايثون - الدرس الثامن: أنواع البيانات في بايثون وتحويلها](/assets/images/2020/pyc-8-1.png)

في هذا الدرس سنتعرف على أنواع البيانات في بايثون وسنرى أمثلة على كل نوع ثم سنتعلم كيفية تحويل البيانات من نوع إلى آخر وفائدة هذا التحويل.

## أنواع البيانات (Data Types)

في بايثون هناك ثلاثة أنواع رئيسية للبيانات والمتغيرات: 

- رقم صحيح (Integer) مثل `2` 
- رقم عشري (Floating-point Number) مثل `3.5`
- سلسلة نصية (String) مثل `"نص"`

بايثون تعرف الفرق بين هذه الأنواع. مثلاً العامل `+` إذا تم استخدامه بين رقمين سيقوم بعملية الجمع بينما إذا تم استخدامه بين سلسلتين نصيتين سيقوم بدمجهما معاً كما يلي:

```python
>>> dd = 1 + 8
>>> print(dd)
9
>>> ee = 'hello ' + 'Ahmad'
>>> print(ee)
hello Ahmad
```

لكن ماذا لو استخدمت `+` بين سلسلة نصية وعدد كما في المثال التالي:

```python
>>> gg = 'hello ' + 'Ahmad'
>>> gg = gg + 1
```

في هذه الحالة بايثون لن تستطيع تنفيذ هذا الأمر وستظهر رسالة خطأ:

![رسالة خطأ من بايثون](/assets/images/2020/pyc-8-2.png)

تخبرك رسالة الخطأ بنوع الخطأ وفي أي سطر وقع وتخبرك بسبب الخطأ. في هذه الحالة السبب يقول أنه يمكن دمج سلسلة نصية مع سلسلة نصية أخرى فقط وليس مع عدد.

بايثون توفر لنا دالة (function) اسمها `type()` تمكننا من معرفة نوع البيانات كما في المثال التالي:

```python
>>> type(1234)
int
>>> type('ammar')
str
>>> type(11.44)
float
>>> x = 'text'
>>> type(x)
str
```

فكما ترى في السطر الأول نضع عدداً صحيحاً فتخبرنا بايثون أن نوعه `int` وهي اختصار كلمة Integer وتعني عدد صحيح. في السطر الثاني نضع سلسلة نصية فتخبرنا بايثون أن نوعها `str` وهي اختصار كلمة String وتعني سلسلة نصية. في السر الثالث نضع عدداً عشرياً (أي فيه فاصلة عشرية) فتخبرنا بايثون أن نوعه `float` اختصاراً لـ Floating-point وتعني الفاصلة العائمة وهي طريقة تمثيل الأعداد العشرية في الحاسب.

نرى أيضاً أنه يمكننا باستخدام هذه الدالة معرفة نوع المتغير حيث قمنا بتعريف متغير اسمه `x` ووضعنا سلسلة نصية بداخله ثم عرفنا باستخدام الدالة أن نوعه `str`. 

### تحويل أنواع البيانات (Data-Type Conversion)

توفر بايثون لنا دوالاً تمكننا من تحويل نوع البيانات، فمثلاً يمكننا تحويل عدد صحيح إلى عشري أو العكس:

```python
>>> x = 3
>>> float(x)
3.0
>>> y = 4.5
>>> int(y)
4
```

في السطر الأول قمنا بتعريف متغير اسمه `x` ووضعنا فيه العدد الصحيح `3`؛ في هذه الحالة فإن نوع `x` سيكون `int`. ثم في السطر الثاني قمنا بتحويل نوع المتغير إلى `float` باستخدام الدالة المسماة `float()` ونرى أن الناتج هو `3.0`. صحيح أن `3` يساوي في الحقيقة `3.0` لكن نوعهما مختلفان بالنسبة لبايثون: عندما تضيف الفاصلة العشرية لرقم يصبح نوعه `float`. 

في السطر الثالث قمنا بتعريف متغير اسمه `y` ووضعنا فيه عدداً عشرياً قيمته `4.5` وهذا سيجعل `y` من نوع `float`. في السطر الرابع قمنا بتحويل نوع هذا المتغير إلى عدد صحيح `int` باستخدام الدالة المسماة `int()` وكان ناتج التحويل `4` حيث أن دالة `int()` تقوم بأخذ الرقم الذي على يسار الفاصلة العشرية وتترك ما على يمينها.

أيضاً يمكننا استخدام الدوال `int()` و `float()` لتحويل السلاسل النصية إلى أرقام. لماذا قد نحتاج لذلك؟ لأنه في الكثير من الأحيان عندما تستقبل برامجنا بيانات من مصادر خارجية مثل الانترنت - كما سنرى لاحقاً - فإن هذه البيانات تأتي على شكل سلاسل نصية حتى لو كانت في حقيقتها تعبر عن أرقام. مثلاً:

```python
>>> str_val = "123"
>>> type(str_val)
str
>>> print(str_val + 3)
```

في السطر الأول نعرف متغيراً اسمه `str_val` ونضع فيه سلسلة نصية هي `"123"`. لاحظ أن السلسلة تحوي أرقاماً ولكن بايثون تعاملها كنص كما تعامل `"abc"` بالضبط. لدلك عندما نحاول جمع هذه السلسلة النصية والرقم `3` في السطر الأخير فإن بايثون ستخبرنا بأن خطأ وقع يشبه الخطأ الذي رأيناه في الأعلى.فبايثون لا تكترث إذا كانت السلسلة النصية تحتوي أرقاماً أو أحرفاً؛ المهم أنها سلسلة نصية، فعندما تحاول جمع رقم مع سلسلة نصية فإن بايثون ستواجه خطأ في التنفيذ.

لذلك إذا أردنا التعامل مع الرقم الموجود في هذه السلسلة النصية كرقم وليس كنص فعلينا استخدام الدالة `int()` لتحويل هذه السلسلة إلى رقم صحيح كالتالي:

```python
>>> int_val = int(str_val)
>>> type(int_val)
int
>>> print(int_val + 3)
126
```

في السطر الأول حولنا السلسلة النصية إلى عدد صحيح ثم في السطر الأخير أضفنا `3` إليه وكان الناتج `126`.

لكن هناك أمر يجب التنبه له وهو أنه يجب أن تحتوي السلسلة النصية فقط على رقم حتى تستطيع تحويل نوعها باستخدام `int()` أو `float()`. في المثال التالي نقوم بمحاولة تحويل سلسلة نصية إلى رقم:

```python
es = 'hello'
es = int(es)
```

عندما تقوم بايثون بتنفيذ السطر الثاني فستواجه خطأ لأن السلسلة `es` لا تحتوي على أرقام.

### ملاحظات

عندما تجمع عدد صحيح وعدد عشري في بايثون فإن الناتج سيكون عدداً عشرياً:

```python
>>> 123 + 45.2
168.2
```

## فيديو الدرس
