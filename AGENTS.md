# 🤖 AI Agent Custom Behavioral Rules & Guidelines

## 🔄 Lesson 3 Pilot Prototyping Directive (第三課優先試作與驗證規範)

1. **Lesson 3 Pilot First (優先在 Lesson 3 試作驗證)**:
   - When the user requests any design modifications, feature additions, layout tweaks, or content formatting updates for worksheets (**Quizzes**, **Stories**, **Sentence Patterns**, or **Answer Keys**), ALWAYS implement the changes on **Lesson 3 first** as a pilot prototype.
   - Target pilot files:
     - Quiz: `movers/worksheets/quizzes/quiz_03_present_simple_questions_doctor.html`
     - Story: `movers/worksheets/stories/story_03_at_the_doctors.html`
     - Sentence Pattern: `movers/worksheets/sentence_patterns/pattern_03_present_simple_questions_doctor.html`
     - Answer Keys: `movers/worksheets/answer_keys/.../answer_*_03_*.html`

2. **Pause for User Confirmation (暫停並等待使用者確認)**:
   - **DO NOT** apply changes to all lessons on the first try.
   - After completing the Lesson 3 prototype:
     - Summarize the changes concisely.
     - Provide clickable local file links to Lesson 3.
     - Ask the user if the result meets their expectations.

3. **Rollout Phase (核准後推廣至全套課程)**:
   - Only after receiving explicit approval from the user regarding the Lesson 3 prototype should you proceed to update Lesson 1, Lesson 2, and any subsequent lessons.

## 📝 Quiz Worksheet Standard (雙空格與 Part 2 移除新規範)

- **Part 2 Removed (完全移除 Part 2)**: Quiz 卷僅包含選擇題 + 提示求助小站。
- **2-Blank Question Format (雙空格一格文法、一格單字)**:
  - 每題均包含兩個空格 `(1) _____` (測驗文法) 與 `(2) _____` (測驗單字)。
  - 每題提供兩組獨立子選項 (1) 文法選項: A / B / C 與 (2) 單字選項: A / B / C。
- **100% Target Vocab Coverage (100% 單字覆蓋率與動態題數)**:
  - 至少 20 題 (40 格)，若該課單字超過 20 個（例如 Lesson 1 有 21 個單字），自動擴充至 21 題 (42 格)，確保 100% 覆蓋所有目標單字。
- **Scoring (每格 1 分)**:
  - 總分標示為 `Score: ____ / 40` (或依據總格數計算)。
