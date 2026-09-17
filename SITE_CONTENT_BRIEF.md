# SITE_CONTENT_BRIEF.md

> **For the coding agent:** this file is the single source of truth for the content of this
> website. Everything below is real, supplied by the site owner. Do not invent facts, dates,
> metrics, institutions or links. Anything marked `TODO(shayo)` is deliberately blank — leave
> the literal `TODO(shayo)` marker in the file you write so it can be found later with a search.
> Delete this file from the repo before the final deploy (or add it to `exclude:` in `_config.yml`).

---

## 0. Identity

| Field           | Value                                                                                                                                  |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Full name       | Emmanuel Ayomide Balogun                                                                                                               |
| Goes by         | Shayo                                                                                                                                  |
| Site title      | Shayo Balogun                                                                                                                          |
| Role            | Product Manager, TekSphere Global Services Limited — Lagos, Nigeria                                                                    |
| Also            | NYSC corps member, Delta State                                                                                                         |
| Degree          | B.Tech Software Engineering, First Class Honours — Federal University of Technology, Akure (FUTA)                                      |
| GitHub          | `oluwashayo`                                                                                                                           |
| Site URL        | `https://oluwashayo.github.io`                                                                                                         |
| Research area   | Vision–language models; medical image analysis; AI for healthcare; retrieval-augmented generation; trustworthy generative AI           |
| Purpose of site | Application-facing academic portfolio for PhD / funded MSc applications, September–October 2027 intake (UK, Europe, Canada, Australia) |

---

## 1. `_config.yml`

Set exactly these; leave every other key at its default unless a later section says otherwise.

```yaml
title: Shayo Balogun
first_name: Emmanuel
middle_name: Ayomide
last_name: Balogun
contact_note: >
  Email is the fastest way to reach me — I answer within a day or two.
description: >
  Emmanuel Ayomide (Shayo) Balogun — product manager at TekSphere Global Services and
  vision–language model researcher working on AI for healthcare, medical image analysis
  and retrieval-augmented diagnosis systems.
keywords: vision-language models, medical image analysis, AI for healthcare, retrieval-augmented generation, LLaVA, Nigeria, FUTA
url: https://oluwashayo.github.io
baseurl: # MUST be empty for a user site. Delete the value /al-folio, keep the key.
icon: 🔬
last_updated: true
serve_og_meta: true
serve_schema_org: true
```

Jekyll Scholar author matching (this is what bolds his name in the publication list):

```yaml
scholar:
  last_name: [Balogun]
  first_name: [Emmanuel, E., Emmanuel Ayomide, E. A.]
```

---

## 2. `_data/socials.yml`

Keep only the lines below. **Delete** `inspirehep_id`, `custom_social`, and the commented WeChat/WhatsApp keys.

```yaml
cv_pdf: /assets/pdf/shayo_balogun_cv.pdf
email: TODO(shayo) # pick one: work address or a personal address you'll keep after TekSphere
github_username: oluwashayo
linkedin_username: TODO(shayo)
scholar_userid: TODO(shayo) # Google Scholar profile ID, or delete this line
orcid_id: TODO(shayo) # free to register at orcid.org — worth having before you apply
rss_icon: false
```

---

## 3. `_pages/about.md`

Front matter changes only:

```yaml
subtitle: >
  Product Manager at <a href="https://teksphereglobal.com">TekSphere Global Services</a>.
  Vision–language models and AI for healthcare. Lagos, Nigeria.
profile:
  align: right
  image: prof_pic.jpg
  image_circular: false
  more_info: >
    <p>Lagos, Nigeria</p>
    <p>B.Tech Software Engineering, FUTA</p>
```

Body copy — use this text as written (it is his, in his own framing):

