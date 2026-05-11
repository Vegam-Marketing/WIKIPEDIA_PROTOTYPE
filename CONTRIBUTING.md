# Contributing to the Vegam Solutions Wikipedia draft

This is a short, practical guide for anyone editing the article draft in this repository. The rules here are stricter than for a typical open-source project, because the eventual destination — Wikipedia — has strict rules of its own.

---

## Before you edit

### Disclose any conflict of interest

If you have any connection to Vegam Solutions — employment, contracting, friendship with founders, investment, or anything else — declare it in your first pull request or commit message. Example:

> *"COI disclosure: I am an employee of Vegam Solutions, in the marketing team. I am preparing this draft as part of my work."*

This disclosure does not disqualify you from contributing. It is required by Wikipedia and protects both you and the article. Failure to disclose, and later being discovered, is what causes accounts to be blocked.

### Read the README

The repository README explains the source-quality hierarchy, the role of each file, and the submission process. Don't skip it.

---

## How to edit the article text

The only file you should be editing for content changes is:

```
content/vegam-solutions.md
```

This is a Markdown file with footnote-style citations. Each section corresponds to a section in the final Wikipedia article.

### Adding a citation

Citations are footnotes in the Markdown format. To cite source 4 (the CHEManager piece) inline:

```markdown
The engagement was deployed across more than twenty production lines.[^4]
```

To add a new citation, add a new footnote reference (e.g., `[^15]`) inline, then add the definition at the bottom of the file:

```markdown
[^15]: Author, "Article title". *Publication name*. Date. *[note: secondary / primary / etc.]*
```

### Adding a TODO

The TODO list at the bottom of the Markdown file tracks every open item. Add new items as you find them, and tick off ones you resolve:

```markdown
- [ ] Find independent source for Hubli office establishment date
- [x] Confirm Vegam SFS module names
```

### What not to do

- **Do not** add LinkedIn URLs as visible blue-underlined links in the article body. They live only in reference 11.
- **Do not** add marketing language. Wikipedia neutral tone is the bar. Words to avoid: *flagship, leading, cutting-edge, world-class, trusted, innovative, transforming, next-generation, premium, robust*.
- **Do not** add customer testimonial quotes from company materials. They will be removed during review.
- **Do not** quote more than 15 words from any single source, or quote the same source more than once.
- **Do not** rename the article or change the corporate name without supporting evidence. If "Vegam SFS" eventually becomes the legal company name, a registry filing or press announcement needs to be cited.

---

## How to edit the visual prototype

The visual prototype lives at:

```
docs/index.html
```

This file is hand-maintained. It mirrors the Markdown content but with Wikipedia-style visual rendering. After significant changes to the Markdown, the HTML should be updated to match.

For small changes (a single citation, a typo fix), you can usually edit both files in one commit. For larger structural changes (adding a section, reordering content), update the Markdown first, get it reviewed, then update the HTML.

---

## Pull request conventions

If you're working in a fork-and-PR workflow:

- **One change per pull request.** Mixing "add a citation" with "rewrite the history section" makes review slow and error-prone.
- **Reference the TODO item** your PR addresses, if applicable.
- **State what type of source** you're adding (secondary / primary / press release / etc.).
- **State any COI** in the PR description.

Example PR description:

> Adds independent citation for BASF Coatings Würzburg deployment.
>
> Source: [Trade publication name], dated [date]. This is a secondary source — independent of Vegam.
>
> Resolves TODO item: "Find an independent press citation for the BASF Coatings Würzburg deployment."
>
> COI: I am an employee of Vegam Solutions. This citation does not contain any claim authored by Vegam or its employees.

---

## When in doubt, ask

Wikipedia's review process is unforgiving but its community is generally helpful. Two good places to ask if you're unsure about something:

- [Articles for Creation help desk](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_creation/Help_desk)
- [Wikipedia Teahouse](https://en.wikipedia.org/wiki/Wikipedia:Teahouse) (newcomer help forum)

You can also open a discussion in this repository's Issues tab to talk through changes before making them.
