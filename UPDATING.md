# Updating Your Website

All changes auto-deploy within ~2 minutes of pushing to `main`. You can make every edit directly on GitHub in your browser — no local tools needed.

---

## Add a new paper

1. Go to `data/papers.yaml` on GitHub and click the pencil (edit) icon.
2. Add a new entry at the top of the appropriate section. Copy an existing entry as a template:

```yaml
- title: "Your Paper Title"
  authors: ["Aryen Shrestha", "Coauthor Name"]
  year: 2025
  status: "working paper"   # working paper | under review | accepted | published | work in progress
  venue: ""                 # journal name if published
  volume: ""
  pages: ""
  pdf: ""                   # e.g. "files/your-paper.pdf"
  link: ""                  # DOI or external URL
  abstract: "One-paragraph abstract."
  job_market_paper: false
  type: "working-paper"     # working-paper | work-in-progress | published
```

3. If you have a PDF, upload it to `static/files/` and set `pdf: "files/filename.pdf"`.
4. Commit. The site rebuilds automatically.

---

## Mark a paper as published

In `data/papers.yaml`, change the entry:
- `status:` → `"published"`
- `type:` → `"published"`
- `venue:` → the journal name
- Add `volume:` and `pages:` if known
- Add `link:` with the DOI

---

## Update your bio

Edit `content/_index.md`. The text there is the three-paragraph bio on your homepage. Write in plain Markdown.

---

## Update your CV

Replace `static/files/cv.pdf` with the new version. Keep the same filename — the download button on the CV page will keep working.

---

## Change your photo

Replace `static/images/photo.jpg` with your new headshot. Keep the same filename. The photo displays at 160×160px, cropped to a circle — a square or portrait image works best.

---

## Add a teaching entry

Edit `data/teaching.yaml` and add an entry:

```yaml
- course: "GOV 50: Data"
  role: "Teaching Fellow"
  institution: "Harvard University"
  term: "Fall 2025"
  instructor: "Prof. Name"
```

---

## Add a news item

Edit `data/news.yaml` and add an entry at the top:

```yaml
- date: "2025"
  text: "Paper accepted at <em>Journal of Political Economy</em>."
```

HTML is allowed in the `text` field (e.g. `<em>` for italics).

---

## Add a policy writing entry

Edit `data/policy.yaml` and add an entry:

```yaml
- title: "Your Essay Title"
  authors: ["Aryen Shrestha"]
  year: 2025
  venue: "Publication Name"
  date: "Month Year"
  link: "https://..."
```

---

## Change your email or institution info

Edit `hugo.yaml` and update the relevant field under `params:`.

---

## Questions?

If something breaks, check the **Actions** tab in GitHub — it shows the build log and any errors.
