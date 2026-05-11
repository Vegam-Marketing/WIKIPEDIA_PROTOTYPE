# Vegam Solutions — Wikipedia article working draft

This repository holds the working draft of the proposed [Wikipedia](https://en.wikipedia.org/) article for **Vegam Solutions**, a Singapore-headquartered industrial software company. The draft is being prepared for submission via Wikipedia's [Articles for Creation](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_creation) process.

This repo is **not** the published Wikipedia article. It is a staging environment for drafting, sourcing, and review before submission.

---

## What's in this repo

```
.
├── README.md                          ← you are here
├── content/
│   └── vegam-solutions.md             ← editable article text (Markdown)
├── docs/
│   └── index.html                     ← rendered visual prototype (auto-served via GitHub Pages)
└── .github/
    └── workflows/
        └── pages.yml                  ← GitHub Pages deployment workflow
```

**Two files matter for editing:**

- **`content/vegam-solutions.md`** is the editable source of truth. Edit this when changing article text. It's plain Markdown, so anyone comfortable with text editing can contribute without touching HTML.
- **`docs/index.html`** is a visualization of what the article will look like once published, styled like Wikipedia's current Vector 2022 skin. It is hand-maintained — when significant changes go into the Markdown, the HTML is updated to match.

When the article is ready to submit, the Markdown content gets translated one more time — into [Wikipedia's MediaWiki markup](https://en.wikipedia.org/wiki/Help:Wikitext) — and submitted through Articles for Creation.

---

## GitHub Pages preview

After you push this repo to GitHub and enable Pages (Settings → Pages → Source: "Deploy from a branch" → Branch: `main` /docs folder), the rendered prototype will be live at:

```
https://<your-username>.github.io/<repo-name>/
```

Anyone with the URL can see the rendered article without cloning the repo or installing anything. This is the easiest way to share the draft with reviewers, your senior, or a Wikipedia editor for feedback.

A GitHub Actions workflow (`.github/workflows/pages.yml`) is included that handles deployment automatically on pushes to `main`. If you'd rather not use Actions, you can still enable Pages from the repo's Settings panel directly — both methods work.

---

## How to edit

### Editing article content

1. Open `content/vegam-solutions.md` in any text editor (VS Code, GitHub's web editor, anything).
2. Edit the section you want to change. Each section corresponds 1:1 with a section in the final Wikipedia article.
3. Citations are written as `[^1]`, `[^2]`, etc., and the reference definitions are at the bottom of the file. Add new citations by adding both the inline marker and the definition.
4. The TODO list at the bottom of the Markdown file tracks every open item. Tick items off (`- [x]`) when resolved, or add new ones as they come up.
5. Commit your changes with a clear message (e.g., `"Add citation for BASF Würzburg deployment"`).

### Updating the rendered prototype

After significant Markdown changes, the HTML prototype in `docs/index.html` should be regenerated to match. This is currently a manual hand-translation step. If you'd like to automate it, two options:

- Use Pandoc: `pandoc content/vegam-solutions.md -o docs/index.html --standalone --css=style.css` (will lose the custom Wikipedia styling — needs a styling pass after).
- Use a static site generator like MkDocs or Eleventy if you want a richer documentation site.

For most edits — small wording changes, citation additions, TODO updates — the Markdown file alone is enough. The HTML only needs regenerating when the structure changes (sections added, removed, or reordered).

---

## Source discipline

The single most important thing about this article is its sourcing. Wikipedia's notability standard for companies ([WP:NCORP](https://en.wikipedia.org/wiki/Wikipedia:Notability_(organizations_and_companies))) requires **significant coverage in independent, reliable, secondary sources** — and the article will be evaluated against that bar within days of submission.

### Source hierarchy (strongest to weakest)

1. **Independent trade press, mainstream journalism, peer-reviewed publications.** *CHEManager International*, *Manufacturing Digital*, *Technology Magazine* (editorial sections), the *Practical Founders Podcast* (editorial summary). These establish notability.
2. **Government registries.** MCA (India), ACRA (Singapore), US state corporate registries. Acceptable for basic corporate facts only — incorporation, registered office, directors. They do not establish notability on their own.
3. **The company's own website and official materials.** vegam.co, the product handbook, the company LinkedIn page. Acceptable for non-controversial factual claims (founding date, product names, leadership names). Cannot be used for evaluative claims or notability.
4. **Personal LinkedIn profiles, employee social-media posts, internal documents.** Treat with caution. Should not appear as inline links in the body text. Can be used only in tightly-scoped reference notes to verify basic facts (names, titles, current employer).
5. **Press releases, sponsored "company reports," database aggregators (Tracxn, Crunchbase, ZoomInfo, IndiaFilings as a standalone source).** Weakest tier. Do not rely on these.

### Citation count target

For a borderline-notability subject like Vegam Solutions, plan for **at least 5–7 independent secondary sources** before submission. Currently confirmed: CHEManager, Manufacturing Digital, Technology Magazine, Business Chief, Practical Founders, and Analytics India Magazine — six sources, several of them clustered around a single customer (Henkel). That is the bare minimum. Each additional independent source materially strengthens the article's chance of survival.

---

## Conflict of interest

If you have any connection to Vegam Solutions — employee, contractor, paid editor, friend of the founders, anyone with a stake — **you must disclose this** before editing the live Wikipedia article. The disclosure goes:

- On your Wikipedia user page
- On the article's Talk page
- In the edit summary of any edit you make to the article

This is required by Wikipedia's [Terms of Use](https://wikimediafoundation.org/wiki/Terms_of_Use) and the [Conflict of Interest guideline](https://en.wikipedia.org/wiki/Wikipedia:Conflict_of_interest). Failure to disclose is the single most common reason company-authored articles get deleted and the author's account gets blocked.

The safer path is to submit the draft through [Articles for Creation](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_creation), where an uninvolved Wikipedia editor reviews the draft before it goes live. This is the recommended route for any draft prepared by someone with a connection to the subject.

---

## Submission checklist

Before submitting to Articles for Creation, work through this checklist:

- [ ] Every claim in the article has a citation, or has been deliberately removed
- [ ] No `[citation needed]` tags remain
- [ ] All TODO items in `content/vegam-solutions.md` are either resolved or moved to a "future work" section
- [ ] The draft has been read end-to-end by at least one independent reviewer (not the author)
- [ ] All promotional language has been removed (no "flagship," "leading," "innovative," "trusted," etc.)
- [ ] No customer testimonial quotes are included
- [ ] No quote in the article exceeds 15 words, and no single source is quoted more than once
- [ ] The author has prepared their conflict-of-interest disclosure for the user page and Talk page
- [ ] At least 5 independent secondary sources are cited
- [ ] The rendered prototype at the GitHub Pages URL has been shared with the senior reviewer for final sign-off

---

## Version history

| Version | Date | Notable changes |
|---|---|---|
| v1.0 | initial | First skeleton structure based on outline |
| v2.0 | post-research | Real source citations integrated; expanded to full structure |
| v3.0 | post-senior-review | AI Intime and Vegam Robotics reframed as products (not subsidiaries); promotional tone removed; ~35% of unsupported content cut |
| v3.5 | partners + customers | Three named partners and nine company-stated customers added |
| v3.6 | BASF | BASF added to main Notable customers list |
| v3.8 | trim | Corporate restructuring paragraph trimmed to one sentence |
| **v4.0** | **consolidated** | **Pronunciation added; products alphabetised; legacy product names removed from history; seed-funding mention removed pending fact-check; corporate restructuring rewritten with AI Intime launch; VSFS modules updated to GR/Staging/Manufacturing/Dispatch/LIMS; external links expanded** |

---

## License and reuse

This draft is provided for use in preparing a Wikipedia submission. Once accepted by Wikipedia, the published article is governed by Wikipedia's licensing ([CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) and [GFDL](https://www.gnu.org/licenses/fdl-1.3.html)). The draft files in this repo are released under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) to be compatible with eventual Wikipedia hosting.

---

## Contact

For questions about this draft, contact the editor maintaining the repository.

For questions about Wikipedia process, see the [Articles for Creation help desk](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_creation/Help_desk) or the [Teahouse](https://en.wikipedia.org/wiki/Wikipedia:Teahouse) (Wikipedia's help forum for new editors).
