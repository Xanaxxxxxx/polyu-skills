# PolyU synchronization policy

Prepare PolyU Daily Brief for a PolyU Computing undergraduate. Full-run instructions below apply to Daily Brief; targeted synchronization remains limited by SKILL.md.

## Sources and canonical state

- Search Gmail with high recall for all new PolyU-related messages from the past 24 hours.
- Use profile `canvas-polyu-edu-hk` and timezone `Asia/Hong_Kong` for a fresh Canvas/Blackboard overview covering the next 21 days. Read Canvas courses, announcements, Planner assignments, and Calendar, plus available Blackboard courses, announcements, to-do items, and calendars. This is bounded evidence collection, not a complete account export.
- Notion PolyU Events is the sole event-level canonical command state and deduplication source:
  - Resolve the database, data source and preferred read-only locator from [workspace configuration](workspace.md).
- Notion Date is the sole canonical time field. Notion Calendar/calendar views are presentation layers.
- Never read, create, update, delete, or synchronize Google Calendar events; never use Google Calendar for deduplication. Do not mention its non-use in the database description.
- Gmail, Canvas, and Blackboard are original evidence; Notion stores structured facts, states, dates, and source links. Only local lms-cli manages LMS credentials; never put them in Notion, prompts, or output.
- Do not mark Gmail read or reply to messages.

## LMS access and authorization

- Canvas/Blackboard are read-only: no submissions, exam starts, messages, grade changes, marking platform content, or other remote changes.
- On AUTH_REQUIRED, use the isolated school sign-in/MFA flow. Never request, copy, or record passwords, MFA codes, tokens, or cookies. Until authorization completes, report a gap and do not perform writes based on unverified LMS evidence; LMS itself remains read-only. Never substitute guesses or stale information for fresh results.
- Blackboard to-do or other individual tool failures are gaps, not proof of no tasks. Continue other successful sources.

## PolyU relevance

Relevant senders contain @polyu.edu.hk or @connect.polyu.hk; display names/body explicitly mention PolyU, 香港理工大學, 理大, or The Hong Kong Polytechnic University; or messages come from PolyU units such as Academic Registry, CPEO, AAE, UHS, uhnotice, RiFood, FS, LST, RIAIoT, ISE, RICRI, School of Nursing, Student Halls, COMP, or CUS. Do not use Gmail's Important label to determine importance.

## What belongs in Notion

- Always important: subject registration/add-drop/timetables; exams/quizzes/assignments/projects; fees/payments/refunds; enrolment/cancellation/no-add-drop warnings; official Academic Registry deadlines; myPolyU/eStudent/Connect setup; hall application deadlines; scholarships/internships/exchanges/CAR/non-local activities with deadlines; official academic calendar items including congregation, Info Day, general holidays, teaching suspension, revision days, exam periods, term starts/ends, and assessment result dates.
- Seminars/workshops/competitions qualify only if at least one applies: registration deadline; Computing/AI/career/course relevance; user decision to attend needed; fixed time and plausible user attendance.
- Usually ignore general research recruitment, generic sustainability/GreenCoins/welcome promotions, unrelated department seminars, pure newsletters, or promotions without deadlines/actions and without direct relevance to a Computing undergraduate. Mention only under the ignore section; create no row.
- Clearly actionable/state-changing items with unknown dates may be recorded and flagged as missing information. Do not guess dates, venues, or actions.
- Do not create non-PolyU or non-academic items.
- Always create/update Events for unfinished Canvas Planner assignments/quizzes/exams/projects with explicit deadlines.
- Create/update announcement-based Events only for explicit fixed dates, deadlines, cancellation/rescheduling, registration, team formation, required completion, or other direct actions. General materials notifications, welcomes, and undated generic reminders are not automatically Events.
- Do not infer dates from ambiguous relative time, incomplete deadlines, group-specific arrangements, or alternative sessions. Do not treat alternatives as all mandatory. A missing-information item may have blank time.
- New official LMS corrections update existing source facts, retaining old sources in the body and preserving user notes. Use only successfully read, confirmed, actionable Blackboard evidence.

## Deduplication and updates

