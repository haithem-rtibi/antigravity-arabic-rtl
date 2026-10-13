# 🌐 Antigravity Arabic RTL & BiDi Assistant Plugin

<p align="center">
  <img src="assets/logo.jpg" alt="Antigravity Arabic RTL Logo" width="160" style="border-radius: 24px;" />
</p>

<p align="center">
  <a href="https://github.com/haithem-rtibi/antigravity-arabic-rtl"><img src="https://img.shields.io/badge/GitHub-Repository-blue?logo=github&style=flat-square" alt="GitHub Repo"></a>
  <a href="https://github.com/haithem-rtibi/antigravity-arabic-rtl/stargazers"><img src="https://img.shields.io/github/stars/haithem-rtibi/antigravity-arabic-rtl?style=flat-square&color=gold" alt="GitHub Stars"></a>
  <a href="https://github.com/haithem-rtibi/antigravity-arabic-rtl/issues"><img src="https://img.shields.io/github/issues/haithem-rtibi/antigravity-arabic-rtl?style=flat-square&color=brightgreen" alt="GitHub Issues"></a>
  <a href="https://github.com/haithem-rtibi/antigravity-arabic-rtl/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-green.svg?style=flat-square" alt="License: MIT"></a>
</p>

> **Official plugin for Google Antigravity (CLI, IDE, and Antigravity 2.0)** to provide native Right-to-Left (RTL) Arabic alignment, bidirectional text isolation (BiDi), and clean documentation outputs.

---

## 🔗 روابط هامة (Quick Links)

* 📦 **المستودع الرسمي (Source Code):** [https://github.com/haithem-rtibi/antigravity-arabic-rtl](https://github.com/haithem-rtibi/antigravity-arabic-rtl)
* ⭐ **ادعم المشروع بنجمة (Give a Star):** إذا ساعدتك الإضافة، اضغط على زر Star في أعلى صفحة GitHub تشجيعاً للمشروع!
* 🐛 **الإبلاغ عن المشاكل (Report Issues):** [https://github.com/haithem-rtibi/antigravity-arabic-rtl/issues](https://github.com/haithem-rtibi/antigravity-arabic-rtl/issues)
* 💡 **اقتراح ميزات جديدة (Feature Requests):** بإمكانك فتح Issue جديدة لاقتراح أي تحسينات في التنسيق أو اللهجات.

---

## 📖 نظرة عامة (Overview)

هذه الإضافة (Plugin) مخصصة لمنصة **Google Antigravity** لضبط وتنسيق اللغة العربية في المحادثات، الملفات، والمخرجات التقنية:

1. **محاذاة كاملة من اليمين لليسار (RTL في الملفات والـ UI):**
   * في **Antigravity 2.0** و **IDE**: تظهر النصوص العربية في المحادثة منسقة طبيعياً من اليمين لليسار.
   * في **ملفات الـ Markdown (`.md`) والـ Artifacts والـ PDF**: يتم توليد كود الـ Markdown مغلّفاً بوسوم الـ RTL (`dir="rtl"`) ليكون التقرير جاهزاً للقراءة والطباعة بأعلى جودة.
2. **عزل الكلمات الأجنبية والأكواد (BiDi Isolation):**
   * عزل المصطلحات التقنية والأكواد (`Rust`, `cargo`, `link.exe`, etc.) داخل الجمل العربية دون تداخل أو انقلاب الكلمات.
3. **توضيح هام بخصوص الـ CLI (Terminal):**
   * شاشات الـ Terminal في أنظمة التشغيل (PowerShell, CMD, Bash) لا تدعم محرك ربط الحروف العربية (BiDi Shaping)، لذلك لا يمكن إظهار الحروف العربية متصلة داخل نافذة الـ Terminal نفسها.
   * **حل الإضافة للـ CLI:** 
     1. يتواصل معك الـ CLI بالـ **Arabizi التونسي** أو الإنجليزية لتفادي الحروف المعكوسة في شاشة التيرمينال.
     2. عند طلب كتابة مقال أو كود أو تقرير، يقوم الـ CLI بتوليد **ملف خارجي (`.md` أو `.pdf` أو Artifact)** منسق 100% بنظام الـ RTL لتفتحه في المتصفح أو المحرر بشكل مثالي.

---

## ⚡ طريقة التنصيب (Installation)

بإمكان أي مستخدم تنصيب هذه الإضافة مباشرة عبر أمر واحد في التيرمينال:

```bash
agy plugin install https://github.com/haithem-rtibi/antigravity-arabic-rtl
```

أو من داخل واجهة الـ CLI التفاعلية:
1. اكتب الأمر: `/plugin`
2. انتقل إلى تبويب **Discover**
3. اختر **Install from local directory** أو أدخل رابط الـ GitHub.

---

## 📁 هيكلية المشروع (Project Structure)

```text
antigravity-arabic-rtl/
├── plugin.json                # معرّف الإضافة وإعداداتها
├── README.md                  # دليل الاستخدام والتنصيب
├── LICENSE                    # رخصة مفتوحة المصدر (MIT)
├── rules/
│   └── AGENTS.md              # قواعد التوجيه التلقائي للذكاء الاصطناعي
└── skills/
    └── arabic-rtl/
        └── SKILL.md           # مهارة معالجة وتنسيق النصوص (/arabic-rtl)
```

---

## 📜 الترخيص (License)
هذا المشروع مفتوح المصدر تحت رخصة [MIT License](LICENSE).
