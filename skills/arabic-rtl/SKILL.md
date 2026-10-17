---
name: arabic-rtl
description: 🌐 (Arabic RTL) Formats, re-aligns, and handles Arabic text directionality (RTL/LTR), bidirectional text issues, and Tunisian Arabizi transliteration in conversations and documents.
metadata:
  icon: translate
---

# Arabic RTL & Arabizi Helper Skill

Use this skill when the user asks to format Arabic text with proper Right-to-Left (RTL) alignment, fix reversed or disconnected Arabic characters from terminals, or transliterate between Arabic script and Arabizi.

## 1. RTL Markdown Formatting

When the user asks to format an Arabic article, explanation, or response with clean RTL:

1. **Section Containers:**
   Wrap the Arabic content in:
   ```html
   <div dir="rtl" style="text-align: right; direction: rtl;">
   ... Arabic text here ...
   </div>
   ```

2. **Mixed Language Handling (BiDi):**
   - Keep English words, brand names, and code tokens wrapped in backticks (`` `token` ``) or `<span dir="ltr">...</span>`.
   - Ensure numbers and punctuation adhere to the surrounding Arabic flow so sentences don't break awkwardly.

3. **Code Blocks:**
   All code snippets must remain strictly LTR (`dir="ltr"`).

## 2. Reversing Terminal Text / BiDi Repair

If the user provides Arabic text that was printed backwards by a terminal (e.g. `ة ي ب ر ع ل ا`):
- Clean the artificial spacing between characters.
- Reverse the character sequence back to its natural Right-to-Left order (`العربية`).
- Present the reconstructed text clearly to the user.

## 3. Arabizi Conversion

When requested to convert between Arabic and Tunisian Arabizi:
- Use standard North African chat numerals:
  - 2 = ء / أ
  - 3 = ع
  - 5 = خ
  - 7 = ح
  - 8 = غ
  - 9 = ق
- Preserve technical English terms in their original form.
