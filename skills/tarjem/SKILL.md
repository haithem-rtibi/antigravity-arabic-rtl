---
name: tarjem
description: (Arabic RTL) Contextual inline translator for code, words, and sentences into Arabic or Tunisian Arabizi with strict RTL formatting. Ideal for inline commands (Ctrl+I) and chat.
---

# Contextual Arabic & Arabizi Translator (`/tarjem`)

Use this skill whenever the user invokes `/tarjem`, `/translate`, asks to translate a phrase, sentence, or code snippet into Arabic or Tunisian Arabizi, or triggers an inline command (<kbd>Ctrl</kbd>+<kbd>I</kbd> / <kbd>Cmd</kbd>+<kbd>I</kbd>) on selected text in the editor.

## 1. Inline Command (`Ctrl+I` / `Cmd+I`) Mode

When invoked as an inline command on selected text in an editor file:
- **Direct & Concise**: Output the translation immediately without conversational chatter or pleasantries.
- **Code & Comments**:
  - For code comments, docstrings, or markdown docs: translate the explanation accurately into clear technical Arabic or Tunisian Arabizi.
  - **Preserve Identifiers**: Keep variable names, function signatures, types, APIs, and syntax tokens strictly in their original English/code form.
- **Dual Representation**:
  When asked to translate a sentence or paragraph, provide both options if helpful:
  1. **اللغة العربية الفصحى (Modern Standard Arabic)**: واضحة، دقيقة ومحايدة تقنياً.
  2. **الدارجة التونسية (Tunisian Arabizi / Arabic)**: بأسلوب عفوي ودقيق باستخدام أرقام المعرب (`3`, `7`, `9`, `5`).

## 2. Chat Canvas Formatting

When invoked inside the conversation chat:
- Always wrap Arabic output in a strict RTL container:
  ```html
  <div dir="rtl" align="right" style="direction: rtl; text-align: right;">
  ... الترجمة هنا ...
  </div>
  ```
- **Strict BiDi Isolation**:
  Always isolate English words, code keywords, parameters, and paths with backticks (e.g. `const`, `endpoint`, `token`).
