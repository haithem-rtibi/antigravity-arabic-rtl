# 🌐 Antigravity Arabic RTL & BiDi Assistant Plugin

> **Official plugin for Google Antigravity (CLI, IDE, and Antigravity 2.0)** to provide native Right-to-Left (RTL) Arabic alignment, bidirectional text isolation (BiDi), and clean documentation outputs.

---

## 🔗 روابط هامة (Quick Links)

* 📦 **المستودع الرسمي (Source Code):** [haithem-rtibi/antigravity-arabic-rtl](https://github.com/haithem-rtibi/antigravity-arabic-rtl)
* ⭐ **ادعم المشروع بنجمة (Give a Star):** إذا ساعدتك الإضافة، اضغط على زر Star في أعلى صفحة GitHub تشجيعاً للمشروع!
* 🐛 **الإبلاغ عن المشاكل (Report Issues):** [فتح تذكرة على GitHub](https://github.com/haithem-rtibi/antigravity-arabic-rtl/issues)
* 💡 **اقتراح ميزات جديدة (Feature Requests):** بإمكانك فتح تذكرة لاقتراح أي تحسينات في التنسيق أو اللهجات.
* 📜 **الترخيص:** [رخصة MIT مفتوحة المصدر](https://github.com/haithem-rtibi/antigravity-arabic-rtl/blob/main/LICENSE)

---

## 📖 نظرة عامة (Overview)

هذه الإضافة (Plugin) مخصصة لمنصة **Google Antigravity** لضبط وتنسيق اللغة العربية في المحادثات، الملفات، والمخرجات التقنية:

### 1. محاذاة كاملة من اليمين لليسار (RTL):
* في **Antigravity 2.0** و **IDE**: تظهر النصوص العربية في المحادثة منسقة طبيعياً من اليمين لليسار.
* في **ملفات الـ Markdown (`.md`) والـ Artifacts والـ PDF**: يتم توليد كود الـ Markdown مغلّفاً بوسوم الـ RTL (`dir="rtl"`) ليكون التقرير جاهزاً للقراءة والطباعة بأعلى جودة.

### 2. عزل الكلمات الأجنبية والأكواد (BiDi Isolation):
* عزل المصطلحات التقنية والأكواد (`Rust`, `cargo`, `link.exe`, etc.) داخل الجمل العربية دون تداخل أو انقلاب الكلمات.

### 3. توضيح هام بخصوص الـ CLI (Terminal):
* شاشات الـ Terminal في أنظمة التشغيل (PowerShell, CMD, Bash) لا تدعم محرك ربط الحروف العربية (BiDi Shaping)، لذلك لا يمكن إظهار الحروف العربية متصلة داخل نافذة الـ Terminal نفسها.
* **حل الإضافة للـ CLI:** 
  1. يتواصل معك الـ CLI بالـ **Arabizi التونسي** أو الإنجليزية لتفادي الحروف المعكوسة في شاشة التيرمينال.
  2. عند طلب كتابة مقال أو كود أو تقرير، يقوم الـ CLI بتوليد **ملف خارجي (`.md` أو `.pdf` أو Artifact)** منسق 100% بنظام الـ RTL لتفتحه في المتصفح أو المحرر بشكل مثالي.

### 4. دعم شامل لكافة الناطقين بالعربية واللهجات (Universal Arabic Coverage):
* 🌍 **اللغة العربية الفصحى (Modern Standard Arabic):** الإضافة مصممة وموجهة لجميع المطورين العرب في مختلف أنحاء العالم (الشرق الأوسط، الخليج، وشمال إفريقيا) لضمان اتساق النصوص والأكواد الرسمية.
* 🗣️ **اللهجات المحكية وشات المعرب (Regional Dialects & Arabizi):** فهم ذكي للهجات العربية المتنوعة، مع دعم متقدم وخاص للدارجة التونسية والـ Arabizi في بيئات الـ Terminal.

---

## ⚡ طريقة التنصيب (Installation)

بإمكانك تنصيب الإضافة واستخدامها بعدة طرق سهلة وسريعة:

### 1. عبر الـ Agent مباشرة (Prompt & Go - الطريقة الأسهل):
انسخ هذا الأمر والصقه مباشرة في شات **Antigravity**:
```text
Install and activate the Arabic RTL & BiDi plugin from: https://github.com/haithem-rtibi/antigravity-arabic-rtl
```
سيتكفل الـ Agent تلقائياً بتنزيل الحزمة، تفعيلها في مسار الإضافات الخاص بجهازك، وتطبيق قواعد الـ RTL على الفور.

### 2. عبر أمر الـ CLI في التيرمينال:
```bash
agy plugin install https://github.com/haithem-rtibi/antigravity-arabic-rtl
```

### 3. عبر واجهة الـ CLI التفاعلية:
1. اكتب الأمر: `/plugin`
2. انتقل إلى تبويب **Discover**
3. اختر **Install from local directory** أو أدخل رابط الـ GitHub.

---

## 📢 الشفافية وحالة المتجر (Marketplace Status & Transparency)

> ℹ️ **حالة المراجعة الرسمية:**  
> تم تقديم الإضافة رسمياً إلى فريق مراجعة **Google Antigravity Marketplace** عبر استمارة اعتماد الإضافات الرسمية، وهي حالياً **قيد المراجعة والفهرسة (Under Review)** من قِبل مهندسي Google لإدراجها في المتجر العام بضغطة زر واحدة.  
> خلال فترة المراجعة، الإضافة **جاهزة، مستقرة 100%، ومتاحة للتنصيب المباشر** لجميع المطورين عبر رابط هذا المستودع.

---

## 📁 هيكلية المشروع (Project Structure)

```text
antigravity-arabic-rtl/
├── plugin.json                # معرّف الإضافة وإعداداتها
├── README.md                  # دليل الاستخدام والتنصيب
├── LICENSE                    # رخصة مفتوحة المصدر (MIT)
├── assets/
│   └── logo.jpg               # شعار الإضافة الرسمي
├── rules/
│   └── AGENTS.md              # قواعد التوجيه التلقائي للذكاء الاصطناعي
└── skills/
    └── arabic-rtl/
        └── SKILL.md           # مهارة معالجة وتنسيق النصوص (/arabic-rtl)
```

---

## 📜 الترخيص (License)
هذا المشروع مفتوح المصدر تحت رخصة [MIT License](LICENSE).
