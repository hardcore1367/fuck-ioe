# Repository Instructions for Exam Notes and Flashcards

## Purpose

This repository contains exam-focused IOE study notes and flashcards. Work on one chapter and one output file at a time. The goal is material that is easy to understand, efficient to revise, and complete enough to earn strong marks when written in an exam.

These instructions apply throughout the repository unless a more specific `AGENTS.md` exists in a subject directory.

## Sources and priority

For each subject, use these sources in this order:

1. `imp.md` or `IMP.md` is the required exam scope and past-paper frequency guide.
2. `syllabus.md` defines the official course boundaries and topic names.
3. The existing chapter note is the text that must be preserved while auditing.

Apply the following rules:

- Never omit a topic listed in `imp.md`, regardless of its frequency.
- Include supporting concepts that are necessary to understand or answer an `imp.md` topic properly, even when those supporting concepts are not listed separately.
- A syllabus topic that has no presence in `imp.md` may be omitted from new content when it is not needed by an important topic.
- Do not delete existing material merely because it has zero frequency in `imp.md`.
- Do not edit `imp.md` or `syllabus.md` unless the user explicitly asks.
- Do not invent frequencies, marks, repeated questions, or syllabus requirements.

## Work sequence

When creating or correcting a chapter:

1. Read the complete relevant section of `syllabus.md`.
2. Read the complete relevant chapter section, warnings, repeated-question notes, and chapter summary in `imp.md`.
3. Read the entire existing chapter note. A blank file means all required topics are missing.
4. Perform and report the gap analysis before editing the chapter file.
5. Correct heading structure and add only the missing or incomplete content.
6. Review the final note against every applicable `imp.md` topic.
7. Create flashcards only after the note itself is complete, and only when requested.

Do not create or revise the note and its flashcards simultaneously unless the user explicitly asks for both.

## Gap analysis

Before changing a note, compare every topic in the relevant `imp.md` frequency table with the existing note. Also check which syllabus topics have no exam frequency.

Report these findings in plain language before editing:

- **Missing:** required topics with no meaningful coverage.
- **Incomplete:** required topics that lack an exam-worthy definition, explanation, steps, comparison, formula, example, or diagram requested by past papers.
- **Already covered:** required topics that need no new prose.
- **Skipped syllabus-only topics:** syllabus items absent from `imp.md` and unnecessary for understanding an important topic.
- **Heading fixes:** headings whose level or number must change.

If nothing is missing, say so clearly. In that case, change only the headings that violate the required structure.

## Preserve existing writing

When auditing an existing note:

- Do not rewrite, rephrase, shorten, expand, or reorder existing prose.
- Do not alter existing sentences merely to improve their style.
- Do not silently correct a factual claim by rewriting it; report the concern unless the user explicitly authorizes corrections.
- Preserve existing tables, formulas, examples, image links, and callouts.
- The only permitted changes to existing headings are their Markdown level and numbering prefix. Preserve the heading title words.
- Add new prose only for gaps identified before editing.
- Insert new material at the logically correct location rather than appending unrelated sections at the end.

## Heading and filename structure

Name a chapter note as:

```text
{chapter number}. {Topic Name}.md
```

Examples:

- `1. Introduction.md`
- `2.1 Distributed Objects.md`
- `2.2 Distributed File System.md`

Use one document title followed by numbered sections:

```markdown
# 5. Time and State in Distributed Systems

## 1. Time in Distributed Systems

### 1.1 Physical Clocks

### 1.2 Logical Clocks

#### 1.2.1 Lamport's Logical Clock

## 2. Causal Ordering of Messages

### 2.1 Causal Order
```

Rules:

- Use exactly one `#` document title containing the chapter number and topic name.
- Use `## 1.`, `## 2.`, `## 3.`, and so on for top-level sections inside the chapter.
- Use `### 1.1`, `### 1.2`, and so on for subsections under `## 1.`.
- Use `### 2.1`, `### 2.2`, and so on for subsections under `## 2.`.
- Every child heading must carry its complete parent number.
- Never use a bare child number such as `### 1.` or `### 2.`.
- If deeper levels are genuinely needed, continue the full hierarchy, such as `#### 1.2.1`.
- Do not skip heading levels.
- While fixing an existing heading, change only its level or number; keep its title text unchanged.

## Writing new note content

New content must be simple, clear, and exam-worthy. It should be neither a vague collection of tiny points nor an unnecessarily long textbook essay.

