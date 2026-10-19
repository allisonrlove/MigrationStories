---
title: Instructions for Instructors
layout: base
header-image: "/assets/images/immigration_collage.jpg"
header-tier: banner
permalink: /instructors-two
header-title: Instructions for Instructors
header-position: 35% center
---

<style>
  details { border: 1px solid #d8d4cc; border-radius: 8px; padding: 0.6rem 1rem; margin: 1rem 0; background: rgba(0,0,0,0.02); }
  details[open] { padding-bottom: 0.5rem; }
  summary { cursor: pointer; font-weight: 600; }
  summary:hover { text-decoration: underline; }
  blockquote { border-left: 4px solid #6b8e7f; background: rgba(107,142,127,0.08); padding: 0.6rem 1rem; border-radius: 0 6px 6px 0; }
  h2 { margin-top: 2.5rem; }
</style>

# Build and edit your own class website with Xanthan

This guide is for instructors who want to create a class website with the Xanthan framework. **You do not need any coding experience.** You will copy a starter site, change ordinary text files, and publish the result for free on GitHub.

This guide is a companion to the [Xanthan documentation](https://xanthan-web.github.io/). The documentation explains every part of the framework; this guide walks you through the specific steps and decisions an instructor needs for a class project.

> **How to use this guide:** Start with **Plan your project**, then follow the steps in order. You can return to any section using the contents below. You do not need to learn every feature before you begin.
>
> 📂 Sections marked **"Click to expand"** hold extra detail, examples, and reference material. Open them only when you need them.

## 📑 Contents
{: #contents}

| Step | Section |
|:---:|---|
| 1 | [Plan your project](#plan-your-project) |
| 2 | [Start from a template](#start-from-a-template) |
| 3 | [Choose how to edit](#choose-how-to-edit) |
| 4 | [Find your way around the files](#folders-and-files) |
| 5 | [Edit pages and text](#edit-pages-with-indexmd-and-other-md-files) |
| 6 | [Change a header image or position](#change-the-page-header) |
| 7 | [Create pages and organize folders](#make-a-new-page) |
| 8 | [Add images, cards, and other components](#use-the-_includes-folder) |
| 9 | [Customize colors, fonts, and sizes](#change-the-look-with-assetscss) |
| 10 | [Prepare the student Instructions page](#write-the-student-instructions-page) |
| 11 | [Tell students how to begin](#what-to-tell-your-students) |
| 12 | [Troubleshoot common problems](#check-your-work-and-fix-problems) |
| 📖 | [Words you will see](#words-you-will-see) |
| 🔗 | [Useful Xanthan references](#useful-xanthan-references) |

---

## Words you will see

You do not need to memorize these. Come back here if a word is unfamiliar.

<details markdown="1">
<summary><strong>Click to expand: glossary of terms</strong></summary>

| Word | What it means in plain language |
|---|---|
| **GitHub** | A free website that stores your site's files and publishes them as a website. |
| **Repository** ("repo") | The folder on GitHub that holds all of your website's files. |
| **Template** | A ready-made starter website you copy and then change. |
| **Markdown** (`.md` file) | A text file where simple symbols format your writing. `## Title` becomes a heading; `**bold**` becomes **bold**. |
| **Front matter** | The small block of settings at the very top of a page, between two lines of `---`. |
| **Include** | A reusable building block (a card, an image with a caption, an audio player) that you place on a page. |
| **CSS** | Files that control how the site looks: colors, fonts, sizes, spacing. |
| **Commit** | Saving your changes to GitHub. You write a short note describing what you changed. |
| **Push** | Sending your saved changes to GitHub so the live site updates. |
| **Path** | The address of a file inside your site, such as `/assets/images/photo.jpg`. |

</details>

[↑ Back to contents](#contents)

---

## Plan your project

Before you touch the template, decide what you want the site to do and what you want it to look like. A short plan now can save time later. Your answers will also help you write the student-facing Instructions page.

Use this checklist to make the main decisions before you build.

<details markdown="1">
<summary><strong>🎯 What is the site for?</strong></summary>

- Will it showcase **objects** (artifacts, artworks, places), students' **writing**, or **both**?
- Is it for your class only, for your campus, or for the **public**? Remember that a public site means student work can be found by anyone, so decide how you will handle student names, permissions, and privacy.

</details>

<details markdown="1">
<summary><strong>✍️ What will each student contribute?</strong></summary>

- Will every student have their **own page** (for example, an essay page)? Or will students add to one shared page?
- Will students add **images**? How many (for example, exactly 3)?
- Will students add **audio**, **video**, or a **map**?
- How long should the writing be? Are captions, citations, image credits, or alt text (a written description of an image for people who can't see it) required?

</details>

<details markdown="1">
<summary><strong>🎨 How should it look and feel?</strong></summary>

- Rough colors, mood, and a header image you like.
- How visitors will move around: a top menu, a homepage with cards linking to every student page, or both.

</details>

<details markdown="1">
<summary><strong>👥 Who is responsible for what?</strong></summary>

- Which parts can students edit, and which should they leave alone so the site stays consistent?
- What are the deadlines?

</details>

> 💡 **A good habit:** sketch the site on paper. Draw the homepage, one student page, and the menu. Then pick the template closest to your sketch.

[↑ Back to contents](#contents)

---

## Start from a template

A template is a complete working website. You will make your own copy so you can change it freely without affecting the original.

1. Create a free account at [github.com](https://github.com/) if you do not have one, and sign in.
2. Go to the [Xanthan starter sites page](https://xanthan-web.github.io/docs/getting-started/templates) and choose the template closest to your plan. Each template is explained there.
3. On the template's GitHub page, click the green **Use this template** button, then **Create a new repository**.
4. Give the repository a short name in lowercase with hyphens, such as `history-class-project`. Choose your own account as the owner.
5. Choose **Public** if you want the site to be viewable by anyone. (Free GitHub Pages sites are public.)
6. Click **Create repository**. You now have your own copy.
7. Publish the site: in your new repository click **Settings**, then **Pages**, and set the source to **GitHub Actions** (or follow the exact steps in the template's README). Wait a few minutes. The address of your site will appear on that page.
8. Open your live site and confirm it loads. Now you are ready to edit.

**Tip:** Keep the original template open in another tab. If you ever break something, you can compare your file to the original.

[↑ Back to contents](#contents)

---

## Choose how to edit

You can edit your site in a browser or use the desktop version of VS Code on your computer. **If you are new to this, start with the browser editor for small text changes. Use desktop VS Code if you plan to customize the design, manage lots of images, or work with many files.** Both approaches change the same website files.

<details markdown="1">
<summary><strong>Option A: Edit in your browser</strong> (no installation, best for small text changes)</summary>

This option does not require installing software.

1. Open your repository on GitHub.
2. Press the **period key (`.`)** on your keyboard. The browser version of Visual Studio Code (VS Code) opens with your files. You can also open `github.dev` and choose your repository.
3. In the left column, called the **Explorer**, click a file such as `index.md` to open it.
4. Make your changes and save the file.
5. Open the **Source Control** icon on the left (it looks like a branching line). Enter a short message describing the change, such as `Update homepage text`, then use the available **Commit** option to save it to GitHub. The exact button labels can vary.
6. Wait a few minutes, then refresh your live website.

The browser editor does not provide a full preview of your finished Xanthan site. Check the published website after each change. For bigger design changes, desktop VS Code is usually easier.

</details>

<details markdown="1">
<summary><strong>Option B: Edit on your computer with desktop VS Code</strong> (more control for design and many files)</summary>

The desktop version of VS Code is free and is the better choice when you want more control over the design. It makes it easier to manage folders and images, search across the site, and make coordinated changes to multiple files.

#### One-time setup

1. Install **[Visual Studio Code](https://code.visualstudio.com)**. Download it, open the installer, and accept the defaults.
2. Install **[GitHub Desktop](https://desktop.github.com)**. Open it and sign in with your GitHub account.
3. In GitHub Desktop choose **File → Clone repository**, pick your class site from the list, choose a place on your computer (such as Documents), and click **Clone**.
4. In GitHub Desktop click **Open in Visual Studio Code**. Your whole site opens.

#### Everyday editing

1. Open GitHub Desktop and click **Fetch origin** or **Pull origin** (this brings in any changes students have made).
2. Click **Open in Visual Studio Code**.
3. Use the Explorer on the left to open files. Edit and save with **Ctrl+S** (Windows) or **Cmd+S** (Mac).
4. When you are happy, switch to GitHub Desktop. You will see a list of changed files. Type a short summary at the bottom left, click **Commit to main**, then click **Push origin**.
5. Wait a few minutes and refresh the live site.

#### VS Code skills worth knowing

- **Find and replace everywhere:** press **Ctrl+Shift+F** (Windows) or **Cmd+Shift+F** (Mac) to search every file. This is the best way to find where a color, a word, or a setting lives.
- **Open any file quickly:** press **Ctrl+P** (Cmd+P on Mac) and start typing the file name.
- **Undo:** **Ctrl+Z** (Cmd+Z). If you have saved and committed a mistake, GitHub Desktop's **History** tab lets you review and revert it.
- **Color previews:** VS Code shows a small colored square beside color codes in CSS files. Click it to pick a new color.
- **Preview Markdown:** open an `.md` file and press **Ctrl+Shift+V** to see roughly how the text will look.

#### Optional: preview the site on your computer

You can see changes instantly, before publishing, by running the site locally. This takes some extra setup, so skip it until you want it. Follow the [Working Locally guide](https://xanthan-web.github.io/docs/reference/working-locally).

</details>

### AI helpers

<details markdown="1">
<summary><strong>Click to expand: getting help from an AI assistant</strong></summary>

If a change feels intimidating, you can ask an AI assistant for help. Tell it which Xanthan template you use, exactly what you want to change, and paste the relevant file. Ask it to "make the smallest change necessary and keep my existing text." Always check the result on your site. See the [Xanthan AI guide](https://xanthan-web.github.io/docs/using-ai/).

</details>

[↑ Back to contents](#contents)

---

## Folders and files

A folder is a container for related files, just like a folder on your computer. Your website is a collection of folders and files. **You do not need to understand everything at once.** Start with the homepage, the student page template, `_includes/`, and `assets/css/`; learn the other folders when you need them.

| File or folder | What it does | How often you will touch it |
|---|---|---|
| `index.md` | The homepage. | Often |
| Other `.md` files (such as `about.md`) | One page each. | Often |
| A folder for student pages (often called `essays/` or `projects/`; the name depends on the template) | Holds one folder per student page. | Often |
| `instructions.md` | The student-facing **Instructions** page. | Edit once to fit your assignment |
| `_data/` | Site menus and other lists. `nav-top.yml` controls the top menu. | Sometimes |
| `_includes/` | Reusable building blocks (cards, images, audio players). | Use often; edit rarely |
| `_layouts/` | Page designs that decide the overall structure of a page. | Rarely |
| `assets/images/` | Images shared by the whole site. | Often |
| `assets/css/` | Files that control colors, fonts, and sizes. | When customizing the look |
| `assets/js/` | Scripts for interactive features. | Rarely |
| `_config.yml` | Site-wide settings, such as the site title. | Occasionally |

> ⚠️ **Underscore rule:** folders that start with an underscore (`_includes`, `_data`, `_layouts`) are used by the system that builds your site. Do not rename them.

### Working with folders

<details markdown="1">
<summary><strong>Click to expand: create, rename, move, and upload</strong></summary>

- **Create a folder:** in VS Code, right-click in the Explorer and choose **New Folder**. (On GitHub's own website, a folder is created by creating a file and typing the folder name followed by a slash, for example `my-folder/index.md`.)
- **Create a file:** right-click a folder and choose **New File**. Include the extension, such as `course-resources.md`.
- **Rename or move:** right-click and choose **Rename**, or drag the file to a new folder. If you move an image, update its path anywhere it is used (use Find in files to locate those places).
- **Add images or audio:** drag them into the folder in VS Code (desktop), or on GitHub choose **Add file → Upload files**.

</details>

### Naming rules that prevent most problems

- Use **lowercase** letters, **numbers**, and **hyphens**. No spaces, accents, or special symbols.
- ✅ Good: `oral-history-project.md`, `family-photo.jpg`
- ❌ Avoid: `Oral History Project FINAL (2).md`, `Family Photo.JPG`
- Always include the file extension (`.md`, `.jpg`, `.mp3`) when you refer to a file, and match capitalization exactly.

### Example: one folder per student

<details markdown="1">
<summary><strong>Click to expand: sample folder layout</strong></summary>

Many class templates give each student their own folder so their writing and media stay together:

```text
index.md
about.md
instructions.md
student-pages/
  index.md
  student-one/
    index.md
    images/
      object-photo.jpg
    audio/
      interview-clip.mp3
  student-two/
    index.md
    images/
      source-photo.jpg
```

The folder name becomes part of the web address. `student-pages/student-one/index.md` appears at `your-site/student-pages/student-one/`. Follow your own template's structure.

</details>

[↑ Back to contents](#contents)

---

## Instructions are hidden inside the folders

Xanthan is built to explain itself. Many files contain notes written for you. Look for them before you change anything.

<details markdown="1">
<summary><strong>Click to expand: where to find the built-in notes</strong></summary>

- **In `_includes/`:** each file begins with a note (between `{% raw %}{% comment %}{% endraw %}` and `{% raw %}{% endcomment %}{% endraw %}`) that lists what the building block does, a copy-and-paste **Usage** example, and every **Parameter** you can change.
- **In `assets/css/`:** each CSS file begins with a comment box (between `/*` and `*/`) that says what the file controls and which other files relate to it.
- **In page templates** (such as a student page template): the top of the file usually has comments like "Step 1 – fill in the information below." These are written for students and for you.
- **In `docs/`:** the site's own documentation pages (if your template includes them) cover navigation, colors and fonts, images, and troubleshooting.
- **The Xanthan website:** [xanthan-web.github.io](https://xanthan-web.github.io/) has a page for every component.

</details>

> 💡 When you open a file you do not recognize, read the comment at the top first. It usually tells you exactly what you need.

[↑ Back to contents](#contents)

---

## Edit pages with index.md and other .md files

Every page on your site is a text file ending in `.md` (Markdown). `index.md` in the main folder is your **homepage**. `about.md` is the About page. An `index.md` inside a folder is the main page of that folder.

### The two parts of a page

Open `index.md`. A page has two parts:

```text
---
title: "My Class Project"
layout: base
header-title: My Class Project
---

# Welcome

This is the page text.
```

1. **Front matter** is the part between the two `---` lines. It holds settings: the title, the layout, header image, and so on.
2. **Content** is everything below the second `---`. It is the writing visitors see.

**Rules for front matter:** keep both `---` lines; keep each setting on its own line; keep the quotation marks and the space after each colon. Change only what comes after the colon.

### Markdown cheat sheet

<details markdown="1">
<summary><strong>Click to expand: Markdown cheat sheet</strong></summary>

Type this on the left to get the result on the right.

| You type | You get |
|---|---|
| `# Big heading` | Largest heading (use once per page) |
| `## Section heading` | Section heading |
| `### Smaller heading` | Smaller heading |
| `**bold**` | **bold** |
| `*italic*` | *italic* |
| `- item` (on each line) | A bullet list |
| `1. item` (on each line) | A numbered list |
| `[Link text](https://example.com)` | A link |
| `[About page](/about)` | A link to another page on your site |
| `![Describe the image](/assets/images/photo.jpg)` | A basic image |
| `> quoted text` | A block quote |
| A blank line | Starts a new paragraph |

Leave a blank line between paragraphs, headings, and lists. If formatting looks wrong, a missing blank line is the most common cause.

</details>

### Example: edit your homepage

1. Open `index.md`.
2. Change the words after `title:` and `header-title:` to your course name.
3. Replace the sample paragraph under the front matter with your own welcome text.
4. Save and commit. Refresh the live site to see the result.

[↑ Back to contents](#contents)

---

## Change the page header

Most pages show a large banner at the top with an image and title. You control it with front matter.

```yaml
header-image: "/assets/images/class-photo.jpg"
header-tier: banner
header-title: My Class Project
header-position: center center
```

- **`header-image`**: the image path. The file must exist at exactly that location.
- **`header-title`**: the large words on the banner.
- **`header-tier`**: how tall the banner is. Try `hero` (tallest), `section`, or `banner` (shortest).
- **`header-position`**: which part of the image stays visible when it is cropped.

### Examples

<details markdown="1">
<summary><strong>Click to expand: header examples</strong></summary>

**Make the banner taller or shorter:** change `header-tier: banner` to `header-tier: hero`, or the reverse.

**Move the image so a face or object isn't cut off:**

```yaml
header-position: center top       # shows the top of the image
header-position: center bottom    # shows the bottom
header-position: 70% center       # slides the image to show more of its left side
header-position: 20% center       # shows more of its right side
```

**Swap the banner picture:** upload a new image into `assets/images/`, then change the `header-image` path. Wide images (wider than they are tall) work best.

**Remove the banner:** delete the `header-` lines, or use a layout that has no banner. Check the [Pages and front matter guide](https://xanthan-web.github.io/docs/reference/pages-and-front-matter) for all available header settings.

</details>

> 💡 Anything after a `#` in front matter is a note to humans, and the site ignores it. You can add `#` in front of a line to switch it off without deleting it.

[↑ Back to contents](#contents)

---

## Make a new page

### A simple page (such as "Course Resources")

1. In the main folder, create a new file named `course-resources.md`.
2. Paste this at the top and change the title:

```yaml
---
title: Course Resources
layout: base
---
```

3. Write your content below the closing `---`.
4. Save and commit. The page appears at `your-site/course-resources`.

Tip: the safest approach is to copy an existing page, rename it, and change its title and text.

### A page inside a folder

Create a folder, then an `index.md` file inside it. For example `readings/index.md` appears at `your-site/readings/`. Use folders when a section will have several pages or images.

### Add the page to the menu

A new page does not automatically appear in the menu. Open `_data/nav-top.yml` and add an entry, matching the spacing of the entries around it:

```yaml
- title: "Course Resources"
  url: "/course-resources"
```

The order of entries is the order of the menu. To remove a page from the menu, delete its entry (the page itself still exists). See the [Navigation guide](https://xanthan-web.github.io/docs/reference/navigation) for dropdown menus and side menus.

### A student page from the template

If your template includes a student page template (a sample folder with an `index.md`, an `images` folder, and so on), students make their page by **copying that folder**, renaming the copy, and filling in the form at the top of `index.md`. Often the homepage or listing page then shows a card for each student page **automatically**, so you do not need to add them by hand. Check the comments in the template to see how yours works. To hide an unfinished page, look for a `draft: true` setting.

[↑ Back to contents](#contents)

---

## Use the _includes folder

An **include** is a reusable building block. Instead of writing complicated code, you add a short line to your page and the include builds the card, image, audio player, or quotation for you.

Think of it like asking a typesetter for "a gallery here": you do not need to know how a gallery is built.

### What an include looks like on a page

```liquid
{% raw %}{% include images/figure.html
  image-path="/assets/images/photo.jpg"
  caption="A short caption and credit"
%}{% endraw %}
```

Parts of this line:

- `{% raw %}{% include{% endraw %}` and `{% raw %}%}{% endraw %}` mark the start and end. Keep them exactly.
- `images/figure.html` is the include's file name inside the `_includes` folder.
- `image-path=` and `caption=` are **parameters**: choices you can change. The text inside the quotation marks is yours to edit.

### How to use any include in four steps

1. Browse `_includes/` and find the folder that fits (`images/`, `cards/`, `typography/`, `essay/`, `layout/`, and so on).
2. Open the file and read the note at the top. Find **Usage** and **Parameters**.
3. Copy the Usage example into your page.
4. Change the values in quotation marks. Optional parameters can simply be left out.

### Example: put an image on a page

<details markdown="1">
<summary><strong>Click to expand: put an image on a page</strong></summary>

Upload a picture to `assets/images/`. Then, on the page:

```liquid
{% raw %}{% include images/figure.html
  image-path="/assets/images/photo.jpg"
  image-width="60%"
  caption="Describe and credit the image."
  alt-text="Describe the picture for people who cannot see it."
%}{% endraw %}
```

- `image-width` makes the picture bigger or smaller (try `40%`, `60%`, or `100%`).
- `caption` appears below the picture.
- `alt-text` is read aloud by screen readers. Always include it.

</details>

### Example: an image beside text

<details markdown="1">
<summary><strong>Click to expand: an image beside text</strong></summary>

```liquid
{% raw %}{% include images/figure-wrap.html
  image-path="/assets/images/photo.jpg"
  image-position="right"
  image-width="35%"
  caption="Caption and credit."
  text="Your paragraph goes here. It appears next to the image."
%}{% endraw %}
```

Change `image-position` to `left` or `right` to switch sides.

</details>

### Example: a card grid

<details markdown="1">
<summary><strong>Click to expand: a card grid</strong></summary>

A **card** is a small preview with a picture, a title, a short description, and a link. A **card grid** shows many cards in a tidy layout, useful for a homepage or a collection of student work.

Cards are made from the information at the top of other pages. The grid reads each page's `title`, `summary`, and `thumbnail` (a small image) and builds the cards for you. A typical call looks like this:

```liquid
{% raw %}{% include cards/card-grid.html cards=pages show-tags=true %}{% endraw %}
```

Read the top of `_includes/cards/card-grid.html` to see every option. Some starter sites also include an automatic grid (for example `cards/essay-grid.html`) that shows one card for every student page without any extra setup.

To control how a page's card looks, change that page's front matter, for example:

```yaml
title: "Object: The Blue Teapot"
summary: "A short, one-sentence description."
thumbnail: images/teapot.jpg
```

If a card is missing or looks wrong, check: Is there a `title`? Does the thumbnail file exist at that path? Is the page marked as a draft?

</details>

### Example: other helpful includes

<details markdown="1">
<summary><strong>Click to expand: more includes you can use</strong></summary>

Look in these folders to see what is available. Each file explains itself.

| Include | What it adds |
|---|---|
| `typography/pullquote.html` | A large highlighted quotation |
| `typography/alert.html` | A colored note box (info, warning, success) |
| `images/carousel.html` | A slideshow of images |
| `images/juxtapose.html` | A slider to compare two images |
| `essay/audio.html` / `media/audio.html` | An audio player with a caption |
| `essay/video.html` | An embedded video |
| `maps/` | Interactive maps |
| `layout/` | Banners, feature rows, and page sections |

The [Component Library](https://xanthan-web.github.io/docs/reference/component-library) shows a picture and example of each one.

</details>

### Editing an include (advanced)

<details markdown="1">
<summary><strong>Click to expand: advanced, editing an include</strong></summary>

You rarely need to change the files in `_includes`. Changing one changes it **everywhere it is used**. If you do edit one:

1. Read its top note first.
2. Use Find in files (Ctrl+Shift+F) to see which pages use it.
3. Change one small thing, save, and check the live site.
4. Use GitHub Desktop's **History** tab to undo it if something breaks.

The most common mistakes are a missing quotation mark, missing `%}`, or a misspelled parameter name.

</details>

[↑ Back to contents](#contents)

---

## Change the look with assets/css

CSS is the part of the site that controls its appearance: colors, fonts, text sizes, spacing, borders, and layout. The files usually live in `assets/css/`. **Read the comment at the top of a CSS file before editing it.** It explains what that file controls.

### Where to find things

Open `assets/css/` and read the comment at the top of each file. Typical files:

| File | Controls |
|---|---|
| `base.css` | The color palette, page width, and basic building blocks |
| `typography.css` | Text: headings, paragraphs, quotes |
| `nav.css` | The top menu |
| `cards.css` | Cards |
| `images.css` | Images and captions |
| `footer.css` | The footer |
| `themes/` (folder) | Complete looks you can switch between |

File names vary slightly among starter sites, so rely on the comments at the top of each file.

### The easiest way to restyle: change the colors

Near the top of `base.css` (or a file in `themes/`) is a list of **variables**: names with values.

```css
:root {
  --bg-page: #f5f3f0;
  --text-body: #2d3e35;
  --accent-primary: #6b8e7f;
}
```

The `#f5f3f0` style values are **color codes**. Change one and the whole site updates. To choose a color, search for "color picker" online, or click the small colored square VS Code shows next to the code. Change one color, save, and look at the result before changing more.

See the [Colors and fonts guide](https://xanthan-web.github.io/docs/reference/colors-and-fonts) and [Themes guide](https://xanthan-web.github.io/docs/reference/themes) for the full list of variable names and ready-made themes.

### The safest place to make changes

Instead of changing several framework files, use the site's theme override file if the template provides one. Check `_config.yml` for a setting such as `theme_css:` to find the active theme file, then look in `assets/css/themes/`. Add your overrides at the **bottom of the active theme file** so they are easy to find and adjust. If your template does not use a theme file, follow the comments in its CSS files and the Xanthan documentation.

### Examples you can copy

<details markdown="1">
<summary><strong>Click to expand: copy-and-paste CSS examples</strong></summary>

Each example goes at the bottom of your theme file (or the file named in the example). Save, refresh, and check. Remove the lines to undo.

**Make all body text bigger**

```css
body {
  font-size: 1.15rem;
}
```

`1rem` is normal size. `1.15rem` is a little larger, `1.3rem` is larger still.

**Make main headings bigger or smaller**

```css
h1 {
  font-size: 3rem;
}
h2 {
  font-size: 2rem;
}
```

**Change the heading font**

```css
:root {
  --font-heading: 'Georgia', serif;
}
```

Fonts must be installed on the visitor's device, or loaded from a font service such as Google Fonts. Ordinary choices that work everywhere: `Georgia`, `Times New Roman`, `Arial`, `Verdana`. Many themes list their fonts in `--font-heading` and `--font-body`.

**Change link color**

```css
a {
  color: #8c3f32;
}
```

**Center a heading**

```css
h1 {
  text-align: center;
}
```

**Add space below paragraphs**

```css
p {
  margin-bottom: 1.5rem;
}
```

**Make the page text column wider or narrower:** search for `content` and `max-width` in `base.css`. Read the comments there before changing it.

**Change the banner height or image position:** this is controlled on each page in the front matter. See "Change the page header" above.

</details>

### CSS words to recognize

<details markdown="1">
<summary><strong>Click to expand: CSS vocabulary</strong></summary>

| Word | Meaning |
|---|---|
| `font-size` | How big the text is. `rem` is a relative size unit. |
| `color` | Text color. |
| `background` / `background-color` | Color behind something. |
| `margin` | Empty space outside an element. |
| `padding` | Empty space inside an element. |
| `text-align` | `left`, `center`, or `right`. |
| `font-weight` | `400` is normal, `700` is bold. |

</details>

### If your CSS change does nothing

<details markdown="1">
<summary><strong>Click to expand: CSS troubleshooting</strong></summary>

- Did you save, commit, push, and wait a few minutes? Try a hard refresh (**Ctrl+Shift+R**, or **Cmd+Shift+R** on Mac).
- Is each rule inside curly braces `{ }`, and does every line end in a semicolon `;`?
- Is another rule overriding it? Search all files for the same name (Ctrl+Shift+F). If you edited an earlier file and a theme file overrides it, edit the theme file instead.
- Undo your last change and try again with only one change.

</details>

[↑ Back to contents](#contents)

---

## Write the student Instructions page

Your site should have an **Instructions** page that students can open from the navigation menu. It is usually a file such as `instructions.md`, though the filename may vary by template. The template should already provide a starting point. **Tailor it to your assignment** so students see only the steps that apply to them.

Open `instructions.md` and revise it using your planning answers. Make sure it states:

- What students are making, and what the finished page must include.
- How many images, audio clips, or other items are required, and any limits.
- Exactly which folder to copy and what to name their copy (for example, `firstname-lastname`).
- Which settings at the top of their file to fill in (name, title, summary, image names).
- Which parts of the template to replace and which to leave alone.
- How to upload images or audio, how to name them, and how to credit sources.
- How to save (commit) their work and how to check it on the live site.
- Whether the work may be shown publicly, and what permissions are needed for photographs or interviews.
- Your deadlines and how to ask for help.

Write for someone who has never used GitHub. Use numbered steps, short sentences, and a finished example. Remove steps that do not apply (for example, delete the audio steps if no one will add audio).

> ✅ **Test it yourself.** Before the class begins, follow your own instructions from start to finish as if you were a student, ideally in a copy of the site. Fix any step that is confusing.

[↑ Back to contents](#contents)

---

## What to tell your students

Once your website is ready, give students the site address and explain how they will contribute. Tell them to:

1. **Create a free GitHub account** at [github.com](https://github.com/) before the first work session. Ask them to send you their GitHub username so you can invite them as collaborators if your assignment needs it. (Open the repository, then **Settings → Collaborators → Add people**.)
2. Open the class website and click the **Instructions** tab.
3. **Follow the Instructions tab step by step.** It explains how to add their page, enter their text, and upload images or audio.
4. Save their work (commit) as the instructions describe, wait a few minutes, and check their page on the live site.
5. Ask you for help if stuck, and include which step they were on plus a screenshot or any error message.

Remind students that the **Instructions tab on your site** is the guide for your assignment. They do not need to read the Xanthan documentation.

[↑ Back to contents](#contents)

---

## Check your work and fix problems

After each set of changes, commit, wait one to three minutes, then refresh. Common problems:

| Problem | What to check |
|---|---|
| The page shows an error (404) | File name, folder, and location. Is the page in the right folder? |
| A page is missing from the menu | Add it to `_data/nav-top.yml`. |
| An image does not show | The file is uploaded; the path, spelling, capitalization, and extension all match. |
| Formatting looks wrong | A missing blank line (Markdown), or a missing `---` or quotation mark (front matter). |
| A CSS change does not appear | You edited the right file, saved, committed, and refreshed hard. |
| A card is missing | The page has a `title`, correct `thumbnail` path, and is not marked `draft: true`. |
| The whole site stopped updating | On GitHub, open the **Actions** tab. A red mark means a build error; open it and read the message. It often names the file and line with the problem. |

**To undo a mistake:** in GitHub Desktop, open **History**, right-click the commit, and choose **Revert**. On GitHub, open the file and click **History** to see earlier versions.

For more help, see the [Xanthan troubleshooting guide](https://xanthan-web.github.io/docs/reference/troubleshooting).

[↑ Back to contents](#contents)

---

## Before you share the site

Use this quick checklist before students begin:

- [ ] The homepage explains the class project.
- [ ] The navigation links work and students can find the Instructions page.
- [ ] You have tested the student workflow from beginning to end.
- [ ] Sample pages, cards, images, and media display correctly.
- [ ] The Instructions page says exactly what students should create, where files belong, and how to save their changes.
- [ ] You have considered public visibility, names, image permissions, and privacy.
- [ ] You have a backup or know how to use GitHub history to undo a change.

[↑ Back to contents](#contents)

---

## Useful Xanthan references

- [Xanthan home and documentation](https://xanthan-web.github.io/)
- [Starter sites](https://xanthan-web.github.io/docs/getting-started/templates)
- [Site structure](https://xanthan-web.github.io/docs/reference/site-structure)
- [Pages and front matter](https://xanthan-web.github.io/docs/reference/pages-and-front-matter)
- [Navigation](https://xanthan-web.github.io/docs/reference/navigation)
- [Component Library](https://xanthan-web.github.io/docs/reference/component-library)
- [Colors and fonts](https://xanthan-web.github.io/docs/reference/colors-and-fonts)
- [Themes](https://xanthan-web.github.io/docs/reference/themes)
- [Working locally](https://xanthan-web.github.io/docs/reference/working-locally)
- [Using AI](https://xanthan-web.github.io/docs/using-ai/)
- [Troubleshooting](https://xanthan-web.github.io/docs/reference/troubleshooting)
