# Content Model & Information Architecture

Date: 2026-02-20
Project: Petra Portfolio (Next.js + Payload)
Source: `notes/project-notes`

## Product goal (from notes)
Portfolio website for Petra Torkošová with:
- profile / biography (SK + EN, optional DE later)
- artistic activity
- current concert season plan
- videos + photo gallery
- links to VŠMU pedagogy/projects
- contact
- optional dissertation link + podcast links

---

## IA (site map)
- Home
- Bio
- Performances
- Media
- Pedagogy & Projects
- Contact

Utility pages:
- Privacy (if contact form enabled)
- 404

---

## Payload CMS model

## Globals

### `siteSettings` (global)
- `siteTitle` (text)
- `defaultLocale` (select: sk/en)
- `supportedLocales` (array)
- `primaryEmail` (email)
- `socialLinks` (array: label + url)
- `seoDefaults` (group: titleTemplate, description, ogImage)

### `homepage` (global)
- `heroTitle` (localized text)
- `heroSubtitle` (localized textarea)
- `heroImage` (upload/media)
- `featuredPerformance` (relationship -> performances, optional)
- `featuredMedia` (relationship -> mediaItems, optional)
- `ctaLabel` / `ctaUrl` (localized text + url)
- `sections` (blocks: shortBio, highlightCards, quote, logos)

### `contactPage` (global)
- `intro` (localized richText)
- `bookingEmail` (email)
- `managementContact` (group, optional)
- `formEnabled` (checkbox)

---

## Collections

### `biographies`
Purpose: structured multilingual profile.

Fields:
- `locale` (select: sk/en/de)
- `shortBio` (textarea, required)
- `fullBio` (richText, required)
- `cvFile` (upload/document, optional)
- `isPrimary` (checkbox)

### `performances`
Purpose: concerts, projects, appearances.

Fields:
- `title` (text, required)
- `startDate` (date+time, required)
- `endDate` (date+time, optional)
- `venue` (text, required)
- `city` (text, required)
- `country` (text, optional)
- `program` (richText, optional)
- `collaborators` (array of text)
- `ticketUrl` (url, optional)
- `status` (select: draft/confirmed/cancelled)
- `featureOnHome` (checkbox)

Derived views:
- Upcoming = startDate >= now && status=confirmed
- Archive = startDate < now && status!=cancelled

### `mediaItems`
Purpose: videos, audio, galleries, documents.

Fields:
- `title` (text, required)
- `type` (select: youtube/spotify/imageGallery/document/link)
- `externalUrl` (url, conditional required)
- `coverImage` (upload/image, optional)
- `galleryImages` (array uploads, for imageGallery)
- `description` (localized richText)
- `publishedAt` (date)
- `tags` (array text)
- `featureOnHome` (checkbox)

### `projects`
Purpose: artistic + educational projects.

Fields:
- `title` (text, required)
- `category` (select: artistic/pedagogy/vsmu/podcast/other)
- `summary` (localized textarea)
- `body` (localized richText)
- `relatedInstitution` (relationship -> institutions, optional)
- `links` (array: label + url)
- `startDate` / `endDate` (optional)
- `assets` (array media)

### `institutions`
Purpose: credibility and external references.

Fields:
- `name` (text, required)
- `role` (localized text)
- `url` (url)
- `logo` (upload/image, optional)
- `sortOrder` (number)

### `pressMentions` (optional MVP+1)
- `title`, `source`, `date`, `url`, `quote`

---

## Reusable Blocks (for page builder fields)
- Hero
- Rich text section
- Quote/testimonial
- Performance list (filtered)
- Media grid
- Institution logos
- CTA banner

---

## URL schema
- `/` home
- `/bio`
- `/performances`
- `/performances/[slug]`
- `/media`
- `/projects`
- `/projects/[slug]`
- `/contact`

---

## Editorial workflow (small-batch)
1. Add event/media in draft.
2. Preview in Next.js.
3. Publish single item.
4. Verify rendering + SEO meta.

Decision log:
- External embeds preferred over large file hosting in MVP.
- Bilingual SK/EN from day one; DE as optional expansion.
- Performance chronology is core domain behavior, so date fields are mandatory.
