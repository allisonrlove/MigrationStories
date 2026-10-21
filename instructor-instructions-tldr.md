---
title: Instructions for Instructors
layout: base
header-image: "/assets/images/immigration_collage.jpg"
header-tier: banner
permalink: /instructors-short
header-title: Instructions for Instructors
header-position: 35% center
---

# Build your class website with Xanthan

This guide helps you set up a website for your class using the Xanthan framework. You will choose a starting template, customize the design, and organize the site so students can contribute their work.

You do not need to know how to code. Xanthan provides working examples and documentation for the technical details. This guide focuses on the decisions you will make as an instructor.

For detailed explanations of Xanthan features, visit the [Xanthan documentation](https://xanthan-web.github.io/).

## Table of Contents

1. [Words you will see](#words-you-will-see)
2. [Plan your website](#plan-your-website)
3. [Start with a Xanthan template](#start-with-a-xanthan-template)
4. [Edit your website](#edit-your-website)
5. [Folders and files](#folders-and-files)
6. [Instructions are hidden inside the folders](#instructions-are-hidden-inside-the-folders)
7. [Design your website](#design-your-website)
8. [Set up student pages](#set-up-student-pages)
9. [Write the student Instructions page](#write-the-student-instructions-page)
10. [Test the student experience](#test-the-student-experience)
11. [Before you share the site](#before-you-share-the-site)
12. [Useful Xanthan references](#useful-xanthan-references)
{: #contents .guide-contents}

{% include nav/scrollspy-toc.html %}

## Words you will see

You do not need to memorize these. Come back here if a word is unfamiliar.

| Word | What it means in plain language |
|---|---|
| **GitHub** | A free website that stores your site's files and publishes your website. |
| **Repository** ("repo") | The folder on GitHub that holds all of your website's files. |
| **Template** | A ready-made starter website you copy and then change. |
| **Markdown** (`.md` file) | A text file where simple symbols format your writing. `## Title` becomes a heading; `**bold**` becomes **bold**. |
| **Front matter** | The small block of settings at the very top of a page, between two lines of `---`. |
| **Include** | A reusable building block (a card, an image with a caption, an audio player) that you place on a page. |
| **CSS** | Files that control how the site looks: colors, fonts, sizes, spacing. |
| **Commit** | Saving your changes to GitHub. You write a short note describing what you changed. |
| **Push** | Sending your saved changes to GitHub so the live site updates. |
| **Path** | The address of a file inside your site, such as `/assets/images/photo.jpg`. |

## Plan your website

Before setting up your site, think about what your students will create and how visitors should experience their work.

**Your project**

- What will students contribute: essays, artwork, objects, research, media, or a combination?
- Will each student have their own page, or will everyone contribute to a shared collection?
- Will the website be public? Consider student privacy, permissions, and image credits.

**Your design**

- What should the website look and feel like? Consider colors, fonts, images, and the overall mood.
- How should visitors find their way around? For example, you could use a homepage with cards linking to student projects and a menu for other pages.
- What information should appear on the homepage, and what should appear on individual pages?

**Your students' experience**

- What information should every student page include?
- Which parts of the website should students be able to edit?
- What should remain consistent across all student pages?
- How should students add their work without having to design a page from scratch?

Sketching a homepage and a sample student page can help you decide how the site should be organized.

## Start with a Xanthan template

You do not need to build your website from scratch. Start with a template that resembles the kind of project you want to create.

Visit [Xanthan's starter sites](https://xanthan-web.github.io/docs/getting-started/templates) to compare the options.

Choose the template that most closely matches your project. You can customize its content, design, navigation, and organization later.

To create your own copy, follow Xanthan's [getting started guide](https://xanthan-web.github.io/docs/getting-started/). It explains how to create a GitHub account, copy a template, and publish your website.

## Edit your website

You can edit your website using the browser-based version of Visual Studio Code (VS Code) through GitHub. This is a good place to start because you do not need to install software.

1. Open your website's repository on GitHub.
2. Press the period key (`.`) to open the browser editor.
3. Use the file list on the left to open and edit your website's files.
4. Save and commit your changes to GitHub.
5. Open the published website to check the result.

For more information, see Xanthan's [getting started guide](https://xanthan-web.github.io/docs/getting-started/).

You can also use desktop VS Code if you prefer to work with files on your computer.

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

**Underscore rule:** folders that start with an underscore (`_includes`, `_data`, `_layouts`) are used by the system that builds your site. Do not rename them.

### Working with folders

- **Create a folder:** in VS Code, right-click in the Explorer and choose **New Folder**. On GitHub's own website, a folder is created by creating a file and typing the folder name followed by a slash, for example `my-folder/index.md`.
- **Create a file:** right-click a folder and choose **New File**. Include the extension, such as `course-resources.md`.
- **Rename or move:** right-click and choose **Rename**, or drag the file to a new folder. If you move an image, update its path anywhere it is used.
- **Add images or audio:** drag them into the folder in VS Code (desktop), or on GitHub choose **Add file → Upload files**.

### Naming rules that prevent most problems

- Use **lowercase** letters, **numbers**, and **hyphens**. No spaces, accents, or special symbols.
- Good: `oral-history-project.md`, `family-photo.jpg`
- Avoid: `Oral History Project FINAL (2).md`, `Family Photo.JPG`
- Always include the file extension (`.md`, `.jpg`, `.mp3`) when you refer to a file, and match capitalization exactly.

### Example: one folder per student

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

Each student has an `index.md` file for their page and can keep images or audio in their own folder. This makes contributions easier to organize and helps students avoid overwriting one another's files.

The folder name becomes part of the web address. For example, `student-pages/student-one/index.md` appears at `your-site/student-pages/student-one/`. Your template may use a different folder name or structure, so follow its existing pattern.

## Instructions are hidden inside the folders

Xanthan includes guidance within many of its files, so you do not have to figure everything out on your own. Before changing a file, look for the comments at the top.

- **In `_includes/`:** Comments explain what each component does, provide a copy-and-paste Usage example, and list the Parameters you can change.
- **In `assets/css/`:** Comments explain what each stylesheet controls and which other files relate to it.
- **In page templates:** Comments often identify which settings to fill in and which parts to leave alone. These can also help you prepare student-facing instructions.
- **In `docs/`:** If your template includes documentation pages, they may explain navigation, design, images, and other features.
- **On the Xanthan website:** The [Xanthan documentation](https://xanthan-web.github.io/) provides additional explanations and examples.

When you open a file you do not recognize, read its comments first. They often tell you what the file does, how to use it, and what you can safely change.

## Design your website

Once your template is working, customize it to suit your class and the work students will produce.

Start with the changes that will have the biggest impact:

- **Colors and fonts:** Choose a readable palette and typography that suit your project.
- **Homepage:** Introduce the project and help visitors find student work.
- **Navigation:** Make important pages easy to find, especially the student Instructions page.
- **Page layouts:** Decide how text, images, captions, and other media should appear.
- **Cards and collections:** Use a consistent way to display and link to student contributions.

Xanthan provides examples and instructions for these features:

- [Colors and fonts](https://xanthan-web.github.io/docs/reference/colors-and-fonts)
- [Themes](https://xanthan-web.github.io/docs/reference/themes)
- [Navigation](https://xanthan-web.github.io/docs/reference/navigation)
- [Component library](https://xanthan-web.github.io/docs/reference/component-library)

### Make the design easy to maintain

Choose a few consistent design choices and use them throughout the website. For example, student pages can share the same heading styles, image sizes, spacing, and page structure.

You do not need to customize every feature. Begin with the overall design and add components as your project needs them.

If you want to make a change but do not know which file controls it, read the comments at the top of the relevant Xanthan files or consult the documentation.

## Set up student pages

A well-designed student page template makes it easier for students to contribute their work while keeping the website consistent.

Instead of asking every student to build a page from scratch, create one example page that students can copy and fill in.

### Choose a structure

For many class projects, a useful structure is:

- A homepage introducing the project.
- A collection page displaying links or cards for student work.
- One page or folder for each student's contribution.
- An Instructions page explaining how to add work.
- Any additional pages your class needs, such as an About page or project resources.

Your structure can be different if your project requires it. The goal is to make it clear where work belongs and how visitors can find it.

### Create a student page template

Build one complete example of the kind of work you want students to submit. Include the elements your assignment requires, such as:

- A title and student name, if appropriate.
- An introduction or summary.
- Sections for the main text.
- Clearly marked spaces for images, captions, and credits.
- Any required dates, sources, tags, or other information.

Use the same layout and design throughout the example. Include sample content that demonstrates what a finished contribution should look like.

If students will contribute images, audio, or other media, decide where those files should go and how students should name them.

### Make adding work straightforward

Whenever possible, use Xanthan's existing components and collection features rather than asking students to create new layouts or write complicated code.

For example, a collection page can display cards that link to individual student pages. Depending on the template, each card may use the page's title, summary, and thumbnail. This allows the collection to grow without requiring you to design a new card for every student.

See Xanthan's [starter sites](https://xanthan-web.github.io/docs/getting-started/templates) and [component library](https://xanthan-web.github.io/docs/reference/component-library) for examples. Check your template's comments to see whether its collection updates automatically or needs to be edited manually.

## Write the student Instructions page

Your website should have an **Instructions** page that students can find easily from the navigation menu. The file is often called `instructions.md`, though the filename may vary by template.

Tailor this page to your assignment so students see only the steps that apply to them. Include:

- **What to create:** Explain the required content and what a finished contribution should include.
- **Where to start:** Identify the exact page or folder students should copy.
- **What to change:** Explain which fields, text, images, and other content students should replace.
- **Where files belong:** Specify the folders for images, audio, or other media, and how files should be named.
- **What to leave alone:** Identify any code, settings, or shared files students should not edit.
- **How to submit:** Explain how students should save their work and check the published page.
- **Assignment requirements:** Include deadlines, citation and credit requirements, privacy considerations, and how to ask for help.

Use short numbered steps and examples where helpful. Remove instructions that do not apply to your assignment.

If students need GitHub accounts or repository access, explain that before they begin.

## Test the student experience

Before sharing the website with your class, pretend you are a student who has never used the site before.

Follow the Instructions page from beginning to end. Check that you can:

- Find the instructions and identify the correct starting template.
- Create a contribution in the intended location.
- Add text and upload images or other required media.
- See the contribution appear in the correct place on the website.
- Understand how to save work and check the published result.

Also check that navigation links work, images display correctly, and the website is readable on a phone as well as a computer.

If possible, ask someone unfamiliar with the project to try the process. Fix confusing steps before students begin.

## What to tell your students

Once your website is ready, give students the site address and explain how they will contribute. Tell them to:

1. **Create a free GitHub account** at [github.com](https://github.com/) before the first work session. Ask them to send you their GitHub username so you can invite them as collaborators if your assignment needs it. (Open the repository, then **Settings → Collaborators → Add people**.)
2. Open the class website and click the **Instructions** tab.
3. **Follow the Instructions tab step by step.** It explains how to add their page, enter their text, and upload images or audio.
4. Save their work (commit) as the instructions describe, wait a few minutes, and check their page on the live site.
5. Ask you for help if stuck, and include which step they were on plus a screenshot or any error message.


## What Amaranth can do for you

Amaranth can work with you every step of the way to help you and your class create this project. 

- Think about if you want Amaranth to visit your class to introduce students to Xanthan and Github; we are avaliable to meet all throughout the semester.
- Plan how you want students to show their work, we have found that having small checkpoints throughout the semester, rather than one big project at the end, works the best.
- Let your students know Amaranth's office hours so that they can reach out for help if they need it. 


## Before you share the site

- [ ] The homepage explains the class project.
- [ ] The design and navigation are consistent and easy to use.
- [ ] Students have a clear page or folder to copy.
- [ ] The collection page displays student work as intended.
- [ ] The Instructions page explains the contribution process.
- [ ] Students know which files they can edit and which they should leave alone.
- [ ] You have tested the process from a student's perspective.
- [ ] You have considered public visibility, student privacy, and image permissions.



## Useful Xanthan references

- [Xanthan home and documentation](https://xanthan-web.github.io/)
- [Getting started](https://xanthan-web.github.io/docs/getting-started/)
- [Starter sites](https://xanthan-web.github.io/docs/getting-started/templates)
- [Site structure](https://xanthan-web.github.io/docs/reference/site-structure)
- [Navigation](https://xanthan-web.github.io/docs/reference/navigation)
- [Component library](https://xanthan-web.github.io/docs/reference/component-library)
- [Colors and fonts](https://xanthan-web.github.io/docs/reference/colors-and-fonts)
- [Themes](https://xanthan-web.github.io/docs/reference/themes)
- [Troubleshooting](https://xanthan-web.github.io/docs/reference/troubleshooting)
