# Cancer Care: Build the First Page

A step-by-step guide to building the first page of the **Cancer Care** blog on GitHub Pages. Follow the parts in order. Parts 1 and 2 are the thinking (your definitions and your project description). Part 3 is the building (a calm, readable website with images).

> **Your job is to make this your own.** The drafts below are starting points. Read each source yourself and rewrite every definition and sentence in your own words. Your mentor will review them with you.

---

## Part 1: Make three decisions

### Decision 1: What does "late diagnosis" mean?

There are two common meanings:

| Meaning | What it says |
|---|---|
| **Advanced stage at diagnosis** | The cancer is first found at stage III or IV |
| **Delayed diagnosis** | Diagnosis happens late because of ignored symptoms, missed appointments, or lack of access to care |

**Chosen definition for this blog: advanced stage at diagnosis (stage III or IV).**

Why this choice: stage is a clear, measurable fact, so the blog can use one definition from start to finish. Delays and lack of access are still worth writing about, but as *reasons* a cancer may be found late, not as the definition.

**Draft definition (rewrite in your own words):**

> In this blog, "late diagnosis" means that a person's cancer was first found at stage III or IV. At stage III, the cancer has usually grown larger or spread to nearby lymph nodes. At stage IV, it has spread to distant parts of the body.

**Sources to read and cite:**

