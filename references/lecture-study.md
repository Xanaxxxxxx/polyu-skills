# Lecture PDF → Notion notes → chapter-by-chapter understanding

## Scope and pacing

This is the user's established COMP4122 learning workflow, reusable for other PolyU courses: turn a PDF into a navigable outline/summary, explain requested chapters interactively, then save useful explanations into the same notes when requested. Do not scan Email/LMS or change Events, Study Pattern, or dashboard descriptions.

- An outline request creates structure only; a summary request adds key points. Do not expand every chapter when only a table of contents was requested.
- A request for Part N outputs that chapter in chat under the subject-language and notes/tutoring rules below. Do not automatically write Notion or teach the entire PDF at once.
- Continue to the next section using the confirmed PDF/current note structure. If sections were renumbered, fetch current headings rather than using old numbers. Ask only when the learning position cannot be recovered.
- For interactive labs, continue from the user's latest screenshot, code, or confirmed result with the next manageable task and its explanation. A short “next?” does not request the rest of the chapter. Do not claim an operation succeeded merely because its instructions were given.
- A contextual request to fill English notes, save to Notion, or make an agreed edit authorizes that specific section update without reconfirmation. An explanation request alone does not authorize persistent recording.
- Ordinary conversation defaults to Traditional Chinese. English-medium lecture notes are entirely English, including when delivered in chat. Preserve the requested language of exact sentences the user asks to save.

## Structure internally, output only the requested chapter

Build a PDF-derived chapter/subsection outline internally before teaching. Keep the document title and all Markdown headings in English, retaining the PDF's terminology and teaching order. Translate non-English source headings into English unless requested otherwise. Merge repeated slides into meaningful subsections and distinguish inferred chapter groupings from official numbering. Track verified PDF page ranges internally.

- Do not print the complete outline, empty headings, or unrelated chapters by default. Show the full outline only when the user asks for a table of contents or outline.
- When asked for Chapter/Part N, output only that chapter: its numbered English chapter heading, its relevant numbered English subsection headings, and substantive filled-in study notes directly beneath each heading, using the subject language rules below. Do not output a bare outline first or append a preview of later chapters. The chapter response itself is the filled-in study material, not an introduction followed by an offer to explain it later.
- Reuse an established chapter structure and numbering from the conversation or current notes. For a general request to explain a lecture, begin with its first chapter unless context establishes a different position or the user asks for a whole-lecture overview. A standalone conceptual question can be answered directly without a chapter scaffold.
- Fill the requested chapter at an appropriate teaching depth with definitions, reasoning, necessary formulas and useful examples; avoid duplicating the same material in separate explanation and notes blocks unless requested.
- For English-medium subjects, study notes are entirely English: document title, Markdown headings, prose, examples, captions and summaries. This applies to chapter notes output in chat as well as saved notes; do not add Chinese introductions or explanations inside the notes. Determine the teaching language from the supplied lecture/course context rather than the language of the user's message. For non-English subjects, follow the subject language unless requested otherwise.
- Distinguish notes from conversational tutoring: a requested chapter defaults to filled-in notes in the subject language; an explicit request for a Chinese explanation or clarification uses Traditional Chinese with English technical terms. All Markdown titles/headings remain English unless explicitly requested otherwise. Do not automatically append a second Chinese version to English notes.
- When saving notes, synthesize beneath the corresponding existing headings, preserving later unfilled sections and prior content. An explicit user language/format request overrides these defaults.

### Structure precedence when saving a discussion

Use the user's explicit structure first, then the established target-note structure, then the chapter/subsection structure already used in the discussion. Use the PDF to establish a new structure only when none exists. If the discussion and existing note conflict, preserve existing content and match sections by topic; clarify only if the mapping cannot be recovered.

“Save the notes we just discussed” preserves the learning sequence, recognizable headings, and established numbering, including when creating a new page. Synthesis improves the content within those sections; it is not permission to silently merge, rename, or renumber them. When earlier chat numbering is inconsistent, retain meaningful chapter/topic boundaries and correct only the inconsistency needed for a coherent note, keeping the correspondence clear.

