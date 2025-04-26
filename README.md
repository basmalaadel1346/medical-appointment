# medical-appointment

medical-appointment
## Why use define 
```bash
#define MAX_DOCTORS 3
#define MAX_DAYS 7
#define MAX_TIME_PERIODS 5
#define FILE_NAME "appointments.txt"  
```

### Explanation:

1) used to create constants -> replace every occurrence of that name with the value you gave it.  
تُستُعمل لإنشاء ثوابت:  
يتم استبدال كل ظهور للاسم الذي قمت بتعريفه بالقيمة التي أعطيتها له.

#### Why use #define instead of writing numbers/strings directly?

أسهل في التحديث:  
إذا أردت تغيير الحد الأقصى لعدد الأطباء من 3 إلى 5، كل ما عليك فعله هو تعديل القيمة مرة واحدة عند تعريف `#define` بدلاً من تعديلها في كل مكان داخل الكود.


## لماذا نستخدم struct في لغة C؟
struct تُستخدم لجمع عدة أنواع بيانات مختلفة تحت نوع واحد 
بمعنى آخر، بدلاً من أن يكون عندك متغير منفصل لكل خاصية (اسم الطبيب، تخصصه، أوقات توافره...)، يمكنك تجميعهم كلهم في هيكل واحد.

تنظيم البيانات: يسمح لك بتنظيم المعلومات المرتبطة معًا بطريقة واضحة.

tutorial at youtube :👀
```bash
https://youtu.be/0fAbic9frEc?si=CD2-kUycV31rseKZ
```