- Late stage defined as stage III and IV, in a peer-reviewed study: [Ismail et al., Journal of Public Health Research](https://pmc.ncbi.nlm.nih.gov/articles/PMC9335192)
- Plain-language explanation of stage III (locally advanced) versus stage IV (spread to other organs): [GRAIL, "Why Finding Cancers Before It's Too Late Matters More Than Ever"](https://grail.com/stories/why-finding-cancers-before-its-too-late-matters-more-than-ever/). Note that GRAIL is a company that sells cancer screening tests, so use it for the stage explanation and confirm the numbers with a neutral source.
- **Also find and cite** the National Cancer Institute's cancer staging page (cancer.gov). A government health source is stronger than a company page for your definition.

### Decision 2: Who are "the people around them"?

**Chosen focus: caregivers and close family** (spouses and partners, parents, adult children, siblings, and close friends who help with daily care).

Why this choice: it is specific enough to write about well. Children, classmates, and coworkers could be future topics.

**Draft (rewrite in your own words):**

> "The people around them" means the caregivers and close family members who support someone through a late-stage cancer diagnosis, by helping with appointments, daily needs, and emotional support.

**Sources to read and cite:**

- Caregivers of people newly diagnosed with stage III or IV colorectal cancer described serious disruption and distress: [Oncology Nursing Forum study](https://ons.org/pubs/article/227986/preview)
- Review finding that cancer negatively affects family caregivers: [Systematic review, International Journal of Environmental Research and Public Health, 2023](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10138338/)

### Decision 3: Your project description

Each sentence connects back to late diagnosis, in the required order.

**Draft (rewrite in your own words, and check the numbers against the sources):**

1. **The problem:** Late diagnosis, meaning cancer first found at stage III or IV, remains common; one estimate says roughly one in five cancers in the US and England is still diagnosed at stage IV.
2. **The gap:** When someone is diagnosed late, the caregivers and close family around them are often given overwhelming news with little plain-language explanation of what the stage means or how to help.
3. **What this blog will do:** Cancer Care explains late-stage diagnosis in clear, jargon-free language and offers practical guidance for supporting a loved one while also caring for yourself.
4. **Who it is for:** It is written mainly for caregivers and close family, and it is also open to students and the general public who want to understand why finding cancer earlier matters.
5. **What makes it hopeful:** A late diagnosis is not the end of the story, because stage III cancers can often be treated with the aim of cure, treatment keeps improving, and informed, supported families can face each step with more confidence.
6. **Hopeful, continued:** By sharing warning signs and screening information, the blog also hopes to help readers catch cancer earlier in the people they love.

> **Check before publishing:** The "one in five" figure comes from the GRAIL page above, which describes stage IV diagnoses in the US and England. Confirm it with a neutral source such as the American Cancer Society or the National Cancer Institute and cite that source instead if you can. Do not publish a number you have not checked.

---

## Part 2: Set up the files

Your repository (`username.github.io`) should end up with this structure:

```
username.github.io/
├── README.md
├── _config.yml
├── index.md
└── assets/
    ├── css/
    │   └── style.scss
    └── images/
        ├── hero.svg
        └── ribbon.svg
```

**To create a file in the browser:** in your repo click **Add file → Create new file**. Typing a `/` in the file name creates a folder, so typing `assets/css/style.scss` makes both folders and the file. Then click **Commit changes**.

**To add the two images:** click **Add file → Upload files**, drag in `hero.svg` and `ribbon.svg`, then move them into `assets/images/` (or create `assets/images/hero.svg` first and upload into that folder). Your mentor can send you both image files.

---

## Part 3: Copy and paste these files

### File 1: `_config.yml`

This sets the site name, the soothing theme, and the tagline.

```yaml
title: Cancer Care
description: Understanding late-stage cancer diagnosis and supporting the people who walk through it
theme: jekyll-theme-cayman
show_downloads: false
lang: en
```

### File 2: `assets/css/style.scss`

This changes the theme's bright green to a calm teal and lavender palette and makes the text easier to read. **Keep the two lines of dashes at the very top.** The file will not work without them.

```scss
---
---
@import "{{ site.theme }}";

body {
  background-color: #fbf9f5;
  color: #2f3e46;
  font-family: "Georgia", "Times New Roman", serif;
}

/* Soft header */
.page-header {
  background-color: #a8d5d1;
  background-image: linear-gradient(120deg, #a8d5d1, #c9cdee);
}
.project-name,
.project-tagline {
  color: #1f3b4d;
  text-shadow: none;
}

/* Headings and links */
.main-content h1,
.main-content h2,
.main-content h3,
.main-content h4 {
  color: #3d6f73;
  font-family: "Helvetica Neue", Arial, sans-serif;
}
.main-content a {
  color: #5a6fb8;
}
.main-content a:hover {
  color: #3d6f73;
}

/* Comfortable reading */
.main-content {
  line-height: 1.8;
  font-size: 1.05rem;
}
.main-content img {
  border-radius: 12px;
  box-shadow: 0 4px 14px rgba(61, 111, 115, 0.15);
}

/* Soft "callout" box for definitions and notes */
.main-content blockquote {
  background: #eef6f5;
  border-left: 5px solid #7fb3ae;
  border-radius: 6px;
  color: #2f3e46;
  padding: 0.8rem 1.2rem;
}

/* Gentle table style */
.main-content table th {
  background: #dcebe9;
  color: #2f3e46;
}
```

### File 3: `index.md` (the first page)

Replace every part in **[brackets]** with your own words and details.

```markdown
---
layout: default
title: Cancer Care
---

![Calm sunrise over soft hills](assets/images/hero.svg)

# Welcome to Cancer Care

[Write 2 sentences in your own words: who you are and why you started this blog.]

## Why this blog exists

[Paste your final 5-7 sentence project description from Part 1, Decision 3, rewritten in your own words.]

## What is "late diagnosis"?

> **Late diagnosis** means that a person's cancer was first found at stage III or IV. [Rewrite this definition in your own words and add your source.]

Stage III usually means the cancer is larger or has spread to nearby lymph nodes. Stage IV means it has spread to distant parts of the body. [Add your source link here.]

## Who this blog is for

This blog is written for **caregivers and close family** of people diagnosed with cancer at a late stage. It is also for students and anyone who wants to understand why finding cancer earlier matters.

![Awareness ribbon](assets/images/ribbon.svg){: width="120"}

## What you will find here

| Topic | What it covers |
|---|---|
| **Understanding stages** | What stage I, II, III, and IV mean in plain language |
| **Why cancer is found late** | Common reasons, from symptoms that are easy to miss to gaps in access to care |
| **Supporting someone you love** | What to say, what to avoid, and practical ways to help |
| **Caring for the caregiver** | Looking after your own health and feelings |
| **Warning signs and screening** | What to watch for and when to ask a doctor |

## A message of hope

[Write 2-3 hopeful sentences in your own words. For example: treatments keep improving, many people live well after treatment, and being informed helps families feel less alone.]

## Important note

> This blog is for education only. It is **not medical advice** and cannot replace a doctor or care team. If you or someone you love has symptoms or questions about their health, please talk to a qualified medical professional.

## Sources

- [Your source 1: title and link]
- [Your source 2: title and link]
- [Your source 3: title and link]

*Last updated: [date]*
```

> **Note on the ribbon image:** the `{: width="120"}` part shrinks the ribbon so it does not fill the page. If it does not work on your page, delete that part and the ribbon will simply appear larger.

---

## Part 4: Check that it worked

1. Go to your repo's **Settings → Pages** and confirm the source is **Deploy from a branch**, branch `main`, folder `/ (root)`.
2. Wait 1-2 minutes after each commit.
3. Open `https://username.github.io` (use your real username).
4. Check the list below.

**Checklist before you call it done:**

- [ ] The site shows the title **Cancer Care** and a soft teal and lavender header
- [ ] The sunrise image appears at the top of the page
- [ ] The ribbon image appears under "Who this blog is for"
- [ ] Every bracketed **[placeholder]** has been replaced with your own words
- [ ] Your definition of late diagnosis has a source link
- [ ] Every number or fact has a source, and you checked the number yourself
- [ ] The "not medical advice" note is on the page
- [ ] You read the page out loud once to catch awkward sentences

**If something looks wrong:**

- *Page is plain with no colors:* check that `assets/css/style.scss` starts with the two `---` lines and that the file is in `assets/css/`.
- *Images do not show:* check the file names and folder (`assets/images/hero.svg`) match exactly, including lowercase letters.
- *Site not updating:* wait a couple of minutes, then refresh with Ctrl+Shift+R (Cmd+Shift+R on Mac).
- *Build error:* in the repo, click the **Actions** tab to see the error message and send it to your mentor.

---

## Optional: use real photos instead

Free, calm photos can be downloaded from [Unsplash](https://unsplash.com) or [Pexels](https://www.pexels.com). Try searching for "sunrise", "holding hands", "tea cup window", or "hands support". Choose images without recognizable faces, upload them to `assets/images/`, and update the file name in `index.md`. Always add a short description in the square brackets (the alt text) and credit the photographer in your Sources list.

---

## Sources used to write this guide

- Ismail H, Mokhtar S, El-Mansy H. Factors associated with late-stage diagnosis of breast cancer among Egyptian women. *Journal of Public Health Research.* https://pmc.ncbi.nlm.nih.gov/articles/PMC9335192
- GRAIL. Why Finding Cancers Before It's Too Late Matters More Than Ever. https://grail.com/stories/why-finding-cancers-before-its-too-late-matters-more-than-ever/
- Caregivers of patients with newly diagnosed advanced colorectal cancer. *Oncology Nursing Forum.* https://ons.org/pubs/article/227986/preview
- Impact of cancer on family caregivers, systematic review. *International Journal of Environmental Research and Public Health,* 2023. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10138338/
