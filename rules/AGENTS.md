# Universal Arabic RTL & BiDi Directionality Rules

> **ALWAYS ACTIVE**: This rule is permanently active across all Antigravity surfaces, sessions, chats, and workspaces (Antigravity 2.0 Desktop, IDE, Chat Canvas, and CLI).

## 1. Universal Language Trigger (Arabic & Arabizi / Latin)
- Whenever the user speaks in:
  - **Arabic script** (العربية الفصحى أو العامية), OR
  - **Arabizi / Franco-Arab in Latin script** (e.g., using numbers 3, 7, 9, 5 such as `bhi`, `kifech`, `3aslema`, `mrigel`, `famech`, `chnowa`, `a3tina`):
- The assistant MUST:
  1. Comprehend the prompt immediately without asking for translation.
  2. In GUI apps, chat canvas, and documentation: Respond in Arabic or Tunisian Arabic, ALWAYS wrapped in strict Right-to-Left (RTL) HTML blocks:
     ```html
     <div dir="rtl" align="right">
     النص العربي هنا...
     </div>
     ```
  3. In CLI / Terminal streams: Prefer clean Tunisian Arabizi or English to avoid non-shaped terminal fonts.

## 2. Strict Right-to-Left (RTL) Paragraph Alignment
- Any Arabic text output (Standard Arabic or Tunisian Arabic) MUST be wrapped in:
  ```html
  <div dir="rtl" align="right">
  النص العربي هنا...
  </div>
  ```
- This ensures:
  - Text lines start at the far right.
  - Periods, question marks (؟), colons (:), and exclamation marks appear at the correct end of the sentence on the left, not at the beginning.

## 3. Bidirectional (BiDi) Isolation for Mixed Languages
- When English, French, or technical keywords appear inside an Arabic sentence:
  - ALWAYS isolate them using code backticks (e.g. `Rust`, `Cargo`, `link.exe`) or `<span dir="ltr">` / `<bdi>`.
  - Example:
    `<div dir="rtl" align="right">قم بتشغيل الأمر `cargo run` لبناء المشروع.</div>`
  - Never allow unescaped Latin text to scramble the order of surrounding Arabic words.

## 4. Code Blocks and Commands
- Code blocks (```rust, ```bash, etc.) must NEVER be RTL.
- Always keep code blocks formatted strictly Left-to-Right (LTR).

## 5. File Generation & Code Comments in Arabic
- **Encoding**: Always generate and save files containing Arabic using standard UTF-8 (without BOM) to prevent mojibake/character corruption.
- **Markdown & Documentation Files (`.md`, `.txt`, `.html`)**:
  - Always wrap Arabic sections with `<div dir="rtl" align="right">` so they render properly in Markdown viewers, GitHub, and browser previews.
- **Source Code Files (`.rs`, `.py`, `.js`, etc.)**:
  - Keep source code logic and identifiers strictly LTR English.
  - When writing Arabic comments, place them on dedicated comment lines (e.g., `// تعليق: دالة تشغيل السيرفر`) so they never disrupt indentation or syntax.
  - Never manually reverse Arabic text inside strings or comments; rely on native Unicode characters.

## 6. Socratic Architecture & Plan Interrogation (`/grill-me`)
- **TRIGGER**: Whenever the user triggers `/grill-me` or asks to interrogate, review, or align on a plan/architecture:
  - You MUST immediately activate and follow the `grill-me` skill.
  - **MANDATORY CHAT MODE**: Conduct the entire interactive dialogue directly inside the chat body. Do NOT use popup modals (`ask_question`), as native IDE modals force LTR alignment and break the Arabic reading flow.
  - **MANDATORY RTL CONTAINER**: Wrap all conversational responses strictly in `<div dir="rtl" align="right" style="direction: rtl; text-align: right;">...</div>`.
  - **MANDATORY BIDI ISOLATION**: Strictly isolate all technical English keywords, frameworks, libraries, file paths, commands, and types with backticks (`...`).
  - **SOCRATIC METHOD**: Do NOT write or propose implementation code immediately. Ask 2 to 3 sharp, critical architectural questions per turn (focusing on edge cases, data invariants, concurrency, security, and UX).
  - Wait for the user to answer and debate before finalizing the plan.




