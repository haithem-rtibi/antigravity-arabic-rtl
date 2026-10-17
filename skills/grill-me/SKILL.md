---
name: grill-me
description: Interrogates the user on plans, architecture, and design decisions using Arabic dialogue with English technical terms in strict RTL and BiDi isolation, supporting both native Unicode RTL Popups and inline Chat modes.
---

# Socratic Architecture & Plan Interrogation (`grill-me`)

Use this skill whenever the user triggers `/grill-me`, asks to be "grilled" on an implementation idea, or wants to stress-test their plan before writing code.

## 1. Interaction Modes: Chat vs. Popup (`Flexible UX`)

The agent supports two complementary interaction modes:
- **Chat Mode (Default & Recommended)**:
  - Questions and discussions are written directly in the chat body, wrapped in:
    `<div dir="rtl" align="right" style="direction: rtl; text-align: right;">...</div>`
  - Recommended for comprehensive architecture debates, edge case analysis, and permanent conversation documentation (`Audit Trail`).
- **Popup Mode (`ask_question` with Unicode RTL Marks)**:
  - When using interactive IDE modals (`ask_question`), **ALWAYS** prefix the `question` string and every entry in `options` with the standard Unicode Right-to-Left Mark character (`\u200F` / RLM).
  - Example:
    - Question: `"\u200Fما هي قاعدة البيانات التي تفضل استخدامها لهذا النظام؟"`
    - Option: `"\u200F(Recommended) استخدام Supabase مع تفعيل سياسات Row Level Security"`
  - This forces the system modal to render Arabic naturally from the right and aligns punctuation (؟, !, .) properly at the end of sentences.

## 2. Strict BiDi Isolation
- Every English technical keyword, framework, library, database table, column, function, command, or parameter MUST be wrapped in backticks (e.g. `Next.js`, `Supabase`, `Row Level Security`, `pnpm test`, `Server Actions`). Never let English characters scramble Arabic sentence order.

## 3. Socratic Interrogation Rules
- **Do NOT propose or write implementation code** during the interrogation phase.
- Ask **2 to 3 sharp, critical questions** per round focused on:
  - Edge cases and failure modes.
  - Database integrity, race conditions, concurrency, and security (RLS, Auth).
  - Component architecture and state management.
  - User experience and loading/error states.
- Present options clearly and challenge any weak assumptions.
- Only when all key decisions are aligned and confirmed by the user, summarize the final architecture and give the green light to proceed with implementation.
