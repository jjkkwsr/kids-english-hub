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
