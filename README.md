# Ginger Tabora — Resume & Portfolio Site

A single-page static resume site, hand-built as HTML/CSS and deployed with GitHub Pages. A portfolio section is planned as part of this same site.

**Live site:** https://gtabora510.github.io/resume-2026/

---

## How I built this

I wanted a resume and portfolio site that looked like something a technical writer would actually make — clean, a little playful, styled like documentation itself (sections labeled `README.md`, `CHANGELOG.md`, `package.json`, and so on). Rather than write the HTML by hand from scratch, I used Claude (via claude.ai) to design and generate it from my resume content, then used Claude Code, VS Code, and GitHub to get it from my machine onto the web.

Here's the actual sequence, step by step.

### 1. Set up the local toolchain

Installed the tools needed to build and ship the site from my Windows PC:

- **Claude Code** — AI coding agent, used from the terminal/VS Code
- **VS Code** — code editor
- **Git** — version control
- **GitHub CLI** (`gh`) — for GitHub operations from the command line

### 2. Created a GitHub account

Signed up at [github.com](https://github.com) — this is where the code and the live site both live.

### 3. Connected Claude Code to GitHub

Authenticated Claude Code against my GitHub account so it could work with repos on my behalf.

### 4. Connected Claude Code to VS Code

Installed/linked the Claude Code integration inside VS Code, so I could prompt Claude directly from the editor instead of switching to a separate terminal window.

### 5. Created the repo on GitHub

Went to github.com and created a new repository through the website (rather than the CLI):

**[gtabora510/resume-2026](https://github.com/gtabora510/resume-2026)**

Because this is a *project* repository (not a `username.github.io` root repo), the live site is served from a sub-path: `gtabora510.github.io/resume-2026/`.

### 6. Created a token for authentication

Generated a GitHub personal access token so Git operations (push/pull) from my local machine would authenticate properly against the new repo.

### 7. Cloned the repo in VS Code

Cloned `resume-2026` down to my local machine and opened it in VS Code:

```bash
git clone https://github.com/gtabora510/resume-2026.git
cd resume-2026
code .
```

### 8. Built the resume content

Uploaded my resume (a Word `.docx` file) directly into a chat with Claude and worked through the design conversationally — content structure, layout concept, color palette, and copy — until the page matched what I wanted.

### 9. Added the file to the repo

Downloaded the finished HTML file from Claude, renamed it to `index.html` (the filename GitHub Pages looks for by default), and dropped it into the cloned `resume-2026` folder in VS Code.

### 10. Committed and pushed

```bash
git add index.html
git commit -m "Add resume site"
git push origin main
```

### 11. Turned on GitHub Pages

In the repo on GitHub: **Settings → Pages** → set the source to deploy from the **`main`** branch, root folder (**`/`**).

GitHub Pages builds and publishes automatically — no separate static site generator step, since the page is already plain HTML/CSS.

### 12. Live

A minute or two after enabling Pages, the site was live at:

**https://gtabora510.github.io/resume-2026/**

---

## Stack

| Purpose | Tool |
|---|---|
| Content & design | Claude (claude.ai) |
| Local editing | VS Code |
| AI pair-programming | Claude Code |
| Version control | Git |
| Repo hosting | GitHub |
| CLI tooling | GitHub CLI |
| Hosting | GitHub Pages |

## Updating the site

Any future edits: change `index.html` locally, then

```bash
git add index.html
git commit -m "Update resume"
git push origin main
```

GitHub Pages will redeploy automatically within a minute or two.
