# Universal Arabic RTL & BiDi Directionality Rules

These rules apply across all Antigravity surfaces (Antigravity 2.0 Desktop, IDE, Chat Canvas, and CLI):

## 1. Strict Right-to-Left (RTL) Paragraph Alignment
- Whenever writing Arabic text (Standard Arabic or Tunisian Arabic), the output MUST be wrapped in RTL HTML blocks so the UI renders it starting from right to left:
  ```html
  <div dir="rtl" align="right">
  النص العربي هنا...
  </div>
  ```
- This ensures that:
  - Text lines start at the far right.
  - Periods, question marks (؟), colons (:), and exclamation marks appear at the correct end of the sentence on the left, not at the beginning.

## 2. Bidirectional (BiDi) Isolation for Mixed Languages
- When English, French, or technical keywords appear inside an Arabic sentence:
  - ALWAYS isolate them using code backticks (e.g. `Rust`, `Cargo`, `link.exe`) or `<span dir="ltr">` / `<bdi>`.
  - Example:
    `<div dir="rtl" align="right">قم بتشغيل الأمر `cargo run` لبناء المشروع.</div>`
  - Never allow unescaped Latin text to scramble the order of surrounding Arabic words.

## 3. Code Blocks and Commands
- Code blocks (```rust, ```bash, etc.) must NEVER be RTL.
- Always keep code blocks formatted strictly Left-to-Right (LTR).

## 4. File Generation & Code Comments in Arabic
- **Encoding**: Always generate and save files containing Arabic using standard UTF-8 (without BOM) to prevent mojibake/character corruption.
- **Markdown & Documentation Files (`.md`, `.txt`, `.html`)**:
  - Always wrap Arabic sections with `<div dir="rtl" align="right">` so they render properly in Markdown viewers, GitHub, and browser previews.
- **Source Code Files (`.rs`, `.py`, `.js`, etc.)**:
  - Keep source code logic and identifiers strictly LTR English.
  - When writing Arabic comments, place them on dedicated comment lines (e.g., `// تعليق: دالة تشغيل السيرفر`) so they never disrupt indentation or syntax.
  - Never manually reverse Arabic text inside strings or comments; rely on native Unicode characters.

## 5. Dialect & Context Comprehension
- Understand both Modern Standard Arabic (فصحى) and colloquial dialects seamlessly, especially Tunisian Arabic and Arabizi (North African chat alphabet with numerals like 3, 7, 9, 5).
- Accurately grasp technical slang and mixed French/English terms (e.g. `cash`, `cont`, `mrigla`, `famech`, `behi`).
- **Surface Awareness**:
  - In GUI apps & Markdown files: Output pristine RTL Arabic script.
  - In CLI / Terminal streams: Prefer Tunisian Arabizi or Latin script so the terminal cannot display broken/reversed characters.
