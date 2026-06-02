---
name: interview-qa-minutes
description: Convert Chinese interview transcripts, meeting recordings, call notes, or rough minutes into formal investment-style Q&A interview memos. Use when the user provides audio transcription text, raw interview dialogue, dinner or casual conversation transcripts that need cleanup, or an additional existing memo that should be checked for omissions and merged into a non-duplicative Q&A version.
---

# Interview Q&A Minutes

## Objective

Transform the user's transcript into a formal Chinese interview memo for investment or industry research use. Preserve original meaning and important factual detail while removing filler, repetition, greetings, meal chatter, and irrelevant small talk.

## Required Output Structure

Use this structure unless the user gives a more specific template:

```text
XXXX访谈纪要
访谈时间：XXXX年XX月XX日
访谈对象：XXX
访谈内容：

一、XXXX
1. Q：
A：

2. Q：
A：

二、XXXX
1. Q：
A：
```

If the transcript does not provide the title, interview date, or interviewee, infer cautiously from context. If unavailable, write `未提供` rather than inventing.

## Output Requirements

By default, return the final memo directly in the chat as Markdown/plain text, preserving the required Q&A structure. Do not create a `.docx` Word document unless the user explicitly asks for Word output, a `.docx` file, or a downloadable/formatted document.

When returning text in chat:

- Use the required title, interview time, interviewee, and `访谈内容` structure.
- Use broad section headings such as `一、业务与商业模式`.
- Bold each question line when using Markdown, e.g. `**1. Q：...**`.
- Keep answers as paragraph-style text unless bullets are clearly more readable.
- Do not mention Word formatting or file generation unless the user asks for it.

When the user explicitly asks for Word output, create a `.docx` and apply these document formatting rules:

- Use 楷体 for the full document.
- Use 小四 font size, equivalent to 12 pt, for the full document.
- Bold every question line, including numbered `Q：` lines. Do not bold answer paragraphs unless the user asks.
- Set paragraph line spacing to 1.5x.
- Set paragraph spacing before to 2x line height, equivalent to 24 pt when using 小四 / 12 pt text.
- Preserve the required Q&A structure in the Word document.

When creating the `.docx`, use a document-generation library or Word-processing workflow that can explicitly set font, size, bolding, and paragraph spacing. If a render/preview workflow is available, inspect the output before delivery.

## Workflow

1. Identify the substantive interview content and discard irrelevant greetings, restaurant ordering, travel logistics, jokes, repeated acknowledgements, and off-topic chatter.
2. Extract all important information, especially data, business model, industry judgment, financial information, competitive landscape, technical details, growth logic, risk points, and policy or reimbursement information.
3. Group the content into 3-4 broad themes. Choose labels from the transcript context, such as `业务与商业模式`, `财务与盈利`, `技术与产品`, `市场与竞争`, `运营与风险`, or `政策与医保`.
4. Convert the content into numbered `Q：/A：` pairs under each theme.
5. Write answers in first person. Do not use third-person attributions such as `杨总表示`, `对方提到`, `受访者认为`, or similar phrases. Use formulations such as `我们目前...`, `我认为...`, `我们看到...`.
6. Preserve the interview feel. Do not rewrite the memo into a summary article.
7. If the user provides another version of minutes, compare it against the transcript or main source, add omitted important information into the Q&A version, and avoid duplicating content already covered.

## Editing Rules

- Keep the original meaning and speaker logic as much as possible.
- Remove filler words, obvious transcription noise, repeated phrases, and casual side comments.
- Do not remove important numbers, assumptions, business mechanics, pricing details, cost structures, margins, capacity, customer information, market size, competitive claims, technical parameters, regulatory details, or risk disclosures.
- Prefer paragraph-style answers. Use bullets only when the answer naturally contains parallel lists or many discrete items.
- Keep answers information-dense and complete; do not compress rich answers into one short sentence.
- When a question is unclear in the transcript, reconstruct a concise question from the answer's topic.
- When one answer covers multiple unrelated topics, split it into separate Q&A pairs under the right themes.
- When multiple transcript fragments answer the same question, merge them into one coherent answer without repeating the same point.
- Maintain a formal internal investment memo tone: precise, restrained, industry-aware, and rich in operational detail.

## Quality Checklist

Before responding, verify:

- The memo has a title, interview time, interviewee, and `访谈内容`.
- Themes are limited to 3-4 unless the content truly requires more.
- Every Q&A pair is numbered within its theme.
- Answers use first-person voice and avoid third-person attribution.
- Important facts from the transcript and any additional memo are retained.
- Meal talk, greetings, and irrelevant chat are removed.
- The result reads like a formal interview memo, not a general article or high-level summary.
- The final output is returned directly in the chat unless Word output was explicitly requested.
- If Word output was explicitly requested, the Word document uses 楷体、小四/12 pt, 1.5x paragraph line spacing, 24 pt paragraph spacing before, and bold question lines.
