---
title: Instructions for Students
layout: base
header-image: "/assets/images/immigration_collage.jpg"
header-tier: banner
header-title: Instructions for Students
header-position: 35% center
---

# How to publish your migration story

You do not need to know how to code. You will copy a template, type your own words, and upload your pictures and audio. Your essay then appears on the home page automatically.

## Step 1: Open the editor

1. Go to this project's page on GitHub and sign in.
2. Press the **period key (`.`)** on your keyboard. A code editor opens in your browser.
3. Your files are listed on the left.

## Step 2: Copy the template

1. In the left list, open the **`essays`** folder. Find the **`template`** folder.
2. Right-click **`template`** and choose **Copy**. Right-click the **`essays`** folder and choose **Paste**.
3. Right-click the new folder and choose **Rename**. Use your name in lowercase with hyphens, like `maria-lopez`. No spaces or capital letters.

Your folder looks like this:

```
essays/
  maria-lopez/
    index.md        <- your essay
    images/         <- your pictures
    audio/          <- your MP3 clip
```

## Step 3: Fill in the top of your essay

Open `index.md` in your folder. At the very top, between the two lines of dashes, type your information after each colon. Keep the quotation marks.

| Line | What to write |
|---|---|
| `title` | The title of your project |
| `student` | Your name |
| `kicker` | A short label for the home page card, like "Village to City" |
| `summary` | One sentence about your story |
| `lead-image` | The file name of your main image |
| `lead-image-alt` | A short description of the image for people using screen readers |
| `lead-image-caption` | Caption and source citation for the main image |

## Step 4: Write your essay

Your essay has the same parts, in the same order, as the template. Replace each paragraph with your own writing. Keep the lines that start with `##`, but change the words after them to your own subheaders. Anything inside a `{% raw %}{% include ... %}{% endraw %}` block is a picture, audio clip, or video; you only change the text inside the quotation marks.

| Order | Part | What to write | Length |
|---|---|---|---|
| 1 | **Title** | The title of your project. It goes in the `title` line at the top. | Short and specific |
| 2 | **Lead image** | One high-quality, small-ish photograph or object that introduces your family. Set in the top lines (`lead-image`). The caption must cite the source. | Caption: one or two lines |
| 3 | **Introduction** | Introduce your family: who they are, where they came from, where they went, and when. | 100-120 words |
| 4 | **Subheader 1: Historical context and impacts** | A short subheader, then a paragraph that connects your family's story to larger history using secondary sources from class. Cite them in Chicago style. | Subheader 4-8 words; paragraph 150-250 words |
| 5 | **Subheader 2: Personal context** | A subheader, then your 1-2 minute audio (MP3) or video (YouTube) clip from the oral history, with a caption and citation. | Caption 10-25 words |
| 6 | **Subheader 3: The oral history as a whole** | Describe the journey as a whole, the family, one important object, and questions of identity and place. Follow it with a second image and citation. | Paragraph 300-350 words; image caption 20-30 words |
| 7 | **Subheader 4: Other migration stories** | Compare your family's story with others from class, then add a third image and citation. | Paragraph 125-175 words; image caption 20-30 words |
| 8 | **Concluding subheader** | Reflect on what you learned about your family, migration, and history. | Final paragraph 70-85 words |
| 9 | **References** | List your oral history interview and the secondary sources you cited. | Chicago style |

Tips:

- Write your words in the template's paragraphs, directly under each subheader. Do not move or delete the picture, audio, and video blocks; just edit them.
- Your lead image and the other images should be sharp and well lit. Always say where each one came from.
- The summary you wrote in Step 3 appears under your title and on your card on the home page, so keep it to one clear sentence.
- To see how finished essays look, open any of the sample essays on the Essays page. They are placeholders only, so replace everything with your own work.

## Step 5: Add your pictures

1. Right-click the **`images`** folder inside your folder and choose **Upload...**. Pick your image.
2. In `index.md`, find the picture block you want to change and type your image's file name:

```
{% raw %}{% include essay/figure.html
  image="images/my-photo.jpg"
  alt="Short description of the picture"
  caption="What it shows and where it came from."
%}{% endraw %}
```

Use lowercase file names with hyphens and no spaces, like `grandmothers-suitcase.jpg`. Add `size="small"` or `size="large"` if you want a different size.

## Step 6: Add your audio or video

**Audio (MP3).** Upload your MP3 into the **`audio`** folder. Then change the file name in the audio block:

```
{% raw %}{% include essay/audio.html
  file="audio/my-clip.mp3"
  caption="Who is speaking, what they describe, and your citation."
%}{% endraw %}
```

**Video (YouTube).** Upload your video to YouTube first (unlisted is fine). Delete the audio block and use this one, pasting the link you copied from YouTube:

```
{% raw %}{% include essay/video.html
  url="https://www.youtube.com/watch?v=XXXXXXXXXXX"
  caption="Who is speaking, what they describe, and your citation."
%}{% endraw %}
```

## Step 7: Save

Press **Ctrl+S** (or **Cmd+S** on a Mac) to save each file. Then click the **Source Control** icon on the left, type a short message like "Add my essay", and click **Commit & Push**. Your essay will appear on the site in a few minutes.

## Troubleshooting

- **My essay isn't on the home page.** Make sure the file is named `index.md`, your folder is inside `essays`, and `draft: true` is not in your front matter.
- **A picture doesn't show.** Check that the file name matches exactly, including capital letters and the `.jpg` or `.png` ending.
- **The page looks broken.** Check that every line you changed at the top still has its quotation marks, and that you didn't delete the lines of dashes.
- Still stuck? Ask your instructor, and tell them which step you were on.

You can delete this page (`instructions.md`) at the end of the semester.
