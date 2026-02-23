# Next-SCORM — Interactive Prototype

> **An AI-native e-learning authoring platform** — faster, cheaper, and more open than traditional SCORM tools.

🔗 **[View live prototype →](https://mdufau.github.io/next-scorm-spec/prototype/next-scorm-index.html)**

> This prototype lives in the [`next-scorm-spec`](https://github.com/mdufau/next-scorm-spec) repository alongside the format specification (`spec.md`), the comparison document (`COMPARISON.md`), and the reference `course.json` structure.

---

## What is Next-SCORM?

Next-SCORM is a concept platform designed to challenge the status quo of e-learning authoring tools like Articulate 360 and Rise — by making course creation faster, more contextual, and accessible to anyone, not just certified instructional designers.

The core idea: **generate, edit, and deploy SCORM-compliant e-learning content with AI assistance**, while preserving full data integrity through the original `course.json` structure — a key differentiator that existing tools ignore.

---

## ✦ Key differentiators

| Feature | Articulate / Rise | Next-SCORM |
|---|---|---|
| AI-generated content | ❌ Limited | ✅ Native, contextual |
| Price | ~$1,400/year | TBD (significantly lower) |
| Open to non-designers | ❌ Steep learning curve | ✅ Prompt-first creation |
| course.json preserved on export | ❌ | ✅ Always |
| Multi-format export | Partial | ✅ SCORM 1.2, 2004, xAPI, HTML, PDF, cmi5 |
| AI voice narration | ❌ | ✅ Built-in |
| Bilingual UI | ❌ | ✅ EN / FR |
| Collaborative editing | ❌ | ✅ Real-time roles |

---

## 🖥 Prototype screens

This prototype demonstrates the full authoring workflow across 7 interconnected screens. All screens are bilingual (EN/FR) with persistent language preference.

| Screen | File | Description |
|---|---|---|
| 🚪 Splash | `next-scorm-index.html` | Entry point — language selection |
| 📊 Dashboard | `next-scorm-dashboard.html` | Course overview, stats, Learning Paths |
| ✨ Create | `next-scorm-create.html` | AI-assisted course creation from prompt |
| ✏️ Editor | `next-scorm-editor.html` | 3-panel editor with drag & drop assets |
| `{ }` JSON Viewer | `next-scorm-json.html` | Live course.json with syntax highlighting & SCORM validation |
| 📦 Export | `next-scorm-export.html` | Multi-format export with LMS configuration |
| 🎓 Learner Preview | `next-scorm-learner.html` | SCORM player simulation with live tracking panel |

---

## 🎯 Target users

- **Responsables Formation** — orchestrate and deploy without technical knowledge
- **Concepteurs Pédagogiques** — design and iterate faster with AI assistance
- **Relecteurs / SMEs** — review content without touching the tool
- **Curators** — manage learning paths and module sequencing

---

## 📦 Export formats supported

- **SCORM 1.2** — Maximum LMS compatibility (Moodle, 360Learning, Docebo, Cornerstone…)
- **SCORM 2004** — Advanced sequencing and richer tracking data
- **xAPI (Tin Can)** — Granular analytics, mobile & offline-ready
- **HTML Standalone** — No LMS needed, shareable link or iframe embed
- **PDF** — Printable reference, compliance documentation
- **cmi5** — Next-generation standard (beta)

---

## 🛠 Tech stack (prototype)

- Pure HTML / CSS / JavaScript — no framework, no build step
- Google Fonts: DM Sans, Syne, JetBrains Mono
- `localStorage` for language persistence
- Fully static — hostable on GitHub Pages, Netlify, or Vercel

---

## 🚀 Run locally

No installation required. Just clone and open in browser:

```bash
git clone https://github.com/mdufau/next-scorm-spec.git
cd next-scorm-spec/prototype
open next-scorm-index.html
```

Or simply download the ZIP and double-click `next-scorm-index.html`.

---

## 🗺 Roadmap (post-prototype)

- [ ] Admin Settings screen — role management (RF, CP, Relecteur, Curator)
- [ ] Learning Paths — module sequencing with auto-generated README for LMS
- [ ] Real AI content generation via API
- [ ] Backend & LRS integration
- [ ] LMS deployment pipeline

---

## 👤 About

Built by **Melanie DCM** — 15 years in e-learning & SCORM, certified Articulate 360 trainer, instructional design educator.

This prototype was designed to validate the concept and gather early feedback before moving into development.

→ Feedback welcome: open an issue or reach out directly.

---

*Next-SCORM — Beta v0.9 prototype · Not yet in production*
