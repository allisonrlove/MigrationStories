---
title: Instructions for Instructors
layout: base
header-image: "/assets/images/immigration_collage.jpg"
header-tier: banner
permalink: /instructors
header-title: Instructions for Instructors
header-position: 35% center
---

# Build a class website with Xanthan

This guide is for instructors who want to create a class website with the Xanthan framework. You do not need previous coding experience. You will start from a template, make changes to ordinary text files, and publish the site through GitHub Pages.

Use this guide alongside the [Xanthan documentation](https://xanthan-web.github.io/). The documentation explains the framework in greater depth; this guide focuses on the decisions and edits instructors commonly need for a class project.

## Before you start: plan the project

Spend a little time deciding what students will contribute and what the finished site should do. These choices determine which template to start from and how much you need to customize.

- **What will students publish?** An essay, an object description, a research project, a profile, or a combination?
- **Will every student have an individual page?** Or will students contribute to a shared page or collection?
- **What media will be included?** Images, audio recordings, video, maps, or links? Decide roughly how many items each student should add.
- **Who is the audience?** Is the site intended for the class, a campus audience, or the general public?
- **What should the site look and feel like?** Think about colors, fonts, images, tone, navigation, and how visitors will move between pages.
- **What should students be responsible for?** Decide which parts they can edit and which parts should remain unchanged so the site stays consistent.
- **What are the requirements?** Set expectations for length, captions, citations, image permissions, accessibility, and deadlines before students begin.

Write down the decisions that affect every student page. You can then build those choices into the template and the student-facing **Instructions** page.

## 1. Choose a template and make your own copy

Start with an existing Xanthan template rather than building the site from scratch. A template provides the page layouts, navigation, styles, and reusable components.

1. Visit the Xanthan website and review the available templates and examples: [Xanthan documentation](https://xanthan-web.github.io/).
2. Choose the template closest to your project. A class-project template is a useful starting point when each student will contribute a separate page. A portfolio or ScrollStory template may be better for other kinds of projects.
3. On the template's GitHub repository, click **Use this template** and create a new repository for your course. Give it a short name using lowercase letters and hyphens, such as `history-class-project`.
4. Open your new repository. It is now your working copy; changes you make here will belong to your course site, not the original template.
5. In the repository's **Settings**, find **Pages** and follow the template's instructions for publishing with GitHub Actions. The first build may take a few minutes.
6. Open the published site and check that it loads before making further changes.

Keep the original template as a reference. If you are unsure what a file does, compare it with the matching file in the template or consult the Xanthan documentation.

## 2. Open Visual Studio Code in your browser through GitHub

You do not need to install software or use the command line. You can edit your website in **Visual Studio Code for the Web**, which runs in your browser and opens your GitHub repository.

1. Sign in to [GitHub](https://github.com/) and open the repository you created from the Xanthan template.
2. Press the period key (`.`) while viewing the repository. This should open the browser-based VS Code editor. If the shortcut does not work, try opening [github.dev](https://github.dev/) and selecting your repository, or use the repository's menu to open it in the web editor.
3. In the left-hand file explorer, click a file such as `index.md` to open it. You can edit text just as you would in a basic text editor.
4. To create a file, use the file explorer's **New File** icon. To create a folder, use **New Folder**. Give files and folders simple names, such as `course-resources.md` or `student-one`.
5. To add an image or other media, return to the repository's regular GitHub page and choose **Add file → Upload files**. Upload the file into the folder where you want to keep it, then make sure the path in your Markdown or front matter matches its location and spelling.
6. When you are ready to save your changes to GitHub, open the **Source Control** panel in the browser editor, enter a short message describing your changes, and choose **Commit & Push** or the available commit/publish option. If prompted to authorize or sign in, follow GitHub's instructions.
7. Open the published website and check your changes. GitHub Pages may take a few minutes to rebuild the site after you commit changes.

**Important:** The browser editor changes files in your GitHub repository; you do not need to download the project or send files back from your computer. You generally cannot preview the complete Jekyll site locally from the browser editor, so check the published GitHub Pages site after each set of changes. If you do not see an update immediately, wait a few minutes and refresh the page.

The browser editor is suitable for editing Markdown, YAML, and CSS files. If you are asked to make a change you do not understand, start with a small edit and keep a copy of the original code so you can undo the change if needed. Do not edit files inside `_site/`; that folder contains generated output and is rebuilt automatically.

## 3. Understand the folders

The file list may look complicated at first. You do not need to understand every file. Start with the ones you are most likely to edit.

| File or folder | What it is for | How often you will use it |
|---|---|---|
| `index.md` | The homepage | Often |
| Other `.md` files | Individual pages, written mostly in Markdown | Often |
| `essays/` or `projects/` | A place to organize student pages | Often, depending on the template |
| `_data/` | Site settings stored in structured text files; top navigation is often here | Occasionally |
| `_includes/` | Reusable components, such as image displays, audio players, cards, and page sections | Usually use existing components; edit only when needed |
| `_layouts/` | Page templates that control the overall structure of a page | Rarely; start with an existing layout |
| `assets/images/` | Images used across the site | Often |
| `assets/css/` | CSS files that control colors, fonts, spacing, and visual design | When customizing the appearance |
| `assets/js/` | Scripts for interactive behavior | Usually not needed for basic editing |
| `_config.yml` | Site-wide settings, such as the site title, base URL, and optional theme | Occasionally |
| `_site/` | Automatically generated website files | Do not edit |

Folders beginning with an underscore are often used by Jekyll or Xanthan to build the website. Leave their names as they are. Folders without an underscore are generally where you organize your own pages and media.

### How folders and file names work

A folder keeps related files together. For example, a class site with individual student essays might be organized like this:

```text
index.md
about.md
instructions.md
instructors.md
_data/
  nav-top.yml
essays/
  student-one/
    index.md
    images/
      source-photo.jpg
  student-two/
    index.md
    images/
      object-photo.jpg
assets/
  css/
  images/
```

This is an example, not a required structure. Follow the structure of the template you chose. Keep each student's page and its media together if that is how the template is designed to work.

Use short file and folder names in lowercase, with hyphens instead of spaces. For example, use `oral-history-project.md` rather than `Oral History Project final.md`. Image names should also be simple, such as `family-photograph.jpg`.

## 4. Edit the homepage and other Markdown pages

Most text pages end in `.md`, which stands for Markdown. Markdown is a simple way to format writing without having to write HTML.

### What is at the top of a page?

Open `index.md`. The block between the two lines of three dashes is called **front matter**. It tells Xanthan the page title, layout, and optional display settings.

```yaml
---
title: "My Class Project"
layout: base
header-image: "/assets/images/class-photo.jpg"
header-tier: banner
header-title: My Class Project
header-position: center center
---
```

This is an example. Use the layout name and settings already used by your chosen template. The image path must match the location and spelling of a real image file in your project.

The content below the closing dashes is the page itself. You can edit ordinary text directly. A few useful Markdown patterns are:

```markdown
# Main heading

## Section heading

A normal paragraph of text.

**Bold text** and *italic text*.

- First list item
- Second list item

[Link to Xanthan](https://xanthan-web.github.io/)
```

The number of `#` characters controls heading level: one `#` is the main heading, two `##` characters are a section heading, and three `###` characters are a smaller heading.

**Be careful with front matter.** Keep the opening and closing `---` lines. Keep each setting on its own line, and do not remove quotation marks from values that contain punctuation unless you know they are not needed.

## 5. Change a header image, its position, or its size

Many Xanthan pages can display a header image. The available options depend on the layout and the template, but these are common settings:

```yaml
header-image: "/assets/images/class-photo.jpg"
header-tier: banner
header-title: My Class Project
header-position: center center
```

- **`header-image`** is the path to the image. Upload the image to the project and check the path carefully.
- **`header-title`** is the text displayed over the image.
- **`header-tier`** controls the general height. Common options are `hero`, `section`, and `banner`.
- **`header-position`** controls which part of the image remains visible when the image is cropped.

For example, change `header-position: center center` to `header-position: 70% center` to shift the visible area horizontally. You can try `left center`, `right center`, `center top`, or `center bottom` as well. If a face or important object is being cropped, adjust this value and refresh the page.

Other settings may include `header-height`, `header-opacity`, or `header-zoom`. The [Pages & Front Matter guide](https://xanthan-web.github.io/docs/reference/pages-and-front-matter) explains the options supported by Xanthan. If your template uses different settings, follow its existing examples.

## 6. Make a new page

A new page is usually a new `.md` file.

1. Decide where the page belongs. A general page such as `about.md` may live beside `index.md`. A student essay may belong inside `essays/student-name/`.
2. Create a new file in that folder. Use a short name, such as `course-resources.md`.
3. Add front matter at the top. Start by copying the front matter from a similar working page and changing the title and other necessary settings.
4. Add the page content below the closing `---` line.
5. Save the file, publish the changes to GitHub, and check the page on the live site.

Example front matter:

```yaml
---
title: Course Resources
layout: base
---
```

The URL is based on the file's location. A root-level file named `course-resources.md` will generally appear at `/course-resources`. A file inside `essays/student-one/index.md` will generally appear under `/essays/student-one/`. The site's `baseurl` can affect the full published address.

### Add the page to the navigation menu

Creating a file does not always add it to the menu automatically. Many Xanthan templates store the top menu in `_data/nav-top.yml`. Open that file and copy the format already used by the other links. For example:

```yaml
- title: "Course Resources"
  url: "/course-resources"
```

Add the entry in the place you want it to appear, keeping the same spacing and indentation as the existing entries. The exact navigation setup may differ by template. See the [Navigation guide](https://xanthan-web.github.io/docs/reference/navigation).

## 7. Use the `_includes` folder

An **include** is a reusable component. Instead of writing all the code for an image, audio player, or layout element on every page, Xanthan lets you insert a component that already exists.

Most instructors should **use existing includes rather than edit the files inside `_includes/`**. The component's file contains the underlying code; the page contains the settings that tell it what to display. Editing an include can change that component everywhere it is used.

For example, a template may use an image include like this:

```liquid
{% raw %}{% include images/figure.html
  image-path="/assets/images/class-photo.jpg"
  caption="Caption and source information"
%}{% endraw %}
```

This is an example of Xanthan include syntax. The exact file name and parameters vary by component and template, so copy a working example from your own project or the [Component Library](https://xanthan-web.github.io/docs/reference/component-library). Change only the parameter values you need, such as the image path or caption.

The folders inside `_includes/` help you identify what a component does. For example, `images/` contains image components, `media/` may contain audio components, `nav/` contains navigation components, and `typography/` contains text treatments. Your template may organize these differently.

### When should you edit an include itself?

Only consider editing an include when you want to change how that component works or looks **everywhere it is used**. Before editing it:

1. Find the include's name in the page, then locate the matching file under `_includes/`.
2. Read the comments in the file. They may explain the available settings and expected format.
3. Search for other pages using the same include so you understand what else could change.
4. Make a copy of the original or use GitHub's version history before making substantial edits.
5. Test every page that uses the component after publishing.

Many files contain comments or instructions near the top. Read these before changing anything. If a file says it is a helper or internal component, leave it alone unless you understand why it needs to change.

## 8. Customize the design in `assets/css/`

CSS is the language that controls the site's appearance: colors, fonts, font sizes, margins, spacing, borders, and more. You can make many visual changes without changing the page text or layout structure.

Start by opening `assets/css/`. Read the comments at the top of a CSS file; they often explain what it controls and whether you should edit it. In general:

- `base.css` contains foundational styles and color variables.
- `typography.css` controls headings, paragraphs, and text formatting.
- Other files may control navigation, cards, images, buttons, or individual components.
- A `themes/` folder, if present, may contain theme files designed for customization.

The exact file names depend on your version of Xanthan. Do not assume every template has the same CSS files.

### Example: change the body font size

Find the rule for the body text in the typography stylesheet. If the file contains a rule like this:

```css
body {
  font-size: 1rem;
}
```

You could change `1rem` to `1.1rem` to make the text a little larger. The example shows the idea; if your stylesheet uses a variable or a different selector, change the existing rule rather than adding a duplicate blindly.

### Example: change heading size

Find the CSS rule for the heading you want to change. For example:

```css
h1 {
  font-size: 2.5rem;
}
```

Changing `2.5rem` to `3rem` makes that heading larger. `h1` usually refers to the main heading; `h2` and `h3` usually refer to section headings and smaller headings. A rule for a specific component may take precedence over these general rules.

### Example: change a color

Many Xanthan versions use CSS variables near the top of `base.css` or a theme file. You may see something like:

```css
:root {
  --bg-page: #f7f4ed;
  --text-body: #282521;
  --accent-primary: #8c3f32;
}
```

The values beginning with `#` are hexadecimal color codes. Replace a value with another color code to change that part of the palette. In this example, `--bg-page` is the page background, `--text-body` is the main text color, and `--accent-primary` is commonly used for links or accents. Your version may use different variable names; look at the comments and where each variable is used.

### Example: change spacing

If an element has a CSS rule such as:

```css
.example-section {
  margin-bottom: 2rem;
}
```

Increasing `2rem` to `3rem` adds more space below it. The selector `.example-section` is only an example; use the actual selector found in your stylesheet.

### Safer ways to customize CSS

1. Search the CSS files for the variable or selector that controls the thing you want to change.
2. Change one or two values at a time.
3. Save and refresh the site to see the effect.
4. If the change has no effect, check whether another stylesheet loads later and overrides it. Also check for spelling mistakes, missing semicolons, and missing braces.
5. Prefer editing a theme or adding a small, clearly labeled override instead of rewriting a large stylesheet.
6. Keep the original Xanthan styles as a reference. The [Colors & Fonts guide](https://xanthan-web.github.io/docs/reference/colors-and-fonts) and [Themes guide](https://xanthan-web.github.io/docs/reference/themes) offer more examples.

## 9. Tailor the student-facing Instructions page

Your students should not have to read the entire Xanthan documentation to complete their assignment. Give them one clear **Instructions** page that explains exactly what they need to do for your course.

Many class templates already include an `instructions.md` file. Open it and adapt the directions to your assignment. Explain:

- What students are making and what the finished page should include.
- Which template or folder they should copy, and what to name their new folder or page.
- Which fields at the top of the file they should edit, such as title, name, summary, and image paths.
- What text, images, audio, video, objects, citations, or other materials are required—and how many.
- Which parts of the template they should replace, and which code or component blocks they should leave in place.
- How to upload media and how to credit its source.
- How to commit and submit their changes through the GitHub browser editor.
- What to do if something does not appear correctly.

Use numbered steps and screenshots if helpful. Include a working example that students can copy. Avoid giving students unnecessary instructions for files they do not need to touch.

Before sharing the site with the class, follow your own student instructions from beginning to end using a test page or a copy of the template. Fix unclear steps and check that a new student page appears where expected.

## 10. What students need to do

Once the website is ready, tell students to:

1. Create or sign in to a **GitHub account**.
2. Open the class website and select the **Instructions** tab.
3. Follow the steps on that page to create or copy their page, enter their content, and add any required media using the browser-based VS Code editor.
4. Commit their changes to GitHub as directed by the instructions, then check the published page after the site rebuilds.
5. Ask for help if they get stuck, including the step they were working on and any error message they see.

Students should follow the instructions on **your class website**, not assume that every Xanthan site uses the same folders or template. Your instructions page is the authoritative guide for your assignment.

## 11. Preview, publish, and troubleshoot

After editing, commit your changes to GitHub from the browser editor. GitHub Pages will rebuild the site. Wait a few minutes, then refresh the live page. A hard refresh can help if the browser is showing an old version.

If something is wrong, check these common causes:

- **The page returns a 404:** confirm the file name, folder, URL, and `baseurl` setting.
- **The page exists but is missing from the menu:** check `_data/nav-top.yml` or the navigation system used by your template.
- **An image is missing:** check that the image is uploaded and the path, capitalization, and file extension match exactly.
- **A style change does not appear:** make sure you edited the correct CSS file, saved it, and checked for later overrides.
- **The site does not rebuild:** look at the repository's **Actions** tab for the build error. Copy the error message before asking for help.
- **An include breaks the page:** compare it with a working example and check the braces, percent signs, quotation marks, and closing `%}`.

For detailed explanations, use the [Xanthan troubleshooting guide](https://xanthan-web.github.io/docs/reference/troubleshooting). You can also ask an AI assistant to explain a file or help with a specific change. Tell it which template you are using, what you want to change, and paste the relevant code. Ask it to preserve your existing text and make the smallest change necessary.

## Useful Xanthan references

- [Xanthan home and documentation](https://xanthan-web.github.io/)
- [Site structure](https://xanthan-web.github.io/docs/reference/site-structure)
- [Pages and front matter](https://xanthan-web.github.io/docs/reference/pages-and-front-matter)
- [Navigation](https://xanthan-web.github.io/docs/reference/navigation)
- [Component Library](https://xanthan-web.github.io/docs/reference/component-library)
- [Colors and fonts](https://xanthan-web.github.io/docs/reference/colors-and-fonts)
- [Themes](https://xanthan-web.github.io/docs/reference/themes)
- [Troubleshooting](https://xanthan-web.github.io/docs/reference/troubleshooting)
