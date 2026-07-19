# 📐 Kids English Hub - Worksheet Design & Layout Specification

This specification document outlines the standardized design, layout, typography, and pedagogical rules for generating **Quizzes** and **Story Cloze Worksheets** across all current and future levels (**Starters**, **Movers**, and **Flyers**).

---

## 💡 1. Core Design Philosophy

1. **Kid-Friendly & Low Cognitive Load (8-12 Years Old)**:
   - Relaxed spacing, large fonts (17px+), clear contrast, and minimal visual distraction.
   - Eliminate noisy numeric markers inside reading passages.
2. **Black & White Print-Friendly (B&W Ink-Saving)**:
   - **Zero colored or gray background fills** (saves printer ink/toner).
   - Use clean **1px - 2px solid black borders** for cards and **1.5px dashed borders** for Hint and Word Bank boxes.
3. **4-in-1 Skill Integration**:
   - Every lesson combines **Vocabulary**, **Grammar**, **Reading**, and **Speaking** (Read Aloud Tasks).

---

## 📝 2. Quiz Worksheet Specification (`quiz_XX.html`)

### **Structure & Volume**
- **Header**: Name, Date, and Score Box (`Score: ____ / 20`).
- **Part 1: Multiple Choice Questions (20 Questions)**:
  - Covers target Grammar lesson + Vocabulary lesson.
  - Every question includes a **Kid-Friendly Hint (💡 Hint)** written in supportive Traditional Chinese.
- **Part 2: Speaking & Read Aloud Task**:
  - Must cover **100% of all vocabulary words** from the target vocabulary CSV list.
  - Includes a specific grammar task (e.g., *"Circle all Be-verbs / past simple verbs while reading aloud"*).

### **Layout & Typography Rules**
- **Single-Column Relaxed Layout**:
  - DO NOT crowd 20 questions onto a single page. Allow questions to flow naturally across 2–3 pages.
  - Question Card Margin: `margin-bottom: 24px`.
  - Question Text: `font-size: 17px`, `line-height: 1.6`.
  - Checkboxes: Large printable square boxes (`width: 18px; height: 18px; border: 1.5px solid #000`).
  - Option Spacing: `gap: 32px` between options (A, B, C).
  - Page Breaks: Set `page-break-inside: avoid` on each question card to prevent splitting a question across pages.

---

## 🪄 3. Story Cloze Worksheet Specification (`story_XX.html`)

### **Structure & Coverage**
- **Multi-Story Layout**: 3 distinct Cloze Stories per lesson.
- **100% Coverage Rule**: Together, the 3 stories must cover **100% of the target grammar rules and vocabulary words** for that lesson.

### **Word Bank & Blank Formatting**
- **Unique Clue Words Rule (消除多重解答)**:
  - Always include a **unique descriptive clue** before or after noun/adjective blanks (e.g., `a tall hopping _____` for `kangaroo`, `a small black-and-white _____` for `panda`, `a tiny meowing _____` for `kitten`, `a soft white long-eared _____` for `rabbit`).
  - Ensures every blank has **100% unique, 1-to-1 unambiguous alignment** with the Word Bank.
- **Word & Grammar Bank Position**:
  - Place a **Word & Grammar Bank Box** directly ON TOP of each story block (`border: 1.5px dashed #000`).
  - Kids pick candidate words from the top box and write directly into the story blanks.
- **Clean Reading (No Number Noise)**:
  - **DO NOT include numeric markers** (e.g., `(1)`, `(2)`) inside the story text blanks or questions.
  - Use clean, wide underlined blanks (`<span class="blank-line"></span>` or `____________`).
  - **Reason**: Numeric markers interrupt fluent reading when kids perform Read Aloud practice.

---

## 🖨️ 4. B&W Print CSS Template Standard

All `.html` worksheets must adhere to the following print-optimized CSS standard:

```css
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Noto+Sans+TC:wght@400;500;700&display=swap');

body {
    font-family: 'Fredoka', 'Noto Sans TC', sans-serif;
    color: #111827;
    background-color: #ffffff; /* Pure white for ink saving */
    margin: 0;
    padding: 20px;
}

.paper {
    background: #ffffff;
    width: 210mm;
    min-height: 297mm;
    padding: 20mm 18mm;
    box-sizing: border-box;
}

/* Header */
.quiz-header {
    border-bottom: 2px solid #000000;
    padding-bottom: 12px;
    margin-bottom: 24px;
}

/* Question Cards & Story Blocks */
.question-card, .story-block {
    background: #ffffff;
    border: 1.5px solid #000000;
    border-radius: 8px;
    padding: 16px 20px;
    margin-bottom: 24px;
    page-break-inside: avoid;
}

/* Top Word Bank Box (Stories) */
.word-bank-box {
    border: 1.5px dashed #000000;
    border-radius: 8px;
    padding: 10px 14px;
    margin-bottom: 16px;
    background: #ffffff;
}

/* Kid-Friendly Hint Box (Quizzes) */
.hint-box {
    background: #ffffff;
    border: 1.5px dashed #4b5563;
    border-radius: 6px;
    padding: 8px 12px;
    font-size: 13.55px;
    color: #1f2937;
}

/* Printable Checkbox */
.checkbox {
    width: 18px;
    height: 18px;
    border: 1.5px solid #000000;
    border-radius: 3px;
    background: #ffffff;
    display: inline-block;
}

/* Print Rules */
@media print {
    body { background: #ffffff; padding: 0; }
    .paper { box-shadow: none; width: 100%; padding: 0; }
}
```

---

## 📂 5. File Location Reference

- **Design Spec File**: `kids-english-hub/WORKSHEET_DESIGN_SPEC.md`
- **Quiz Reference**: `kids-english-hub/movers/worksheets/quizzes/quiz_01_be_verbs_toy_shop.html`
- **Story Reference**: `kids-english-hub/movers/worksheets/stories/story_01_magic_toy_shop.html`
