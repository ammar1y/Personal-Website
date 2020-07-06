---
layout: post_ar
title: "تعلم البرمجة بلغة بايثون #21: الحلقات في بايثون | Loops in Python: for Loop"
date: 2020-07-01
categories: [دورة-تعلم-البرمجة-بلغة-بايثون] 
tags: [بايثون, برمجة, لغات-برمجة, تعلم-البرمجة, البرمجة-للمبتدئين, تعلم-البرمجة-بالعربي]
postlang: arabic 
permalink: "/ar/:year/learn-programming-with-python-1-21-arabic"
sharing-img: "/assets/images/2020/pyc-21-1.png"
---

![تعلم البرمجة بلغة بايثون #21"](/assets/images/2020/pyc-21-1.png)

في هذا الدرس سنكمل حديثنا عن الحلقات في بايثون ونتحدث عن حلقة for.

## حلقة for

تعرفنا سابقاً على حلقة `while` ورأينا أنها تتكرر طالما بقي شرطها متحققاً. الآن سنتعرف على حلقة `for` وهي نوع آخر من الحلقات تتكرر لعدد محدد (معروف مسبقاً) من المرات.

لنر المثال التالي عن حلقة `for`:

```python
for i in [1,2,4,5,7]:
  print(i)
print('انتهى')
```

في هذه الحلقة سيتم تكرار تعليمات الحلقة لكل عنصر في هذه القائمة: `[1,2,4,5,7]`. هذا يعني أن أمر الطباعة هذا:

```python
print(i)
```

سيتم تنفيذه مرة لكل عنصر في تلك القائمة، وفي كل مرة ستكون قيمة `i` نفس قيمة ذلك العنصر. يعني أنه في المرة الأولى لتكرار الحلقة سيتم طباعة "1" وهو العنصر الأول في القائمة؛ في التكرار الثاني سيتم طباعة "2" والذي هو العنصر الثاني في القائمة، وهكذا حتى نصل إلى العنصر الأخير وهو "7" حيث ستتم طباعته ثم تنتهي الحلقة ويتم الخروج منها إلى الأمر الذي بعدها وهو أمر الطباعة الذي سيطبع كلمة "انتهى".

في هذا المثال اخترنا أن يكون اسم متغير الحلقة `i` لكن يمكن أن نختار أي اسم نريده. 

في المثال التالي سنمر على قائمة تحتوي على سلاسل نصية:

```python
for f in ['Ahmad', 'Leen', 'John']:
  print('Happy birthday ' + f)
```

هذا البرنامج سيمر على عناصر هذه القائمة وسيطبع لكل عنصر عبارة تهنئة. في البداية سيمر على "Ahmad" وبالتالي ستكون قيمة المتغير `f` تساوي "أحمد" وسينفذ الأوامر داخل الحلقة. هناك أمر واحد، أمر الطباعة، فسينفذه ويطبع:

```
Happy birthday Ahmad
```

ثم سيمر على بقية العناصر ويطبع جملاً مشابهة:

```
Happy birthday Leen
Happy birthday John
```

### تحليل حلقة `for`

لننظر إلى المثال التالي:

```python
for w in [1,3,4,7,3]:
  print(w)
```

عرفنا من دراستنا لحلقة `for` أن هذا البرنامج سيمر على عناصر القائمة ويطبعها على الشاشة. هذا البرنامج مكافئ للبرنامج التالي الذي سنكتبه بدون استخدام حلقة `for`:

```python
w = 1
print(w)
w = 3
print(w)
w = 4
print(w)
w = 7
print(w)
w = 3
print(w)
```

هذا يشابه ما تفعله حلقة `for`: تمر على كل عنصر، وتجعل متغير الحلقة يحمل قيمة ذلك العنصر، ثم تنفذ التعليمات داخل الحلقة.

ملاحظة: `break` و `continue` تعمل مع حلقة `for` مثلما تعمل مع حلقة `while`.

ملاحظة: رأينا في هذا الدرس شيئاً جديداً هو القوائم. سنتعرف عليها بالتفصيل في المستقبل.

## فيديو الدرس

<iframe width="560" height="315" src="https://www.youtube.com/embed/d2YJSuQUqlM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
