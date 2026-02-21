# Next-SCORM Format Specification — v0.1

> A human-readable, AI-friendly, LMS-compatible course format.  
> Designed for instructional designers. Built for the modern web.

---

## Why a new format?

SCORM was designed in 2001. It was built for a web that no longer exists.

Today, instructional designers deal with:
- Zip packages that break without warning
- Content locked inside expensive proprietary tools
- A 4096-character limit on learner data (SCORM 1.2)
- Source files that disappear when a vendor closes

Next-SCORM is a clean, open alternative. Your course lives in a single readable
JSON file. You own it. You version it. You deploy it anywhere.

---

## Core principles

**1. Human-readable first**  
A Next-SCORM file can be opened in any text editor and understood immediately.
No XML. No compiled bundles. No mystery.

**2. Pedagogically structured**  
Every course has explicit learning objectives mapped to Bloom's Taxonomy levels.
Structure is not optional — it's part of the format.

**3. AI-native**  
The format is designed to be generated and modified by AI tools.
Describe your course in plain language → get a valid Next-SCORM file.

**4. LMS-compatible by design**  
Next-SCORM exports to SCORM 1.2, SCORM 2004, LTI 1.3, and standalone HTML.
No LMS left behind.

**5. Git-friendly**  
Plain JSON means full version history, diffs, branches, and pull requests.
Your course content finally lives where your code lives.

---

## File structure

A Next-SCORM course is a single `course.json` file with 5 sections:

### `meta` — Course identity

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | ✅ | Unique identifier for this course |
| `title` | string | ✅ | Display title |
| `description` | string | ✅ | What learners will achieve |
| `language` | string | ✅ | BCP 47 language code (e.g. `en`, `fr`, `de`) |
| `author` | string | | Course author name |
| `created_at` | date | ✅ | ISO 8601 date |
| `updated_at` | date | ✅ | ISO 8601 date — update on every change |
| `tags` | array | | Free-form tags for search and categorization |

---

### `objectives` — Learning objectives

Each objective is mapped to a **Bloom's Taxonomy level**:

| Level | Verbs (examples) |
|-------|-----------------|
| `remember` | list, recall, identify |
| `understand` | explain, describe, summarize |
| `apply` | use, demonstrate, solve |
| `analyze` | compare, differentiate, examine |
| `evaluate` | judge, justify, critique |
| `create` | design, build, produce |

Objectives are referenced by `id` inside modules, creating a traceable link
between what you promise and what you deliver.

---

### `modules` — Course structure

A course is divided into modules. Each module contains **blocks**.

**Module fields:**

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `title` | string | Display title |
| `objectives` | array | References to objective IDs covered in this module |
| `sequence` | string | `linear` (default) or `free` |
| `blocks` | array | Ordered list of content and assessment blocks |

**Block types:**

| Type | Description |
|------|-------------|
| `content` | Text, images, video — the learning material |
| `quiz` | Questions with scoring and feedback |
| `scenario` | Branching decision-based interactions |
| `reflection` | Open-ended questions for self-assessment |
| `summary` | Key takeaways recap |

---

### `completion` — Tracking and scoring

| Field | Description |
|-------|-------------|
| `strategy` | `all_modules` (complete everything) or `min_score` (pass the assessment) |
| `min_score` | Minimum passing score (0–100) |
| `tracking.progress` | Track module-by-module progress |
| `tracking.score` | Track quiz scores |
| `tracking.time_spent` | Track time per module and total |
| `tracking.interactions` | Track individual question responses |

Unlike SCORM 1.2, there is **no character limit** on tracking data.  
Full interaction history is stored and retrievable.

---

### `export` — LMS compatibility

| Format | Description |
|--------|-------------|
| `scorm_1_2` | Classic SCORM 1.2 package for legacy LMS |
| `scorm_2004` | SCORM 2004 3rd edition |
| `lti_1_3` | Modern LTI 1.3 for Canvas, Moodle, Blackboard |
| `standalone_html` | Self-contained HTML — no LMS required |

---

## Versioning

This is **v0.1** — an early draft open for community feedback.

The format will evolve. Backwards compatibility is a core commitment:
a course valid in v0.1 will always be loadable in future versions.

---

## Contributing

This format is open. We welcome:
