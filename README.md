# FYUG Study Hub — Assam University

A responsive static website for Semester 1 BA FYUGP / NEP 2020 study materials.

## Included
- `index.html` — complete HTML/CSS/JavaScript website
- `data.json` — subject → unit → chapter → resource mapping
- `documents/` — 116 real PDF files generated for the 29 syllabus chapters
- Each chapter has Detailed Notes, 2-mark Answers, 10-mark Model Answers, and a PYQ status PDF
- Search, subject/unit/chapter navigation, resource buttons, PYQ filters, and browser-local revision tracker

## Important academic accuracy note
The PDFs are syllabus-aligned study resources and model revision materials. They are not represented as university-issued material. No verified original past papers were supplied, so each PYQ PDF honestly states **No verified PYQs uploaded yet** and does not invent exam years or claim model questions appeared in exams.

## Test locally
Because the site loads `data.json` and checks files with `fetch`, open it through a local web server rather than directly as a `file://` URL.

Python:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`.

## Deploy to GitHub Pages
1. Create a repository or open your existing repository.
2. Upload the contents of this folder (the `index.html`, `data.json`, and `documents/` folder must all be at the repository root).
3. In GitHub, open **Settings → Pages**.
4. Select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Wait for the deployment to finish.

The website uses relative paths, so it works on a project URL such as `https://USERNAME.github.io/REPOSITORY/`.

## Add more subjects later
Edit `data.json` using the same hierarchy:
`subjects[] → units[] → chapters[] → resources[]`.
For each resource, include `type`, `title`, `path`, and optional `description`. Upload the PDF to that exact path. Supported types:
- `detailed-notes`
- `2-mark-answers`
- `10-mark-answers`
- `pyqs`

## PDF replacement and uploads
This is a static GitHub Pages project. It cannot securely upload files back into GitHub without a server and authentication. To replace a PDF, upload the new file at the same path in the repository; the mapping remains unchanged. Do not add a PYQ as verified until the original paper or a reliable source is recorded.