- Start a topic with a precise definition when appropriate.
- Explain how or why something works, not only what it is called.
- Give enough detail to answer the likely marks and wording shown in `imp.md`.
- Give high-frequency and repeatedly asked topics fuller treatment than low-frequency short-note topics.
- Use complete, meaningful sentences. Avoid unsupported fragments such as “fast,” “secure,” or “scalable” without explaining them.
- For lists, prefer a bold key term followed by a short explanation.
- Group related features, functions, advantages, disadvantages, requirements, and applications under clear headings.
- Use numbered steps for mechanisms, algorithms, procedures, and working processes.
- Use Markdown tables for comparisons when they make differences easier to reproduce in an exam.
- Use LaTeX/KaTeX for formulas and define every symbol needed to use the formula.
- Include a small example when it materially improves an exam answer.
- Stay within the subject scope. Add prerequisite context only when it is needed for an `imp.md` topic.
- Do not add a summary, encouragement, transition paragraph, or meta-commentary.

Use Markdown wherever it improves readability: headings, lists, tables, blockquotes, fenced blocks, emphasis, formulas, and existing images. Do not use decorative formatting that adds no study value.

## Diagrams and images

Preserve any useful image already present in the notes. When an exam-worthy diagram would help but no image is available, do not invent a URL. Insert a callout at the correct location using this form:

```markdown
> [!NOTE]
> Insert a diagram of **Lamport's logical clock** here. It should show the processes, events, message arrows, and timestamp updates.
```

The callout must name the exact diagram and the important labels or components it should contain. Prefer diagrams that a student can reproduce by hand in an exam.

## Final note checks

Before finishing a chapter note, verify all of the following:

- Every topic in the relevant `imp.md` section is covered.
- Any prerequisite needed by an important topic is present.
- No unnecessary syllabus-only topic was newly added.
- Existing prose was not rewritten or deleted.
- Added material corresponds exactly to a reported gap.
- Heading levels and parent-child numbers are consistent.
- Definitions, mechanisms, comparisons, formulas, and requested diagrams have enough detail for an exam answer.
- Only one chapter note file was created or changed.

## Flashcard creation

Create flashcards from the completed chapter note, not directly from `imp.md` or `syllabus.md`. First understand the whole topic, then distill it into balanced active-recall cards.

### Card design

- Use normal question-and-answer cards only.
- Do not use cloze deletion, Anki syntax, multiple-choice questions, or app-specific formatting.
- Prefer one card per logical concept.
- Do not create a separate card for every tiny fact or sentence.
- Avoid cards whose answers require memorizing an entire long paragraph.
- Group closely related features, functions, steps, types, applications, advantages, or disadvantages when they naturally form one answer.
- Split a sentence into separate cards only when it contains independent concepts that should be recalled independently.
- Preserve all exam-important information while removing unnecessary textbook wording.
- Keep answers concise but complete enough that their meaning is unambiguous.
- Test recall with direct questions such as “What is...?”, “How does... work?”, “Why...?”, “List...”, “Compare...”, or “What are the steps...?”.
- Include definitions, formulas, functions, comparisons, mechanisms, algorithms, examples, and diagram-related concepts when present in the note.
- Use Markdown, bullets, tables, fenced blocks, and LaTeX inside strings only when they improve clarity.
- Reuse an image only when it already appears in the note and is genuinely useful for recall.
- Create enough cards to cover the note well, but prioritize retention-to-review-time ratio over card count.

### Deduplication

After drafting the complete deck, review every card again:

- Remove duplicate and near-duplicate questions.
- If two cards test the same idea, merge them or keep the clearer one.
- If the same fact appears in a definition, feature list, and comparison, keep the card that tests it best.
- Do not repeat the same answer in several cards unless the contexts are meaningfully different.

### Flashcard file and JSON format

Use the established location for that subject. Otherwise place the deck beside the chapter note and use the same chapter number, for example `5.json` or `2.1.json`.

The file must be a top-level JSON array containing only `question` and `answer` strings:

```json
[
  {
    "question": "What is TCP?",
    "answer": "TCP is a **connection-oriented transport-layer protocol** that provides reliable data delivery."
  },
  {
    "question": "What are the main features of TCP?",
    "answer": "- Connection-oriented\n- Reliable delivery\n- Flow control\n- Error checking"
  }
]
```

JSON requirements:

- Escape line breaks inside strings as `\n`.
- Escape quotation marks and backslashes correctly.
- Do not use trailing commas, comments, or raw control characters.
- Do not add fields other than `question` and `answer`.
- Validate the completed deck with `jq empty <file>` before finishing.
- Return only a JSON code block when the user asks for flashcard content in chat instead of a repository edit.

## Final response behavior

- Work on one requested file per response unless the user explicitly broadens the scope.
- For a note, always report the gap analysis before producing or editing the file.
- State exactly which missing content and heading fixes were added and why.
- If no content was missing, state that only heading fixes were made.
- Do not claim completion until the Markdown or JSON validation checks have passed.