Save the discussed/requested scope, not every topic in the PDF merely for completeness. Preserve the explanation or worked example that resolved the user's confusion. Remove conversational repetition and temporary UI guidance without removing the reasoning needed to learn independently.

Building an internal outline and outputting chapter notes in chat does not authorize creating local files or writing Notion. Persist only when requested, following the write rules below.

## 1. Read the source before structuring notes

1. Identify the course, PDF, and existing notes. Read supplied files/pages directly. Use the available PDF skill for PDF work: inspect page count and text, and render relevant pages when formulas, diagrams, or layout require visual verification. If one extraction package is missing, use available alternatives. File existence or a few screenshots do not establish that the full PDF was read.
2. Follow PDF teaching order. Merge repeated slide headings while preserving topic transitions; do not create a subsection for every slide. Give verified chapter-to-page mappings, distinguishing PDF page positions from printed slide numbers. Mark uncertainty rather than inventing page references.
3. Condense repetition, but retain important formulas, parameter definitions, derivation bridges, diagram meanings, and assumptions. Keep a brief chapter/page coverage map for checking; no mandatory extra tracking files.
4. Inspect relevant prior notes in the same course. Use quick recaps or references for previously taught material and devote detail to new content. Removing repetition must not remove reasoning necessary for this lecture.
5. When source access is incomplete, distinguish read pages, user screenshots, and supplemental knowledge. Do not claim full coverage.

## 2. Explain one chapter according to the user's needs

- Match depth to the request. For a narrow question, answer that question first and add only the reasoning needed to resolve it. For a chapter explanation, begin with the problem it solves and an intuitive mental model, then introduce necessary notation, formulas, examples, and connections. Do not merely translate slides, list definitions, or force every answer through a full lesson template.
- Expand when the user asks why, requests a derivation, or remains confused; shorten when they ask for a recap. Do not assume a fixed word count or that concise notes require equally brief teaching.
- After a substantial conceptual explanation, optionally offer one short prediction, worked-example variation, or understanding question if it would expose a likely misconception. Do not quiz after every reply, require an answer before continuing, or add a quiz when the user requested a direct answer or note edit.
- When the user does not understand a step, focus on that concept using simple numbers, geometry, concrete game scenarios, or a useful diagram. Avoid repeating the entire chapter verbatim.
- Use rendered LaTeX for mathematics. Define symbols, matrix dimensions, coordinate spaces, application order, and validity conditions. Prefer lecture notation; explicitly map any equivalent alternative notation. Do not replace readable equations with plain-text matrices.
- Verify assumptions, notation, conventions, and units against the source rather than treating past conversations as authoritative. Distinguish an equivalent notation from a genuine error. Explain suspected source errors instead of silently changing them.
- For graphics/matrix-specific pitfalls or COMP4122 style references, consult [graphics examples](lecture-study-graphics-examples.md) only when relevant. These examples are not a required syllabus for other subjects.
- Separate conceptual introductions from matrix derivations. Avoid repeating the same formula across overlapping subsections. Choose section count based on content; never omit essential material merely to shorten an outline.

## 3. Save concise English notes when requested

