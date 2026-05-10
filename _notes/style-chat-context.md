# somlk.org — Style & Formatting Work
## Context for new chat

### Project
Migrating somlk.org (Southern Oregon MLK Day Celebration) from Weebly to Jekyll/Minimal Mistakes on GitHub Pages.

- **Repo:** https://github.com/gracion/somlk.org
- **Live preview:** https://gracion.github.io/somlk.org/
- **Local dev:** `bundle exec jekyll serve --baseurl ""` → http://localhost:4000/
- **macOS**, rbenv Ruby 3.3.6, `github-pages` gem, Minimal Mistakes remote theme, dark skin
- **Tools:** BBEdit + SourceTree + Terminal. Tab indentation in code files.

### What's done (as of end of migration chat)

- Jekyll + Minimal Mistakes dark skin working locally and on GitHub Pages
- `_config.yml` with `baseurl: "/somlk.org"` (change to `""` when custom domain is live)
- All pages migrated from Weebly to Markdown:
  - `index.md` (home) — 2026 event info, sponsors, video embeds, blood drive, book rec
  - `videos.md` — 2021/2022 video archive
  - `past-events/ashland.md` — 2015–2020 celebration archive with video embeds, PDF report links
  - `past-events/medford.md` — 2020 Medford event
  - `grants-pass.md` — Grants Pass celebration
  - `history.md` — historical Dr. King videos + "How did Coretta Cope?" essay
  - `about.md` — org info, past keynote speakers
  - `quote.md` — "A Proper Sense of Priorities" (Feb 6, 1968)
- `_data/navigation.yml` — full nav; Past Events is heading-only with Ashland/Medford as children
- Custom `_includes/masthead.html` — click-to-reveal dropdown for Past Events, dark theme styled (teal `#00adb5`, gray `#bbbbbb`, background `#252a34`)
- Hamburger menu shows Past Events children inline with indenting
- `_includes/video.html` — responsive YouTube/Vimeo embed include
- `assets/images/` — all images and PDFs downloaded from Weebly (11MB total), committed to Git (no LFS needed)
- All internal links use `{{ site.baseurl }}/...` prefix
- All asset references use `{{ site.baseurl }}/assets/images/...`
- Migration notes saved in `_notes/migration.md`

### Known issues / things not yet done

- **Formatting and style work** — this is the focus of the next chat:
  - Review each page for layout quality in the dark skin
  - Sponsors list on home page (currently a plain list — may want columns or logo treatment)
  - Video archive pages have year/theme/quote entries that could use better visual structure
  - Celebration report PDF links (plain list at bottom of Ashland page)
  - The `_includes/video.html` responsive embed CSS is in `_sass/custom.scss` — verify it's imported correctly in `assets/css/main.scss`
  - Image sizing/placement (some images float beside text on Weebly, currently just inline)
- **Custom domain** — when somlk.org DNS is pointed to GitHub Pages, set `baseurl: ""` in `_config.yml`

### Key file locations
- `_config.yml` — site config, baseurl, theme settings
- `_data/navigation.yml` — nav structure
- `_includes/masthead.html` — custom nav with dropdown
- `_includes/video.html` — video embed include
- `_sass/custom.scss` — custom CSS (responsive video, any new styles)
- `assets/css/main.scss` — imports custom.scss
- `assets/images/` — all migrated images and PDFs

### Video embed syntax
```liquid
{% include video.html id="YOUTUBE_ID" provider="youtube" %}
{% include video.html id="VIMEO_ID" provider="vimeo" %}
```

### Theme colors (dark skin)
- Teal accent: `#00adb5`
- Hover gray: `#bbbbbb`
- Background: `#252a34`