- Query actual PolyU Events records first on every sync; it is the sole event-level dedupe source.
- Match Canvas assignments by exact Canvas ID `courseId:assignmentId`; announcements without assignment IDs use `courseId:announcementId`. Update matches rather than creating rows. Never put Blackboard/Gmail identifiers in Canvas ID.
- Match Canvas announcements/other LMS items by source URL or courseId:announcementId first; otherwise conservatively compare Course relation + event name + date range.
- Before Gmail-based creation, match Gmail link, source subject, normalized event name, and date range. Update existing events.
- Merge Gmail/LMS evidence for the same event into one row, retaining both source links and history.
- One email may produce multiple events sharing its link, but each row's name/date/type combination must distinguish the event.
- Academic Calendar 2026/27 has already been imported. Update matching sources or name/date records; do not reimport duplicates.
- Preserve manually set My State. Only new rows default to Not started.

## Events schema

- Name: title.
- Type: Assignment, Quiz, Exam, Project, Registration, Application, Subject, Fee, Seminar, Workshop, Competition, Admin, Event, Resource, Recruitment. This is classification, not progress.
- My State: Not started, In progress, Almost done, Done, Skip. This is the sole manual decision/progress state.
- Course: relation to the Courses data source in [workspace configuration](workspace.md), never a text course code. Use an existing course relation whenever found. Create missing courses only when authoritative email/LMS evidence meets the Courses rules below.
- Write only Date for canonical dates; Day, Time, Countdown, and Priority are read-only formulas/projections.
- Where an end date/time exists, write Date start and end. Use start alone only for genuine single-day deadlines/date-only FYIs.
- Treat any remaining Google Calendar property as deprecated; do not write it.
- Do not recreate Next Action, Todo, old Status, Calendar Sync, Apple Reminder, Last Seen, Priority Signal, or Priority Score.

## Source content in page bodies

- Email-created or substantively updated items must contain these exact headings in order:
  1. `### 中文說明`: explain/translate facts, dates, venue, required actions, deadlines, and relevance in Chinese.
  2. `### Email body snapshot`: preserve the original email body and hyperlinks.
- LMS-created or substantively updated items must contain `### 中文說明`, original Canvas/Blackboard link, platform, source ID, and a source summary or announcement quotation. Never fabricate an email snapshot.
- Use normal Markdown headings, paragraphs, bullets, or necessary tables. No toggles/details, whole-email code blocks, or forced Source Email/Overview headings.
- Preserve manual Notes, My State, non-source content, and user additions. Change source facts only when new evidence explicitly corrects dates, titles, scores, requirements, or links.

## Event icons and colors

- Every Events page should have a Notion page icon; do not prefix Name with emoji.
- Use built-in `calendar-week`. Type is the sole color source; match its existing select-option color.
- Mapping: Assignment=red; Quiz=orange; Exam=red; Project=pink; Registration=brown; Application=yellow; Subject=brown; Fee=red; Seminar=green; Workshop=green; Competition=pink; Admin=default; Event=default; Resource=gray; Recruitment=yellow.
- Set the icon/color during new-page creation. For updates, add an icon if absent; preserve nonstandard custom icons. If authoritative evidence changes Type, change icon color only for an automation-managed calendar-week icon.
- Icons are presentation metadata, unrelated to canonical state, Date, Type, My State, Priority, or dedupe. Audits/backfills fill missing icons only; do not rewrite identical icons.

## Events database description

- At the end of each full Daily Brief, update the Events data-source description.
- Use only `Last checked: MMM D, h:mm A`, for example `Last checked: Oct 24, 8:00 AM`: exact capitalization, English three-letter month, unpadded day and 12-hour hour, two-digit minutes, uppercase AM/PM, and no trailing punctuation.
- Use the actual Daily Brief check time in Asia/Hong_Kong, not the scheduled run time. Do not advance it for a description-only formatting change or an unsuccessful brief; an explicitly user-supplied display timestamp may be applied as requested.
- Do not add a year, timezone label, event summary, data gaps, or ignored-item summary. Keep those details in the brief itself.

## Courses synchronization

- Courses is canonical at course level:
  - Resolve its database and data source from [workspace configuration](workspace.md).
