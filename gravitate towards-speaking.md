---
description: Generate an IELTS Speaking Part 3 interactive study HTML file from a list of questions
---

# IELTS Speaking Study Generator

The user will provide IELTS Speaking Part 3 questions (or any speaking test questions). Generate a fully interactive HTML study file based on the format in `Speaking.html` in this directory.

## Input

The user provides:
- A list of questions (grouped by category/topic, or ungrouped)
- Optionally: a filename for the output

If no filename is given, use `Speaking_[topic].html`.

## Output Format

Generate a single self-contained HTML file with ALL of these features:

### 1. Structure
- Questions organized by category with `<h2>` headings
- Each question in a `<div class="question-card answered" data-theme="[theme]">` with collapsible answer
- Theme tags: work, education, technology, society, lifestyle, city, shopping, environment (pick best fit)

### 2. Answers (for each question, generate THREE versions)
- **Original answer**: Band 8.5-9, ~120-150 words, sophisticated vocabulary, complex structures. Wrap in `<div class="answer"><p>...</p></div>`
- **Easy Version**: Band 8-9, ~60-80 words, simpler vocabulary, shorter sentences, same logical flow. Wrap in `<details class="answer-alt"><summary>Easy Version (Band 8-9)</summary><p>...</p></details>`
- **Conversational Version**: Most natural spoken style with fillers, hedging, self-corrections — how a native speaker would actually talk in a real conversation. Wrap in `<details class="answer-alt"><summary>Conversational Version</summary><p>...</p></details>`

### 3. Answer Pattern (before the answer `<p>`)
Each answer must have a `<details class="answer-pattern" open>` explaining the structure:
```html
<details class="answer-pattern" open>
  <summary>Answer Structure</summary>
  <div class="pattern-step"><span class="pattern-label">1. [Label]:</span> [explanation]</div>
  <div class="pattern-step"><span class="pattern-label">2. [Label]:</span> [explanation]</div>
  ...
  <p><strong>Why scores high:</strong> [explanation]</p>
</details>
```

### 4. Highlighted Vocabulary (in original answer only)
Wrap 6-9 key phrases in:
```html
<span class="highlight" data-tip="phrase|Meaning: explanation.|Example: example sentence.">phrase</span>
```
Choose phrases that are:
- Idiomatic or semi-fixed expressions
- Useful across multiple IELTS topics
- Natural in spoken English (not overly academic)

### 5. Interactive Features (copy from Speaking.html template)
Include ALL of these in the `<style>` and `<script>`:
- **Text-to-speech**: Voice button per question, American English, reads question then answer
- **Sentence-by-sentence mode**: Split into sentences, play/pause/replay each
- **Repeat controls**: Set repeat count, auto-advance to next sentence/question
- **Dark mode toggle**: Full dark theme with localStorage persistence
- **Theme filter tabs**: Clickable pills that show/hide by topic
- **Voice version toggle**: Switch between Original/Easy/Conversational for voice playback
- **Vocabulary tooltips**: Click highlighted words to see meaning + example
- **Vocabulary summary**: Alphabetical list at bottom with search filter
- **Sticky controls bar**: Controls stay at top while scrolling
- **Expand/Collapse all**: Toggle all answers open/closed

### 6. Voice Settings
```javascript
rate: 1.05
pitch: 1.0
lang: 'en-US'
// Prefer voices: Samantha, Alex, or any en-US voice
```

### 7. CSS Essentials
- Clean card-based layout with left border color (blue default, green for answered)
- `.highlight` with yellow background and dotted border
- `.answer-pattern` with blue-tinted background
- `.theme-tag` pills with unique colors per theme
- Dark mode variants for ALL elements
- Responsive design (max-width: 900px)

## Answer Writing Guidelines

When writing answers, follow these IELTS Band 9 principles:
- **Coherence**: Clear logical flow — opinion, reason, example, conclusion
- **Lexical resource**: Use idiomatic language naturally, not forced
- **Grammar range**: Mix simple and complex structures (conditionals, relative clauses, passive voice)
- **Fluency markers**: Use discourse markers (Having said that, On the flip side, I'd argue that)
- **Spoken register**: These are SPEAKING answers — avoid essay language. Use contractions, hedging (I think, I'd say, sort of), and natural pausing phrases

## Template Reference

Use `/Users/huanghong8/Documents/myself/Summary/Speaking.html` as the reference template for:
- Exact CSS styles
- JavaScript functions (speak, openSentenceMode, playFull, filterByTheme, toggleDark, etc.)
- HTML structure and class names
- Tooltip and playback panel markup

Read that file first, then generate the new HTML following the same patterns exactly.

## Execution Steps

1. Read `Speaking.html` to get the full template (CSS + JS)
2. Categorize the user's questions by theme
3. Write Band 9 answers for each question (original + easy + conversational)
4. Add answer patterns and vocabulary highlights to original answers
5. Assemble the full HTML file
6. Write it to the specified filename in this directory
7. Report: number of questions processed, themes used, total vocabulary phrases
