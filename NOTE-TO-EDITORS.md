# Note to Editors

This document provides an overview of how WE Rocketry's website is built and serves as a guide for editors who may not be familiar with web development.

## Quick Primer: How Websites Work

Websites are made of three core technologies:

- **HTML** (structure): defines content and layout
- **CSS** (style): controls appearance and design
- **JavaScript** (behavior): adds interactivity

Websites can be delivered in different ways:

- **Static**: Pre-built files served directly (fast, simple, cheap)
- **Server-Rendered**: Server generates pages on each request (dynamic, complex)
- **Client-Rendered**: Browser runs JavaScript to build pages (interactive apps)

Content can be authored using:

- **Raw HTML/CSS/JS**: Direct coding
- **Markdown**: Simple text format that converts to HTML
- **Content Management Systems**: WordPress, Ghost, etc.
- **Frameworks**: React, Vue, etc. (for complex web apps)

For deployment:

- **Static Hosting**: Services like GitHub Pages, Netlify (free, simple)
- **Server Hosting**: Traditional web servers (requires maintenance)
- **Cloud/Serverless**: AWS, Vercel, etc. (scalable, expensive)

---

## What We Use (and Why)

We use **[GitHub Pages](https://pages.github.com/)** + **[Jekyll](https://jekyllrb.com/)** to build and host the Western Engineering Rocketry website. This stack was intentionally chosen for engineering teams with high technical demand but low time and coding availability.

### Why GitHub Pages

- **Free hosting** with zero maintenance cost
- **No server setup** — GitHub builds and serves the site automatically
- **Version-controlled** — the entire site lives in a Git repo, so changes are tracked and reversible
- **Team-friendly** — anyone can edit or propose changes with a [GitHub account](https://github.com/signup)

### Why Jekyll

- **Simple content model**: pages and posts are just Markdown (`.md`) files
- **No coding required** for most updates — students only edit human-readable text
- **Low barrier to entry**: even first-years with no programming experience can contribute
- **Long-term maintainability**: Markdown is portable and future-proof; no lock-in to a framework
- **Consistent look**: Jekyll layouts ensure uniform design without manual HTML/CSS work

### Why This Is the Right Fit for a University Rocketry Team

- Teams rotate every year, so tools must be **easy to hand off**
- Skill levels vary widely; a Markdown-based system ensures **anyone can update the site**
- The site is primarily informational (who we are, sponsors, updates), which fits **static content** perfectly
- GitHub's infrastructure ensures **reliable uptime** for sponsors, judges, and prospective members
- Zero hosting fees and minimal technical overhead keep focus on **engineering, not web operations**
- Full control of the repo means we avoid proprietary website builders or subscription tools

### Summary

GitHub Pages + Jekyll gives us a **free, simple, maintainable, student-friendly, long-lived** web platform. It provides the right balance of control and ease of use while supporting the natural turnover and varied experience levels of a university engineering team.

---

### Important Note for Future "Let's Rewrite the Site" People

So you're a future member or exec and you're thinking:  
"Let's rebuild the site with the latest JavaScript framework / serverless platform / animated-whatever. That would be so much cooler!"

That instinct? **Wrong. Fully wrong.**  
For this site, that thinking is a distraction and a liability.

Here's why you should **not** "modernize" the stack:

- **This is not a web dev club.**  
  We are a rocketry team. Our scarce time, energy, and brainpower belong on design reviews, simulations, testing, manufacturing, and documentation — not on debugging a React build or chasing deployment bugs at 2 a.m.

- **The current stack is deliberately boring for a reason.**

  - Markdown + Jekyll + GitHub Pages + CNAME → **simple**, **free**, **stable**, and **easy to hand off**
  - Anyone can edit content with minimal onboarding
  - No one needs to be "the web person" to keep the site alive

- **Turnover destroys fancy stacks.**  
  That shiny JavaScript framework you love today will be outdated in 2–3 years. The one person who understands it will graduate. Then the site rots, breaks, or becomes unmaintainable — and someone has to waste time ripping it all out and going back to something like… Markdown + Jekyll.

- **Our audience does not care about your "cool" tech.**  
  Most of our sponsors, judges, mentors, and professors are 40–70+.  
  They want:

  - Fast load times
  - Clear navigation
  - Straightforward content

  They do **not** want their cursor turning into a rocket, parallax scroll, or some "reactive button" nonsense between them and the info they need.

- **Complexity is a cost, not a flex.**  
  Every extra framework, build step, dependency, plugin, and deployment target is one more thing that can fail, misbehave, or block contributions. The more "impressive" you make the tech stack, the fewer people can safely touch it — and the more fragile it becomes.

- **The current solution already solves the real problem.**  
  We need:

  - A reliable, low-cost, low-friction public face for the team
  - Easy sponsor updates and project summaries
  - Something a non-coder can update in a pinch

  Jekyll + GitHub Pages already delivers exactly that.

If you're still convinced you "know better" and want to play with fancy stacks:

- Do it in a **separate repo / subdomain** as a personal or experimental project
- Do **not** migrate the main site away from Markdown + Jekyll + GitHub Pages unless you have a rock-solid, multi-year continuity plan and buy-in from multiple technically competent maintainers (and even then, think twice)

**Bottom line:**  
The main website is infrastructure, not a toy. Keep it **boring, stable, readable, cheap, and maintainable**. That's the correct engineering decision for this team.

---

## Getting Started as an Editor

You do **not** need programming experience to edit the website. All content is simple Markdown files stored in a GitHub repository.

### 1. Editing Directly on GitHub (Easiest / Recommended for Most People)

1. Open the website repository on [GitHub](https://github.com/)
2. Navigate to the page you want to edit (files ending in `.md`)
3. Click the file → click the **✏️ Edit** button
4. Make your changes directly in the browser
5. Scroll to **Commit changes**:
   - Add a short message describing what you did (e.g., `Add new sponsor`, `Update team bio`, `Fix grammar on main page`)
   - Select **Commit directly to main**
6. Click **Commit changes**

Use this method for:

- Updating sponsor lists
- Editing text
- Adding new pages or posts
- Fixing typos
- Updating links

This is the normal workflow.

---

### 2. Cloning the Repo Locally (Git or GitHub Desktop)

Use this if you want to work offline or prefer a full editor.

#### Option A: Git (Command Line)

1. [Install Git](https://git-scm.com/downloads)
2. On the repo page → click **Code** → copy the HTTPS URL
3. Run:

   ```bash
   git clone <repo-url>
   ```

4. Navigate into the repo:

   ```bash
   cd <repo-name>
   ```

5. Open in [VS Code](https://code.visualstudio.com/):

   ```bash
   code .
   ```

Make changes, then:

6. Stage and commit:

   ```bash
   git add .
   git commit -m "Update About page"
   ```

7. Push:

   ```bash
   git push
   ```

Your changes are now live on `main`.

#### Option B: GitHub Desktop (Simplest Local Option)

1. [Install GitHub Desktop](https://desktop.github.com/)
2. File → **Clone repository…** → pick the repo
3. In GitHub Desktop: **Open in Visual Studio Code**
4. Make your edits
5. Back in GitHub Desktop:
   - Write a commit message
   - **Commit to main**
   - Click **Push origin**

---

### 3. Editing in VS Code (After Cloning)

1. Open the repository folder in [VS Code](https://code.visualstudio.com/)
2. Find a `.md` file in the Explorer panel
3. Edit using [Markdown syntax](https://www.markdownguide.org/basic-syntax/):
   - `#` for headings
   - `-` for bullet lists
   - `[text](link)` for links
   - `**bold**` for bold text
   - `*italic*` for italic text
4. Save changes (`Ctrl+S` / `Cmd+S`)
5. Optionally use Markdown preview (`Ctrl+Shift+V` / `Cmd+Shift+V`)

When done, commit + push to `main`.

---

### 4. General Editing Guidelines

- Keep content simple and clear — sponsors and faculty will read it
- Avoid moving/renaming files unless you're sure it won't break navigation
- Keep stylistic consistency with existing pages
- If unsure, ask someone before deleting or restructuring anything
- Small edits go straight to `main` — this is expected and normal

---

## When to Use Branching (Advanced; Big Changes Only)

Branching is **not** required for normal editing.  
Use a separate branch only for **large** or **risky** edits, such as:

- Modifying the theme or layout
- Editing `_config.yml`
- Restructuring folders or navigation
- Changing includes or templates
- Adding/removing plugins
- Anything that could break the site
- Multi-file content overhauls

**Workflow for large changes:**

1. Clone the repo locally
2. Create a branch:

   ```bash
   git checkout -b feature/theme-rework
   ```

3. Make your changes in VS Code
4. Commit and push the branch:

   ```bash
   git push -u origin feature/theme-rework
   ```

5. Open a **Pull Request** on GitHub
6. Have at least one other person review it
7. Merge into `main` once confirmed safe

This branching workflow protects the site from accidental breakage while still allowing deeper technical changes when necessary.

---

## Additional Resources

- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Docs](https://docs.github.com/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