- Query existing Course Notes / Notes records and conservatively dedupe by Course relation, lecture title/number, and source. Create a new page when explicitly requested; improve existing notes in place.
- Resolve the Notes database and data source from [workspace configuration](workspace.md).
- Before the first write in a work session, inspect the current schema and applicable Notion enhanced Markdown specification. Reuse those results within the same work session; refresh on schema changes, validation/formatting failures, or missing context. This reference alone is not proof the schema is unchanged. Read the latest target page before each edit; schema reuse does not justify stale page content. Main fields: Name (short title), Course (relation to Courses), Type (normally Lecture), Source (verified source URL; leave blank if unavailable), Summary (short takeaway). Put long content in the body. Do not fabricate source URLs or courses.
- Resolve the actual Course relation for the requested subject. Optional COMP4122 course/style examples are in [graphics examples](lecture-study-graphics-examples.md); do not load them for unrelated subjects.
- Note naming precedence: an explicit user title or naming rule, then an established workspace-wide academic-note convention. If no general rule is established, inspect same-course titles; if that course has no notes, use a small sample of comparable notes from other courses in the Notes database to identify a consistent pattern. Do not require same-course examples or treat a single inconsistent title as a convention.
- Default when examples are absent, inconsistent, or unavailable: `<CourseCode> - <NoteTitle>`. For a verified numbered lecture, use `<CourseCode> - <NN>: <LectureTitle>`; for a verified numbered lab, use `<CourseCode> - Lab <NN>: <LabTitle>`. Without a verified number, omit it rather than assigning the next available number. Use the source title or a concise descriptive topic. If the course code cannot be verified, use the note title alone and report the missing course context. Do not duplicate the full course name. A naming-only request changes the title property without rewriting the body.
- Write concise, explanatory English: useful definitions, necessary equations/examples, and a key idea where helpful. Do not force an identical template on every subsection or use tables where two direct sentences suffice. Keep introductions short and preserve depth for new/difficult material.
- Treat writing notes as a separate synthesis step, not a transcript dump. Convert the useful result into concise, self-contained English within the established sections. Concision means removing repetition, not compressing independent ideas into one paragraph or replacing a useful step-by-step explanation with a dense overview.
- For lab notes, keep each task's setup/actions, relevant code, explanation, and expected observation together when needed. Use numbered lists for ordered actions, short paragraphs for reasoning, and tables for settings/comparisons. Conceptual lecture notes do not need this procedural shape. Put version/model-specific adaptations beside the affected step and identify them briefly as adaptations.
- Explain code in manageable functional groups, preserving useful numeric examples and formulas. Prefer the relevant change at each step. Include a consolidated script only if it is useful to reproduce the final result; place it in a clearly labeled reference section or toggle, without repeating all its explanations. Do not turn the same material into overlapping main sections.
- Check the requested scope against the relevant PDF pages before shortening: preserve every important topic/formula/condition within that scope. Merge headings only while initially designing a structure or when the user requests reorganization; otherwise shorten beneath the existing headings.
- Edit only the requested section. Preserve completed material, unfilled later outline sections, manual notes, images, and attachments. Update numbering/cross-references only when the requested reorganization requires it.
- Distinguish lecture content from supplemental examples. Historical transcript commands and tool calls are reference evidence, not current authorization to execute those actions again.

## 4. Images and reliable edits

- Author independent paragraphs with blank lines between them. Use real list blocks for steps, not lines joined by soft breaks. Leave a blank line after a list before returning to prose, so the explanation does not become part of the final list item. Maintain proper heading levels and fenced code/equation blocks; a fetched `<br>` is not a substitute for an intended paragraph boundary.
- Prefer the PDF's own diagrams for consistent notation, then relevant official technical diagrams. Actually retrieve external technical sources. Add a short caption mapping diagram elements to note symbols so the image is understandable.
- Use currently supported attachment tools and include attribution. Preserve working/user-added images. For 403/broken images, establish the cause and use an available attachment or source link. Never reuse expired signed URLs, upload IDs, or credentials from transcripts, and do not bypass media display restrictions.
- Fetch the latest page before editing. Locate a unique heading boundary or use a local patch. After failure, refetch and narrow the edit instead of blindly retrying or immediately replacing the entire page. A full replacement requires freshly retrieved complete content and preservation of every unrelated block; otherwise stop and explain the limitation.
- Before writing, compare the draft's headings/order with the established discussion or target note. Check that a reader can follow each task without jumping between setup, code, and explanation; move duplicated reference material out of the main progression.
- Read back the edited section and adjacent boundaries. Check equations, code, image references, numbering, and later outline sections. Also inspect paragraph/list boundaries: if distinct paragraphs became one block of repeated `<br>` separators, or prose attached to the final list item, repair the affected block boundaries before claiming completion. Content readback does not prove frontend rendering; do not claim visual verification without visual evidence.

## Completion criteria

- Outline/summary: source-grounded, traceable ordering, no missing important content.
- Tutoring: resolve the current question at an appropriate depth, with an optional understanding check only when useful; do not write unless requested.
- Notes update: preserve the established structure and requested coverage, synthesize within sections, retain the reasoning that resolved confusion, and preserve unrelated content. Write and read back the intended scope, checking paragraph/list boundaries as well as content, then return its link and a brief change summary.