> I build and study multimodal systems that reason over images and text, with a focus on
> healthcare. My final-year research at the Federal University of Technology, Akure (FUTA)
> fine-tuned a vision–language model and paired it with a retrieval-augmented generation
> pipeline so that a diagnosis could be grounded in retrievable clinical text rather than
> produced from model weights alone. That work became a skin disease diagnosis and information
> system, and two papers with my supervisor, Olukemi Victoria Olatunde.
>
> I am extending it in two directions: fusing multimodal clinical data rather than treating
> images and text as separate channels, and making generative diagnostic output trustworthy
> enough to be checked — grounded, attributable, and honest about uncertainty. I am looking for
> a PhD or fully funded MSc position starting in the September–October 2027 intake.
>
> Day to day I am a product manager at TekSphere Global Services in Lagos, where I work on
> production revenue systems for a state joint revenue board — taxpayer identification, an
> e-receipt payment management platform, and a fleet management platform — covering
> requirements, release documentation and user training. Before that I graduated from FUTA
> with First Class Honours in Software Engineering. I am currently serving my NYSC year in
> Delta State.

---

## 4. `_bibliography/papers.bib`

Delete every Einstein entry and the `@string{aps = ...}` line. Write exactly these two:

```bibtex
---
---

@inproceedings{olatunde2026integrated,
  abbr        = {ECAT'26},
  title       = {Integrated VLM-RAG-Powered Skin Disease Diagnosis and Information System},
  author      = {Olatunde, Olukemi Victoria and Balogun, Emmanuel Ayomide and Omoniyi, Victoria Ibiyemi},
  booktitle   = {1st International Conference on Emerging Computing Applications and Technologies (ECAT'26), School of Computing, Federal University of Technology Akure},
  year        = {2026},
  month       = jul,
  address     = {Akure, Nigeria},
  selected    = {true},
  bibtex_show = {true},
  note        = {Accepted for presentation, 15--16 July 2026. Selected papers to appear in the International Journal of Computing and Digital Innovation},
  abstract    = {TODO(shayo) paste the accepted abstract here},
  pdf         = {TODO(shayo) drop the paper in assets/pdf/ and put the filename here, or delete this line}
}

@inproceedings{olatunde2026development,
  abbr        = {ASBAMI'26},
  title       = {Development of a VLM-RAG-Powered Skin Disease Diagnosis and Information System},
  author      = {Olatunde, Olukemi Victoria and Balogun, Emmanuel Ayomide and Omoniyi, Victoria Ibiyemi},
  booktitle   = {5th African Symposium on Big Data, Analytics and Machine Intelligence (ASBAMI 2026), Federal University of Technology Akure},
  year        = {2026},
  address     = {Akure, Nigeria},
  selected    = {true},
  bibtex_show = {true},
  note        = {Under review},
  abstract    = {TODO(shayo) paste the submitted abstract here}
}
```

`_data/coauthors.yml` — delete all demo entries, then:

```yaml
"olatunde":
  - firstname: ["Olukemi Victoria", "Olukemi V.", "O. V.", "Olukemi"]
    url: TODO(shayo) # her FUTA staff page or Google Scholar profile, or delete the url line

"omoniyi":
  - firstname: ["Victoria Ibiyemi", "Victoria I.", "V. I."]
```

---

## 5. `_news/` — delete the three demo announcements, create these

Each file is `inline: true` with `layout: post`, `related_posts: false`. Newest last in this list.

1. `2026-XX-XX-futa-graduation.md` — `TODO(shayo) date` — "Graduated from FUTA with First Class Honours in Software Engineering."
2. `2026-XX-XX-ecat-accepted.md` — `TODO(shayo) acceptance date` — "Our paper _Integrated VLM-RAG-Powered Skin Disease Diagnosis and Information System_ was accepted for presentation at ECAT'26, School of Computing, FUTA."
3. `2026-XX-XX-asbami-submitted.md` — `TODO(shayo) date` — "Submitted _Development of a VLM-RAG-Powered Skin Disease Diagnosis and Information System_ to ASBAMI 2026. Under review."
4. `2026-XX-XX-nysc.md` — `TODO(shayo) date` — "Began NYSC service in Delta State."
5. `2026-07-15-ecat-presentation.md` — "Presented at ECAT'26 in Akure." — `TODO(shayo) keep only if you presented; otherwise delete.`

