---
# ============================================================
#  STEP 1 - FILL IN THE INFORMATION BETWEEN THE DASHED LINES
#  Only change the text AFTER the colon on each line.
#  Keep the quotation marks. Lines starting with # are notes.
# ============================================================
layout: essay

# Title of your project
title: "Allie's Test Essay"

# Your name and course (shown under the title)
student: "Allie Love"
course: "US Immigration History, Fall 2026"

# Small label on the home page card, e.g. "Village to City"
kicker: "Place to Place"

# One sentence that appears on the home page card and under the title
summary: "One sentence that tells readers what your family's migration story is about."

# Main image: a photograph or object that introduces your family.
# Upload your image into the "images" folder next to this file, then type its file name below.
lead-image: images/test-image.jpg
lead-image-alt: "Short description of the image for screen readers"
lead-image-caption: "What the image shows, who is in it, and the source. Example: Maria and Jose Lopez outside their first apartment, Chicago, 1968. Courtesy of the Lopez family."

# To hide an unfinished essay from the home page, remove the # in front of the next line
# draft: true
---

{% comment %}
  ============================================================
  HOW TO USE THIS TEMPLATE
  ============================================================
  1. Copy this whole "template" folder and rename the copy with your
     name, e.g.  essays/maria-lopez
  2. In YOUR copy, fill in the information at the top of this file.
  3. Replace each paragraph below with your own writing.
     Keep the ## marks, but change the words after them to your own subheader.
  4. To add a picture, audio clip, or video, upload the file into your folder
     (images go in "images", audio goes in "audio") and change the file name
     inside the quotation marks in the matching block below.
  Text in a block like this one is a note. Readers can't see it.
  ============================================================
{% endcomment %}

Introduction (100-120 words). Introduce your family to the reader. Who are they, where did they come from, and where did they go? Name the people, the places, and the years. Use clear, welcoming language that a high school student could follow.

## Subheader 1: Historical context and impacts (4-8 words)

Paragraph 2 (150-250 words). Explain how your family's story connects to the larger history of migration. Draw on secondary sources from class, such as books and articles. What economic, political, or social forces pushed your family to leave and pulled them toward their destination? Cite your sources in Chicago style.

## Subheader 2: Personal context (4-8 words)

{% comment %}
  AUDIO: replace the file name below with your MP3, uploaded to the "audio" folder.
  VIDEO: to use YouTube instead, delete the audio block and paste this in its place:

  {% include essay/video.html
    url="https://www.youtube.com/watch?v=XXXXXXXXXXX"
    caption="10-25 words: who is speaking, what they describe, and a citation."
  %}
{% endcomment %}

{% include essay/audio.html
  file="audio/sample-clip.wav"
  caption="10-25 words: who is speaking, what they describe, and a citation. Interview by Your Name, City, Month Day, Year."
%}

Use a sentence or two here to introduce the clip and say why you chose it.

## Subheader 3: Describing the oral history as a whole

Paragraph 3 (300-350 words). Describe the journey as a whole: the family, one important object, and questions of identity and place. Where did your family end up, and how did they make it home? Which object carries the story, and what does it mean to them? Draw on your oral history and cite it.

{% include essay/figure.html
  image="images/placeholder.svg"
  alt="Short description of the image for screen readers"
  caption="20-30 words: what the image shows, why it matters to the story, and its source."
%}

## Subheader 4: Connections to other migration stories

Paragraph 4 (125-175 words). How does your family's story compare with the migration stories we studied in class? Name specific similarities and differences, and cite the class materials you are drawing on.

{% include essay/figure.html
  image="images/placeholder.svg"
  alt="Short description of the image for screen readers"
  caption="20-30 words: what the image shows, why it matters to the story, and its source."
%}

## Concluding subheader of your choice

Final paragraph (70-85 words). Reflect on what you learned about your family, about migration, and about U.S. history by doing this project.

{% comment %}
  OPTIONAL highlighted quotation from the oral history. Paste this where you want it:

  {% include typography/pullquote.html text="\"A short, powerful line from your interview.\"" %}
{% endcomment %}

## References

### Primary sources

Last name, First name. Oral history interview. Interviewed by Your Name. City, Month Day, Year.

### Secondary sources

List the articles, books, and class readings you cited, in Chicago style.