- For authoritative email/LMS evidence about registration, waitlists, enrolment, cancellation, timetables, components, offerings, or explicit subject codes, query Courses first. Dedupe by normalized subject code, Source Gmail, source LMS URL/course ID, and course name. Events remains the sole event-level dedupe source; Courses the sole course-level source.
- Explicit evidence of a new course, successful registration, waitlist, cancellation, withdrawal, component/offering change updates existing rows; create only if missing. Multiple messages/LMS items must not create duplicate courses.
- Write only explicit source facts. Allowed fields: Name, Code, Component, Credits, Offered In 2026/27, Offering Source, Registration Source, Source Gmail, Notes. Do not infer Requirement, Stream, semester, or other unstated facts from codes.
- If only a subject code is known, use it as Name and document missing information in Notes. Do not invent names, credits, components, semesters, or requirements.
- Preserve manual My Course State; new courses default to Not started. Registration Source classifies evidence, not progress. A successful waitlist registration may retain Waitlist with successful registration explained in Notes.
- Email-based creation/substantive updates use 中文說明 then Email body snapshot. LMS-based changes use 中文說明, platform, source URL/ID, and summary; no fabricated email snapshot.
- After matching/creating a course, directly related Events must use its Course relation, never a text code.

## Study Pattern synchronization

- Study Pattern is canonical at semester level:
  - Resolve its database and data source from [workspace configuration](workspace.md).
- Keep only five Period rows: Sem 1, Sem 2, Summer Sem, Sem 3, Sem 4; one row per Academic Year + Period. No Programme-wide row or separate elective-slot/requirement rows.
- Schema: Name, Academic Year, Period, Open Requirements, Required Subjects, Training Credits, My Study State, Courses relation, Credits rollup, Fulfilled formula, Source Gmail, Notes.
- Credits is a read-only sum of Courses.Credits; Fulfilled is a read-only formula. Never overwrite either.
- For Sem 1/2/3/4, Fulfilled requires actual related-course count >= Required Subjects AND empty Open Requirements. Summer Sem uses manual My Study State = Done because WIE may lack a subject code. Never invent a WIE Course.
- Required Subjects counts only requirements representable as real subjects. Never fabricate courses for GE Essential or other non-subject components to meet counts. Baselines: Sem 1=5, Sem 2=6, Sem 3=5, Sem 4=5; change only on explicit authoritative study-pattern changes.
- Link only actual courses with genuine subject codes. Fixed/selected/allocated/successfully registered subjects require explicit authoritative support. Unconfirmed COMP Elective, CAR, Service Learning, WIE, GE Essential, Language, or LCR remain in Open Requirements.
- Remove an open requirement only when a confirmed specific Course relation satisfies it. Preserve uncertain requirements even when the course count is sufficient.
- On new authoritative study-pattern/programme requirements, query and dedupe by Academic Year + Period, updating existing rows. Programme-wide rules belong in relevant semester Notes/Open Requirements, not a new row.
- Write only explicit PolyU source facts. Unknown dates, credits, subject mappings, placements, or actions remain blank and are reported as unknown. Do not guess semester allocations from annual credit totals.
- Preserve manual My Study State; new rows default to Not started.
- Courses.Study Pattern is the reverse relation. Events.Course links only real Courses, never Study Pattern rows.
- Email-based creation/substantive updates use 中文說明 then Email body snapshot; attached study patterns may use Source study pattern snapshot. LMS-based changes retain platform, URL/ID, and summary without fabricated email snapshots.
- The old slot-based model is deprecated. In Study Pattern, do not recreate Sequence, Academic Credits, Credits Required, Slots Required, Requirement Type, Study Semester, My Course State, Requirement, Code, or Registration Source. Credits may exist only as the current rollup.

## Notion view protection

- Views are presentation, not canonical state. Read existing views if useful, but never create, update, delete, copy, rename, move, reorder, switch, or rebuild any view.
- Never change filters, sorting, grouping, layout, visible properties, display configuration, or other view settings. Do not call create_view/update_view tools.
- Modify only authorized database/data-source attributes, descriptions, page properties, relations, and bodies. The preferred table view is a read-only locator.
