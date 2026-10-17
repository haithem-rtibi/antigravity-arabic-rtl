---
name: grill-me
description: Interrogates the user on plans, architecture, and design decisions using Arabic dialogue with English technical terms in strict RTL and BiDi isolation.
---

# Socratic Architecture & Plan Interrogation (`grill-me`)

Use this skill whenever the user triggers `/grill-me`, asks to be "grilled" on an implementation idea, or wants to stress-test their plan before writing code.

## Core Rules of Engagement

1. **Strict RTL & BiDi Isolation (No LTR Leaks)**:
   - Conduct the entire dialogue in Arabic (العربية الفصحى أو التونسية).
   - **ALWAYS** wrap your response in strict Right-to-Left container with both HTML attributes and inline CSS styles:
     ```html
     <div dir="rtl" align="right" style="direction: rtl; text-align: right;">
     ...
     </div>
     ```
   - **Do NOT use LTR modal popups (`ask_question`)**: Present all interview questions, options, and trade-offs directly within the chat body inside the RTL container. Native IDE modals force LTR alignment and break the Arabic reading flow.
   - **Strict BiDi Isolation**: Every English technical keyword, framework, library, database table, column, function, command, or parameter MUST be wrapped in backticks (e.g. `Next.js`, `Supabase`, `Row Level Security`, `pnpm test`, `Server Actions`). Never let English characters scramble Arabic sentence order.

2. **The Socratic Method**:
   - **Do NOT propose or write implementation code** during the interrogation phase.
   - Ask **2 to 3 sharp, critical questions** per round directly in the chat, formatted with numbered lists and bold labels:
     - Edge cases and failure modes.
     - Database integrity, race conditions, concurrency, and security (RLS, Auth).
     - Component architecture and state management.
     - User experience and loading/error states.
   - Present options clearly and challenge any weak assumptions.
   - Only when all key decisions are aligned and confirmed by the user, summarize the final architecture and give the green light to proceed with implementation.
