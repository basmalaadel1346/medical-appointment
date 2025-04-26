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

```bash
Doctor doctors[MAX_DOCTORS] = {
    {"Dr. Smith", "Cardiologist",
     {
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"},
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"},
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"},
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"},
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"},
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"},
         {"10:00 AM - 10:30 AM", "11:00 AM - 11:30 AM", "12:00 PM - 12:30 PM", "02:00 PM - 02:30 PM", "03:00 PM - 03:30 PM"}
     },
     {{0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}}
    },

    {"Dr. Alice", "Dermatologist",
     {
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"},
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"},
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"},
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"},
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"},
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"},
         {"09:00 AM - 09:30 AM", "10:30 AM - 11:00 AM", "12:30 PM - 01:00 PM", "01:30 PM - 02:00 PM", "03:30 PM - 04:00 PM"}
     },
     {{0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}}
    },

    {"Dr. John", "Pediatrician",
     {
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"},
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"},
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"},
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"},
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"},
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"},
         {"09:15 AM - 09:45 AM", "10:15 AM - 10:45 AM", "11:45 AM - 12:15 PM", "01:00 PM - 01:30 PM", "02:30 PM - 03:00 PM"}
     },
     {{0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}, {0, 0, 0, 0, 0}}
    }
};

```

👀This code defines and initializes an array of doctors — specifically, an array named doctors, with a size of MAX_DOCTORS. |    
هذا الكود يقوم بتعريف وتهيئة 
array من الأطباء 



```bash
void loadAppointments() {
    FILE *file = fopen(FILE_NAME, "rb");
    if (!file) return;

    Appointment appt;
    while (fread(&appt, sizeof(Appointment), 1, file)) {
        for (int i = 0; i < MAX_DOCTORS; i++) {
            if (strcmp(doctors[i].name, appt.doctorName) == 0) {
                int dayIndex = -1;
                const char *days[MAX_DAYS] = {"Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"};

                for (int j = 0; j < MAX_DAYS; j++) {
                    if (strcmp(appt.appointmentDay, days[j]) == 0) {
                        dayIndex = j;
                        break;
                    }
                }

                if (dayIndex != -1) {
                    for (int t = 0; t < MAX_TIME_PERIODS; t++) {
                        if (strcmp(appt.appointmentTime, doctors[i].availableTimes[dayIndex][t]) == 0) {
                            doctors[i].isTimeBooked[dayIndex][t] = 1;
                        }
                    }
                }
            }
        }
    }
    fclose(file);
}
```

This code defines a function named loadAppointments() that reads appointments from a binary file and updates the booking status for the corresponding doctor and time 

 1) pointers .
 2) address-of operator
 3) fread
 4) file save
 5) fwrite
