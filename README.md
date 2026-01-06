# Fake REST API - JSON Server 🚀

مشروع سيرفر وهمي (Fake REST API) مبني باستخدام أداة JSON Server، مصمم لمحاكاة عمليات السيرفر الحقيقي لأغراض التطوير والاختبار.

## 🛠 المتطلبات (Prerequisites)

- يجب التأكد من وجود [Node.js](https://nodejs.org/) مثبت على جهازك

## 🚀 كيفية التشغيل (Getting Started)

### 1. تحميل المشروع
قم بتحميل ملفات المشروع أو عمل clone للمستودع:

```bash
git clone <repository-url>
cd Fake-REST-API---JSON-Server
```

### 2. تثبيت الملحقات
افتح موجه الأوامر (Terminal) في مجلد المشروع ونفذ الأمر التالي:

```bash
npm install
```

### 3. بدء تشغيل السيرفر
لتشغيل السيرفر ومراقبة التغييرات في ملف `db.json`:

```bash
npm start
```

أو استخدم الأمر المباشر:

```bash
npx json-server --watch db.json
```

## 🔗 الروابط المتاحة (Resources)

بمجرد تشغيل السيرفر، يمكنك الوصول إلى البيانات عبر الروابط التالية:

- **الكورسات**: [http://localhost:3000/courses](http://localhost:3000/courses)
- **المستخدمين**: [http://localhost:3000/users](http://localhost:3000/users)

## 📊 هيكل البيانات (Data Structure)

ملف `db.json` يحتوي على البيانات التالية:

```json
{
  "courses": [
    { "id": 1, "title": "Postman" },
    { "id": 2, "title": "Selenium" }
  ],
  "users": [
    { "id": 1, "firstName": "Fahad Alghamdi" }
  ]
}
```

## 📡 العمليات المدعومة (Endpoints)

يمكنك استخدام هذا السيرفر لاختبار جميع عمليات HTTP:

| العملية | الوصف | مثال |
|---------|--------|------|
| `GET` | لجلب البيانات | `GET /courses` |
| `POST` | لإضافة بيانات جديدة | `POST /courses` |
| `PUT` | لتعديل كامل البيانات | `PUT /courses/1` |
| `PATCH` | لتعديل جزئي للبيانات | `PATCH /courses/1` |
| `DELETE` | لحذف البيانات | `DELETE /courses/1` |

### أمثلة الاستخدام:

#### جلب جميع الكورسات:
```bash
GET http://localhost:3000/courses
```

**الاستجابة:**
```json
[
  { "id": 1, "title": "Postman" },
  { "id": 2, "title": "Selenium" }
]
```

#### جلب كورس معين:
```bash
GET http://localhost:3000/courses/1
```

**الاستجابة:**
```json
{ "id": 1, "title": "Postman" }
```

#### إضافة كورس جديد:
```bash
POST http://localhost:3000/courses
Content-Type: application/json

{
  "title": "API Testing"
}
```

#### تعديل كورس:
```bash
PATCH http://localhost:3000/courses/1
Content-Type: application/json

{
  "title": "Advanced Postman"
}
```

#### حذف كورس:
```bash
DELETE http://localhost:3000/courses/1
```

#### جلب جميع المستخدمين:
```bash
GET http://localhost:3000/users
```

**الاستجابة:**
```json
[
  { "id": 1, "firstName": "Fahad Alghamdi" }
]
```

## 📁 هيكل المشروع (Project Structure)

```
Fake-REST-API---JSON-Server/
│
├── db.json           # الملف الذي يحتوي على البيانات المخزنة
├── package.json      # إعدادات وأوامر المشروع
├── package-lock.json # قفل إصدارات الحزم
├── .gitignore        # استثناء ملفات من Git
└── README.md         # ملف التوثيق
```

## 📝 ملاحظات إضافية

- جميع التغييرات على البيانات يتم حفظها تلقائياً في ملف `db.json`
- السيرفر يدعم عمليات الفلترة والترتيب والبحث
- يمكن تخصيص رقم البورت باستخدام: `json-server --watch db.json --port 4000`

### عمليات متقدمة:

#### الفلترة:
```bash
GET http://localhost:3000/courses?title=Postman
```

#### الترتيب:
```bash
GET http://localhost:3000/courses?_sort=title&_order=asc
```

#### البحث:
```bash
GET http://localhost:3000/courses?q=Postman
```

## 🤝 المساهمة (Contributing)

نرحب بأي مساهمات لتحسين المشروع! يمكنك فتح Issue أو إرسال Pull Request.

## 📄 الترخيص (License)

هذا المشروع مفتوح المصدر ومتاح للاستخدام الحر.

