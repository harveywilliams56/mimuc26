# MIMUC Website

This website is intentionally kept as a **simple static holding page**.

It is built using **plain HTML + CSS + Bootstrap**, with **no build system, no framework, and no backend**.  
This is deliberate: future student organisers should be able to understand and update the site quickly with minimal technical overhead.
The only reason I even bothered using Bootstrap is to get a simple image carousel. Otherwise I would have used plain HTML/CSS.

---

## Design Philosophy

Keep this site:

- Simple  
- Static  
- Easy to edit  
- Easy to hand over  

Do **not** turn this into a complex web app.

---

## Use External Tools for Forms & Mailing Lists

This site should **not** implement its own:

- Registration systems  
- Submission forms  
- Mailing lists  
- Databases  

Instead, use third-party services such as:

- Google Forms  
- Microsoft Forms  
- Mailchimp  
- Eventbrite  

Then:
- link to them, or  
- embed them into the page  

This keeps the site maintainable and avoids unnecessary complexity.

---

## Images — IMPORTANT

**Do not upload large images to this repository.**

GitHub repositories perform poorly with large binary files, and this will:

- slow down cloning  
- bloat the repository permanently  
- make future updates painful  

### Before adding images:

- Compress them  
- Resize to web-appropriate dimensions (e.g. 1200–2000px max)  
- Prefer JPEG or WebP over large PNGs  
- Only include a curated selection, not everything  

---

## If large images are accidentally added

### Case 1 — Not yet commited

This is fine - just delete the file


### Case 2 — Already in repository history (more serious)

Git will still retain the file even if deleted normally.

You will need to go figure out how to remove the file from the repository history (a huge nuisance)

---

## How to Update the Site

Do **not** edit the main repository directly.

### Workflow:

1. Fork the repository to your own GitHub account  
2. Clone your fork locally  
3. Create a new branch:
   git checkout -b your-feature-name
3. Make your changes  
4. Commit and push:
   git add .
   git commit -m "Describe your changes"
   git push origin your-feature-name
5. Open a Pull Request to the main MIMUC repository  

---

## Editing Structure (Important)

The website is intentionally structured using HTML `<section>...</section>` blocks. Each section represents a self-contained part of the page (e.g. hero, about, schedule, sponsors).

**All edits should be done one section at a time. Do not attempt to modify multiple sections in a single change.**

This keeps the codebase simple, avoids merge conflicts, and reduces the risk of accidentally breaking unrelated parts of the page.


### Using LLMs (ChatGPT, etc.)

It's helpful to paste the entire `index.html` into your preferred LLM for context if needed. However:

- **Only ask it to generate or modify one `<section>` at a time**
- Do not accept large full-file rewrites
- Review changes carefully before committing
- Replace only that section in `index.html`  
- Commit and test

This ensures changes remain controlled, readable, and easy to review.

---

## Approval Process

All changes must be approved before merging.

If you are unsure or something is blocked contact:

Harvey Williams  
hw562@cantab.ac.uk  
[harveywilliams.com](https://www.harveywilliams.com)

I've set the domain to autorenew at approx £15 - pls reimburse me in 2027 🙏

---

## Final Principle

This is a **simple, static, handover-friendly site**.

When in doubt:

- Remove complexity  
- Avoid adding tooling  
- Keep things obvious for the next student  