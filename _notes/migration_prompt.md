I'm migrating somlk.org from Weebly to Jekyll/Minimal Mistakes (dark skin) on GitHub Pages.
The repo is at ~Documents/Web/MLK/somlk.org

Stub .md files already exist for all pages. Fill them in with the content below.
Use tabs for indentation in any code/config files (not Python).

---

## SETUP NOTES

- baseurl is "/somlk.org" during dev/staging
- layout: single for most pages; layout: home for index
- Video embeds use: {% include video.html id="VIDEO_ID" provider="youtube" %}
  and for Vimeo: {% include video.html id="VIDEO_ID" provider="vimeo" %}
  The _includes/video.html file doesn't exist yet — create it too (see below).
- For Internet Archive embeds, use a raw <iframe> since there's no include for those.
- External links should open in a new tab: [text](url){:target="_blank"}
- Images from the old Weebly site (somlk.org/uploads/...) should be referenced
  as-is for now (hotlinked) — we'll migrate assets separately.

---

## 1. Create _includes/video.html

This include should render a responsive embed for YouTube or Vimeo.
Usage: {% include video.html id="VIDEOID" provider="youtube" %}

It should output a <div class="responsive-video"> with the appropriate iframe.
YouTube URL: https://www.youtube.com/embed/{{ include.id }}
Vimeo URL: https://player.vimeo.com/video/{{ include.id }}

Add this CSS to _sass/custom.scss (create if it doesn't exist, and import it
from assets/css/main.scss):

.responsive-video {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
  overflow: hidden;
}
.responsive-video iframe {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  border: 0;
}

---

## 2. index.md (Home page)

---
title: "Martin Luther King, Jr. Day Celebrations"
layout: home
permalink: /
excerpt: "Southern Oregon celebrates Martin Luther King, Jr. Day each year with events in Ashland and Grants Pass."
header:
  overlay_color: "#000"
---

Content to include (in this order):

- Heading: "Monday, January 19, 2026"
- 2026 celebration video embed: YouTube ID = HSSdk_TI3cw
  Note: "Main program starts at 50:54"
- 2026 event details:
  - Theme: "The time is always right to do right. We are all tied together in a single
    Garment of Destiny caught in an inescapable network of Mutuality."
  - Keynote: Southern Oregon University President Rick Bailey
  - Performers: students from SOU, Ashland High School, Ashland Middle School,
    Helman and Walker elementary schools, Nina Davis, Rogue Valley Peace Choir
  - After celebration: march to downtown Plaza for "I Have a Dream" speech
  - When: Noon–1:30pm, doors open 11:30am
  - Where: Historic Ashland Armory, 208 Oak St., Ashland
  - Overflow: OSF's Carpenter Hall (live stream)
  - Admission: FREE; non-perishable food donations encouraged for SOU Food Pantry

- Sponsors section (use a simple list or two-column layout):
  Ashland Chamber of Commerce (ashlandchamber.com)
  Ashland Food Coop (ashlandfood.coop)
  Black Southern Oregon Alliance (blacksouthernoregonalliance.com)
  Jackson County Library System (jcls.org)
  Oregon Shakespeare Festival (osfashland.org)
  Peace House (peacehouse.net)
  Rogue Valley Community Resource Center (rvml.org)
  SOPride (sopride.org)
  Southern Oregon University (sou.edu)
  TC Chevy (tcchevy.com)
  Two Sisters Writing and Publishing (twosisterswriting.com)

  In partnership with:
  Ashland's Historic Armory (historicashlandarmory.com)
  B.A.S.E. (baseoregon.org)
  SOU Digital Media Center (dmc.sou.edu)
  City of Ashland (ashlandoregon.gov)

- Divider, then: link to Grants Pass MLK Jr Day Celebration (/grants-pass/)

- 2025 recording note: "The recording of Ashland MLK Day 2025 can be viewed at
  RVTV's YouTube channel." Link: https://www.youtube.com/live/hj9R_5LrZOk?si=r6Pc9jrM-VG6UBEK