---

## 6. `_projects/` — delete all nine demo projects, create these

First set the categories in `_pages/projects.md`:

```yaml
display_categories: [research, systems, side projects]
```

Every project file: `layout: page`, a one-line `description`, `img: assets/img/projects/<name>.jpg`, an
`importance` number, and a `category` from the list above. Order below is the intended `importance`.

**1 — `1_vlm_rag_skin_diagnosis.md`** · category `research` · `related_publications: true`
Title: _VLM-RAG skin disease diagnosis and information system_
Content: fine-tuned a vision–language model for skin lesion images and paired it with a
retrieval-augmented generation layer so answers are grounded in retrievable dermatological text.
Basis of both 2026 papers. Cite them with `{% cite olatunde2026integrated %}` and
`{% cite olatunde2026development %}`.
`TODO(shayo)` — datasets used, base model checkpoint, evaluation metric and result, repo link.

**2 — `2_taxman.md`** · category `research`
Title: _Taxman — a multimodal agent for Nigerian tax filing_
Content: an n8n-orchestrated AI agent that accepts text, images, voice and PDF/CSV input, with a
RAG layer grounded in the Nigeria Tax Act 2025, so guidance can be traced back to statute.
`TODO(shayo)` — screenshot or architecture diagram, current status, whether the repo is public.

**3 — `3_revenue_systems.md`** · category `systems`
Title: _Revenue systems for a state joint revenue board_
Content: product management and release documentation for three production systems — taxpayer
identification, an e-receipt payment management platform (prepaid organisation wallets, payment
profile settlement, reversals, receipts and reports), and a fleet management platform (web portal
plus mobile app, two-level trip approval). Wrote the user manuals and ran executive training.
`TODO(shayo)` — confirm what you are permitted to publish about a government client, and swap
any screenshots for redacted ones or generic diagrams.

**4 — `4_fleet_management.md`** · category `systems`
Only if you want fleet separate from #3 rather than folded into it. Same permission caveat.
`TODO(shayo)` — keep or delete this file.

**5 — `5_abbis_farm.md`** · category `systems`
Title: _Abbis Farm — commerce and operations platform_
Content: a Next.js 15 App Router e-commerce, POS and operations platform for a Nigerian red palm
oil producer with a mill in Iwo, Osun State — Prisma/Postgres, Paystack payments, Cloudinary media,
Resend mail, JWT admin auth.
`TODO(shayo)` — live URL if it is public, and a screenshot of the storefront and POS.

**6 — `6_agent_evaluation_tasks.md`** · category `side projects`
Title: _Authoring evaluation tasks for coding agents_
Content: authored SWE-Bench-Pro-style tasks against Python repositories — hidden test patches,
fail-to-pass / pass-to-pass separation, and a grading harness — plus a precision-constrained ML
engineering task for an agent-evaluation platform.
`TODO(shayo)` — say which parts you can name publicly.

**7 — `7_bible_memory_tools.md`** · category `side projects`
Title: _Quiz and memory tools for teenagers_
Content: small web tools built for church youth ministry — Bible memory games and quizzes used
with teenagers, part of a broader interest in skills-focused programming for Nigerian secondary
school students.
`TODO(shayo)` — screenshot, and a link if any of them are hosted.

**8 — `8_webgl_network_scene.md`** · category `side projects`
Title: _WebGL network scene_
Content: an interactive Three.js network animation — the visual language behind the TekSphere
"living motherboard" site redesign.
`TODO(shayo)` — keep only if you can host or GIF it; a project page with no visual is weak.

---

## 7. CV page

