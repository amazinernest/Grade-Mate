# GradeMate — Smart Assignment Marking for Academics

GradeMate is a free, browser-based academic assignment marking tool built for university lecturers. It works entirely in a single HTML file — no server, no installation, no API key required.

Upload student submissions, define your marking criteria, run automatic scoring, review and adjust each score, then download the final results as a CSV file ready to open in Excel.

---

## Live demo

Host on GitHub Pages and open in any browser. Works on desktop, tablet, and mobile.

---

## Features

### For any course, any university
- Set your own course code, course title, lecturer name, session, department, total marks, pass mark, and grade boundaries
- Not tied to any specific course — works for EDF 423, EGC 812, or any other course

### Flexible submission upload
| Format | How |
|--------|-----|
| CSV | Google Forms export, Excel export as CSV |
| Excel (.xlsx) | Direct spreadsheet export |
| Word (.docx) | Individual student files — select multiple |
| PDF | Individual student files — select multiple |
| Plain text (.txt) | Individual student files |

Mix formats in the same session. Drag and drop or click to browse.

### Custom marking guide
- Type your criteria directly — one row per criterion with label and maximum marks
- Or upload your marking guide as a Word, PDF, or text file and the app extracts the criteria automatically
- The app warns you if your criteria total does not match the declared total marks

### Integrity check (no API needed)
Every submission is scanned automatically before marking begins:

**AI writing detection** — flags responses with known AI writing patterns including overused vocabulary ("foundational", "pivotal", "underscore"), formulaic phrases ("it is worth noting that", "plays a crucial role"), and suspiciously uniform sentence lengths. Gives each submission an AI likelihood score.

**Duplicate detection** — compares every submission against every other submission using word trigram similarity. Flags pairs with 35% or more shared content and shows the similarity percentage and matching student name.

**Word count** — flags submissions that appear too short for the assignment requirements.

> These flags are indicators only — not proof. Always read the full submission before making any decision.

### Auto marking
The built-in marking engine scores each submission against your criteria by:
- Checking keyword coverage from the criterion label
- Rewarding examples and application language
- Rewarding analytical language (because, therefore, explains, demonstrates)
- Giving citation credit when a criterion mentions references or literature

Every score is pre-filled as a suggestion. You review and override each one.

### Marking interface
- **Jump-to-student dropdown** — find any student instantly without clicking through the list
- **Quick score buttons** — 0 / half / full marks buttons for each criterion
- **Editable input** — type any score including decimals
- **Running total** — updates live as you score, shown as pass (green) or fail (red) with grade
- **Feedback box** — optional written feedback per student, included in the CSV export
- **"View duplicate" button** — jump directly to the matching student when a duplicate is flagged

### Results
- Sortable table — click any column header to sort by name, score, grade, result, word count, AI flag, or duplicate flag
- Live search — filter results by student name instantly
- Full statistics — total submissions, class average, passed, failed, AI flagged, duplicates flagged
- **Zero all flagged** — set all flagged submissions to zero with one click (still editable individually)

### CSV export
Downloads a spreadsheet with:
- Student name, matric/ID, department, course, assignment, session
- Total score, max marks, percentage, grade, pass/fail
- Word count, AI flag, AI score, duplicate flag, duplicate match, similarity percentage
- Written feedback
- Individual score per criterion

---

## How to use

### Option A — GitHub Pages (recommended, free hosting)
1. Create a new GitHub repository
2. Upload `index.html` to the repository root
3. Go to **Settings → Pages → Source: main branch / root**
4. Your app is live at `https://yourusername.github.io/your-repo-name`

### Option B — Run locally
Open `index.html` in any modern browser. No server needed.

---

## Workflow

```
1. Open GradeMate
2. Enter course details and define marking criteria
3. Upload student submissions (CSV, Word, PDF, or text)
4. Review the integrity check report
5. Run auto marking
6. Review and adjust each student's scores
7. Download results as CSV
```

---

## Google Forms setup tips

For best results when using Google Forms:
- Add a "Full Name" question (Short answer)
- Add a "Matric Number" question (Short answer)
- Add a "Response" question (Paragraph) for the actual submission

When you export responses as CSV from Google Forms (Responses → Download as CSV), GradeMate automatically detects the name, matric, and response columns.

---

## Grade boundaries

The default grade boundaries are:

| Grade | Percentage |
|-------|-----------|
| A | ≥ 70% |
| B | ≥ 55% |
| C | ≥ 45% |
| D | ≥ 35% |
| F | Below 35% |

These are fully configurable in the course setup screen.

---

## Limitations

- **PDF text extraction is limited** — PDFs with scanned images or complex formatting may not extract correctly. For best results, ask students to submit Word (.docx) or plain text files.
- **Auto marking is rule-based** — it uses keyword matching and linguistic patterns, not AI. Treat auto scores as a starting point, not a final decision. You must review every score.
- **No data is saved between sessions** — GradeMate runs entirely in the browser. If you close or refresh the page, your work is lost. Download the CSV before closing.
- **No login or accounts** — all data stays in your browser and is never uploaded to any server.

---

## Browser support

Works in all modern browsers: Chrome, Firefox, Edge, Safari. Recommended: Chrome or Edge for best file reading support.

---

## Built for Nigerian universities

GradeMate was originally built for use at the University of Lagos, Department of Educational Foundations, for EDF 423 (Behaviour Modification). It is designed to work in the Nigerian university context — Google Forms submissions, CSV exports, Word and PDF individual files, and the specific marking conventions used in Nigerian higher education.

---

## License

Free to use, share, and adapt for academic purposes.