- Section: "Local MLK Documentaries"
  - "Remembering Dr. Martin Luther King Jr." — YouTube: PaXTaWvrbw8
    Description: "Explore the meaning of MLK Day through the eyes of our own community,
    created by BASE Southern Oregon."
  - We Stand Together — YouTube: EsHaet4OLD4
  - Why We Can't Wait — YouTube: fr3JbFlaRGE
  - Where Do We Go From Here (Youth Leadership) — YouTube: CEnifgJkHVk
  Links: [More Video and Info](/videos/) | [BASE YouTube Channel](https://www.youtube.com/channel/UCW4qCfQO0I9Yn1mcGYXw5rg)

- "Dr. King's 1961 message for Oregonians" — link to oregonlive.com article:
  
https://www.oregonlive.com/history/2021/01/martin-luther-king-jr-challenged-oregonians-60-years-ago-to-find-a-way-to-live-together-or-perish-as-fools.html

- "Dr. King on Expediency vs. Right" - link to quote.md page below

- Book recommendation: "Read Dr. King's book Why We Can't Wait"
  Get it from your local bookstore or Jackson County Library Services
  (link: https://catalog.jcls.org/GroupedWork/614a3b8a-ddd8-68a7-1dfb-1f0024e24354-eng/Home)

- Blood Drive section:
  "The need for blood donors is urgent. Following in the tradition of our MLK Day
  blood drives, we urge you to sign up to donate blood."
  Link to Red Cross campaign: https://sleevesup.redcrossblood.org/campaign/southern-oregon-mlk-our-voices/
  Schedule link: https://www.redcross.org

---

## 3. videos.md

---
title: "Video Archive"
layout: single
permalink: /videos/
---

### 2022

Photo: https://www.somlk.org/uploads/9/5/8/8/95881824/movieposterthumbnail_orig.jpg
Alt: "Where Do We Go From Here film poster"

Description: A new film from BASE Southern Oregon premiered with a live chat discussion
in January 2022. In the film, the children of BASE's AfroScoutz program explore issues
identified by Dr. King in "Where Do We Go From Here," including education, economics,
civics, and policing. Together, the leaders of today and tomorrow discuss how we can
apply Dr. King's wisdom to current issues in the Rogue Valley and beyond.
Watch on: Facebook (https://www.facebook.com/SOMLKDay/) or YouTube (https://youtu.be/CEnifgJkHVk)

Book rec: "Where Do We Go From Here: Chaos or Community?" by Dr. King.
Get it from: local bookstore, Jackson County Library (https://catalog.jcls.org/Record/103556),
Apple Books (https://books.apple.com/us/book/where-do-we-go-from-here/id476023461),
Kindle (https://smile.amazon.com/dp/B009U9S6EO/),
Nook (https://www.barnesandnoble.com/w/where-do-we-go-from-here-martin-luther-king-jr/1112547782)
ISBN: 9780807000670

### 2021

Video 1 — YouTube ID: VbmlMarDaDk
Caption: "The documentary video that premiered January 18, 2021"

Video 2 — YouTube ID: 4FXDgbVIXlA
Caption: "The live panel discussion that followed the premiere"

Video 3 — Vimeo ID: 501990265
Caption: "In Memoriam of those we lost, nationally and locally, in 2020"

Link at bottom: [Watch Previous MLK Events](/past-events/ashland/)

---

## 4. _pages/past-events/ashland.md
(or wherever the stub lives — check the repo structure)

---
title: "Ashland MLK Celebration"
layout: single
permalink: /past-events/ashland/
---

Note at top: "For the 2021 and 2022 video events, see the [Videos page](/videos/)"

### 2020 Ashland MLK Celebration

Event image: https://www.somlk.org/uploads/9/5/8/8/95881824/editor/mlk-2020-front-v2-01.png
Alt: "In the Spirit of Freedom Summer — 2020 MLK celebration poster"

Vimeo embed: ID = 386358758
Caption: "Our entire program, starting with the pre-show performance by the Bishop
Mayfield band, and a history of Freedom Summer, before the main program, featuring
Keynote Speaker Nataki Garrett, OSF Artistic Director."
Note: "See more of Dr. King and our shared history on the [History page](/history/)"

Details:
The 32nd annual Ashland Martin Luther King Jr. Holiday Celebration was held on Monday,
January 20th at the Historic Ashland Armory. Overflow attendees watched a simulcast
live stream at the Varsity Theatre.

Featured: Brent Florendo, Walker Elementary School students, SOU BSU, Ashland High
School Jazz Band, Children for Change, Ashland Danceworks, The Bishop Mayfield Band,
MC: D.L. Richardson. Program includes a history of Freedom Summer, In Memoriam, and
"We Stand Together."

The celebration is FREE and open to the public. Non-Perishable Food Donations for
ACCESS are encouraged. After the celebration, marched to the Ashland Plaza for the
playing of Dr. King's "I Have a Dream" speech.

Blockquote linking to /quote/:
> "There comes a time when one must take a position that is neither safe, nor politic,
> nor popular, but he [or they] must take it because his [or their] conscience tells
> him [or them] it is right…"
> — Dr. Martin Luther King, Jr.
>
> [Read the full quotation in context →](/quote/)

Social links:
Facebook: https://www.facebook.com/Ashland-Martin-Luther-King-Jr-Holiday-Celebration-139540922765640/
Twitter/X: https://twitter.com/AshlandMLKDay
Instagram: https://www.instagram.com/ashlandmlkday/

### Ashland MLK Celebration Archive

For each year, show the video embed alongside the theme and quote.
Use a two-column-style layout if possible (e.g., a table or side-by-side div),
or just embed the video followed by the year/theme/quote as a blockquote.

2019 — Internet Archive embed (use raw iframe):
src="https://archive.org/embed/PA5739805"
Theme: "From Then to Now… Empowering the Dream"
Quote: "We have inherited a large house … a family unduly separated in ideas, culture
and interest, who because we can never again live apart, must learn somehow to live
with each other in peace."

2018 — YouTube ID: 1x-vQ3kmtpE (use youtube-nocookie.com in the iframe src)
Theme: "The fierce urgency of now: tomorrow is today."
Quote: "We are now faced with the fact that tomorrow is today. We are confronted with
the fierce urgency of now. In this unfolding conundrum of life and history, there is
such a thing as being too late...There is an invisible book of life that faithfully
records our vigilance or our neglect."

2017 — YouTube ID: m-5Sv-4FzD8
Theme: "Power. Justice. Love for All"
Quote: "Power without love is reckless and abusive, and love without power is sentimental
and anemic. Power at its best is love implementing the demands of justice, and justice
at its best is power correcting everything that stands against love."

2016 — YouTube ID: WBzEI3KdZcI
Theme: "Let Us Be Dissatisfied and Transform Dark Yesterday's Into Bright Tomorrow's."
Quote: "We have a task and let us go out with a 'divine dissatisfaction.' Let us be
dissatisfied until America will no longer have a high blood pressure of creeds and an
anemia of deeds..."

2015 — YouTube ID: mW5HxtNzs3M
Theme: "Share the Dream, Live the Reality"
Quote: "I believe that unarmed truth and unconditional love will have the final word in
reality. This is why right temporarily defeated is stronger than evil triumphant."

### Celebration Reports (PDF links, hosted on Weebly for now)

- [2008 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2008_mlk_report.pdf)
- [2009 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2009_mlk_report.pdf)
- [2010 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2010_mlk_report.pdf)
- [2011 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2011_ashland_martin_luther_king_celebration_report.pdf)
- [2012 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2012_mlk_report.pdf)
- [2013 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2013_mlk_report.pdf)
- [2014 Celebration Report](https://www.somlk.org/uploads/9/5/8/8/95881824/2014_report.pdf)

---

## 5. _pages/past-events/medford.md

---
title: "Medford MLK Celebration"
layout: single
permalink: /past-events/medford/
---

Note: "Previous Medford and Rogue Valley events. See also our [Videos page](/videos/)"

### 2020 Medford Celebration

Image: https://www.somlk.org/uploads/9/5/8/8/95881824/medford-mlk-collage.jpg
Alt: "Medford MLK celebration collage"

Event details:
Sunday, January 19, 2020, 2:00–3:30 PM
Medford School District Auditorium
815 South Oakdale Ave., Medford, OR
Free to the Public

"Celebrate the life and legacy of Dr. King through song, speeches and more. Commit to
the work still to be done."

"Finding Our Voice" — after the celebration, held in the cafeteria 3:30–5:00 PM.
Light refreshments provided.

Facebook: http://facebook.com/MedfordMLK

About the Task Force: "The MLK Day celebration is an annual project of the MLK Task
Force. The Task Force is comprised of members of the Multicultural Commission,
Multicultural Association of Southern Oregon, Medford School District, and other
community volunteers. We work to honor Dr. King's memory and keep his dream alive
in our community."

---

## 6. grants-pass.md

---
title: "Grants Pass MLK Celebration"
layout: single
permalink: /grants-pass/
---

Heading: "Martin Luther King Jr. Day Events in Grants Pass"

### Grants Pass Celebration

Newman United Methodist Church (https://newmanumc.net) hosted an event on January 19, 2025
at 6:00 pm with keynote speaker Joseph Wallace-Williams. A reception followed.

Image: https://www.somlk.org/uploads/9/5/8/8/95881824/grants-pass-mlk-2026_orig.png
Alt: "Grants Pass MLK 2026 event flyer"

---

## 7. history.md

---
title: "Learn From History"
layout: single
permalink: /history/
---

Intro: "Take a moment to go back in time, experience history, and hear Dr. King in
his own words."

Table of contents (anchor links within the page):
- 1957: "Segregation and the South" documentary
- 1962: Dr. King on the Emancipation Proclamation
- 1965: Dr. King on "Meet the Press"
- 1967: "The Other America" speech
- 1956: How did Coretta Cope?

For each video section, show the year + title as a heading, followed by the embed:

1957 — YouTube ID: tfgQdCld3Fg
Title: "Segregation and the South," a documentary aired on ABC

1962 — YouTube ID: N0Jzqiqwo5A
Title: Speech on the Centennial of the Emancipation Proclamation

1965 — YouTube ID: fAtsAwGreyE
Title: Dr. King on "Meet the Press"
Context: "One month after Minister Malcolm X is assassinated, Dr. King was on Meet
the Press. This interview occurs in the midst of the 1965 march the movie Selma is
patterned after."

1967 — YouTube ID: dOWDtDUKz-U
Title: "The Other America" — Speech at Stanford University

### How did Coretta Cope?

by Kokayi Nosakhere

[Include the full text of this essay exactly as written — it is original creative
writing by a named author and must be preserved verbatim.]

The essay begins: "It is January 30, 1956. It is 9:15 pm..." and ends with the
two rhetorical questions about a White mother's sympathy and apology.

---

## 8. about.md

---
title: "About Southern Oregon MLK"
layout: single
permalink: /about/
---

### Connecting Community

"Southern Oregon's tradition of coming together on this day continues. Some of us have
participated with their screens at home or at the Varsity Theatre. Our online spaces
are where our friends across the county and our friends next door can share what's
important to them. Please like our Facebook pages, follow us on Twitter, and share your
pictures and observations of the many celebrations taking place in January. #SOMLK"

Image: https://www.somlk.org/uploads/9/5/8/8/95881824/14j-5446-2014-mlk-jr-ashland-armory_1.jpg
Alt: "MLK Jr. celebration at the Ashland Armory, 2014"

Past Ashland Keynote Speakers have included: Kayse Jama (executive director of the
Portland-based Center for Intercultural Organizing), D.L. Richardson (Civil Rights
Historian and Educator), Magdaleno Rose-Avila (Executive Director of the Social Justice
Fund in Seattle), La Clinica Development Director Maria Ramos Underwood, Professor
Rickerby Hinds, Flora Chavez (Crater Alumna and Actor), and Mary Farell of The Maslow
Project.

somlk.org was created by the Ashland MLK Day Committee. It is currently maintained by
Paul Collins. [Omit the email address — it was obfuscated by Weebly's CDN anyway.]

---

## 9. quote.md

---
title: "A Proper Sense of Priorities"
layout: single
permalink: /quote-priorities/
---

Subtitle/intro: "A selected quotation of Dr. Martin Luther King, Jr." — February 6, 1968"

Context paragraph (in italics):
"Dr. King made a speech to a group of clergy and laypeople in Washington DC who were
concerned about the Vietnam War. Near the end of the speech, he said this:"

Then the full quotation as a Markdown blockquote. The text begins with "Someone said
to me not long ago..." and ends with "...because conscience tells him it is right."
Preserve the [Applause] and [Laughter] notations exactly as they appear in the source.

---

## AFTER WRITING FILES

Please confirm:
1. All 9 files/includes are created
2. Run `bundle exec jekyll build` from the repo root and report any errors
3. List any Weebly image URLs that are hotlinked (so they can be downloaded later)