Two possible sources, and **only one may exist**: `assets/json/resume.json` (JSON Resume /
RenderCV) or `_data/cv.yml`. Read `docs/CUSTOMIZE.md` § CV, pick one, delete the other, and make
`cv_format` in `_pages/cv.md` match. Also set `cv_pdf: /assets/pdf/shayo_balogun_cv.pdf`.

Sections and content, in this order:

- **Education** — B.Tech Software Engineering, First Class Honours, Federal University of
  Technology Akure. `TODO(shayo)` start and end years, CGPA if you want it shown, final-year
  research title (the VLM-RAG skin disease system).
- **Experience** — Product Manager, TekSphere Global Services Limited, Lagos (`TODO(shayo)` start
  date). Highlights: product management for a state joint revenue board's tax identification,
  e-receipt payment management and fleet management systems; authored the user manuals and
  API documentation; ran role-based executive training.
- **Service** — NYSC corps member, Delta State (`TODO(shayo)` dates).
- **Publications** — the two 2026 papers from section 4.
- **Research interests** — vision–language models, medical image analysis, multimodal clinical
  data fusion, retrieval-augmented generation, trustworthy generative AI.
- **Skills** — `TODO(shayo)` list them yourself so the list is honest; suggested groupings:
  ML/LLM (fine-tuning, RAG pipelines, PyTorch, Weights & Biases), engineering (Python,
  TypeScript/Next.js, Postgres/Prisma, n8n), product (requirements, release documentation,
  user training).
- **Awards** — `TODO(shayo)` First Class Honours plus anything else you want listed.

---

## 8. Theme and assets

- Theme colour: `#1f6f6b` (deep teal). In `v1.x` the theme tokens are gem-owned, so create a
  local `_sass/_themes.scss` override in this repo — see `docs/CUSTOMIZE.md` § Changing theme
  color. This override is legitimate in a personal site (it is only forbidden in the upstream
  al-folio repo).
- `assets/img/prof_pic.jpg` — replace with a real headshot. `TODO(shayo)` supply the photo.
- `assets/img/projects/` — one 3:2 image per project, ~1200×800.
- `assets/pdf/` — delete `example_pdf.pdf`, add `shayo_balogun_cv.pdf`.
- Favicon: `icon: 🔬` in `_config.yml`.

---

## 9. Demo content to delete before deploying

```
_pages/about_einstein.md
_pages/books.md          _books/
_pages/teaching.md       _teachings/
_pages/plugins.md
_pages/repositories.md   (or keep it and set _data/repositories.yml to oluwashayo's real repos)
_posts/                  (all demo posts — keep the blog only if you will actually write)
_data/venues.yml         (edit rather than delete if you keep publication venue colouring)
assets/pdf/example_pdf.pdf
```

If the blog goes, also set `blog_name` / `blog_description` or remove `_pages/blog.md` and its
nav entry. If it stays, `TODO(shayo)` write one real post — an empty blog reads worse than none.

---

## 10. Hard rules for the agent

1. `baseurl:` must be present and empty. Blanking the key entirely, or leaving `/al-folio`,
   is the single most common way this site deploys unstyled with broken links.
2. Do **not** create `_layouts/`, `_includes/`, `_scripts/`, `assets/tailwind/` or
   `tailwind.config.js`. Runtime lives in gems (`theme: al_folio_core`). The one sanctioned
   local override is `_sass/_themes.scss` / `_sass/_variables.scss` for colour.
3. `Gemfile` and `_config.yml` are two lists that must agree — a plugin in only one is inert.
   Do not add or remove plugins for this build.
4. Features fail silently: a feature renders only when its gem is loaded, its flag is on, and the
   page opts in. If something does not appear, check the flag before rewriting the page.
5. Never invent a date, metric, dataset, institution or URL. Leave `TODO(shayo)`.
6. Run `npx prettier --write .` before committing — CI checks formatting and will fail the build.
