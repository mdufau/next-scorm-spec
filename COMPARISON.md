# How Next-SCORM compares

## The landscape today

| | SCORM 1.2 / 2004 | xAPI / cmi5 | AI Tools (e.g. Mindsmith) | **Next-SCORM** |
|---|---|---|---|---|
| Format | Binary zip + XML | JSON statements | Proprietary + SCORM export | **Open JSON** |
| Content ownership | Locked in zip | Locked in LRS | Locked in platform | **You own it** |
| Git-friendly | ❌ | ❌ | ❌ | **✅** |
| AI-native authoring | ❌ | ❌ | ✅ (content only) | **✅ (pedagogical structure)** |
| Bloom's Taxonomy built-in | ❌ | ❌ | ❌ | **✅** |
| Edit without source files | ❌ | ❌ | ❌ | **✅** |
| Works offline / self-hosted | ✅ | ⚠️ | ❌ | **✅** |
| Free / open source | ❌ | ⚠️ | ❌ | **✅ (MIT)** |
| LMS compatible | ✅ | ✅ | ✅ | **✅ (via adapters)** |

---

## Why not just use xAPI or cmi5?

xAPI and cmi5 are excellent *tracking* standards. They solve the "limited data" 
problem of SCORM 1.2. But they don't solve the *authoring* problem.

You still need a proprietary tool to create content. You still export a 
package that lives on a vendor's server. You still can't open the course 
file in a text editor and make a change.

xAPI and cmi5 are a better pipe. Next-SCORM is a better container.

---

## Why not just use Mindsmith (or similar AI tools)?

AI-native authoring tools are a step forward for *speed of creation*. 
But they introduce a new form of lock-in:

- Your content is stored on their servers
- Export is still SCORM — the same opaque zip format
- If they raise prices or shut down, your courses are gone
- No pedagogical structure — AI generates content, not learning design

Mindsmith makes SCORM faster to produce. Next-SCORM makes content 
permanently free.

---

## The actual problem xAPI, cmi5 and AI tools don't solve

Imagine your colleague inherits a compliance module created 2 years ago.
The original vendor is gone. No source files. Just a zip on a server.

She needs to change the logo and update the date.

With SCORM (any version): half a day of surgery on compiled files.  
With Mindsmith: impossible — the content lives on someone else's server.  
With xAPI/cmi5: the tracking is better, but the course file is still opaque.

**With Next-SCORM**: open `course.json`, change two values, redeploy in 30 seconds.

This is the problem we're solving.

---

## What Next-SCORM is not

Next-SCORM is not an LMS. It does not replace your LMS.  
Next-SCORM is not anti-SCORM. It exports to SCORM for LMS compatibility.  
Next-SCORM is not a closed SaaS. The format is open and MIT licensed.

Next-SCORM is a better *content format* — and a platform built on top of it.
