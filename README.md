# 🌐 Antigravity Arabic RTL & BiDi Assistant Plugin

> **Official plugin for Google Antigravity (CLI, IDE, and Antigravity 2.0)** to provide native Right-to-Left (RTL) Arabic alignment, bidirectional text isolation (BiDi), and terminal readability.

---

## 📖 نظرة عامة (Overview)

هذه الإضافة (Plugin) مخصصة لمنصة **Google Antigravity** لمعالجة كافة مشاكل اللغة العربية في المحادثات والأكواد:
1. **محاذاة كاملة من اليمين لليسار (RTL):** ترتيب طبيعي للنصوص وعلامات الترقيم (النقاط والاستفهام في آخر الجملة على اليسار).
2. **عزل الكلمات الأجنبية والأكواد (BiDi Isolation):** دمج الكلمات الإنجليزية والفرنسية وأسماء المتغيرات والأوامر التقنية (`Rust`, `cargo`, `link.exe`) داخل الجملة العربية دون أن تنعكس أو تتداخل الكلمات.
3. **حماية التيرمينال (Terminal Readability):** منع ظهور الحروف العربية المعكوسة أو المقطعة في شاشات الـ CLI.
4. **دعم التونسي بالـ Arabizi:** إمكانية الترجمة والتحويل السلس.

---

## ⚡ طريقة التنصيب (Installation)

بإمكان أي مستخدم تنصيب هذه الإضافة مباشرة عبر أمر واحد في التيرمينال:

```bash
agy plugin install https://github.com/<YOUR-USERNAME>/antigravity-arabic-rtl
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
