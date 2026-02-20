# Content Model — Petra Portfolio (Next.js + Payload)

Date: 2026-02-20
Source: `notes/project-notes`

## Locale strategy (required)
- **MVP languages:** `sk`, `en`
- **Rule:** every publishable page must have SK+EN core text populated.
- **Future:** `de` can be added later without schema rewrite.

## IA (MVP)
- Home
- Bio
- Performances
- Media
- Pedagogy & Projects
- Contact

---

## Payload Globals

### `siteSettings`
- `siteTitle` (text, **required**)
- `defaultLocale` (select sk/en, **required**)
- `primaryEmail` (email, **required**)
- `socialLinks[]` (label/url, optional)
- `seoDefaults` (group, optional)

### `homepage`
- `heroTitle` (localized text sk/en, **required**)
- `heroSubtitle` (localized textarea sk/en, **required**)
- `heroImage` (media, optional)
- `featuredPerformance` (relation -> performances, optional)
- `featuredMedia` (relation -> mediaItems, optional)
- `ctaLabel` (localized text sk/en, **required**)
- `ctaUrl` (url, **required**)

### `contactPage`
- `intro` (localized richText sk/en, **required**)
- `bookingEmail` (email, **required**)
- `managementName` (text, optional)
- `managementEmail` (email, optional)
- `formEnabled` (checkbox, optional)

---

## Payload Collections

### 1) `biographies`
- `locale` (select sk/en, **required**)
- `shortBio` (textarea, **required**)
- `fullBio` (richText, **required**)
- `cvFile` (document, optional)
- `isPrimary` (checkbox, optional)

### 2) `performances`
- `title` (localized text sk/en, **required**)
- `startDate` (dateTime, **required**)
- `endDate` (dateTime, optional)
- `venue` (text, **required**)
- `city` (text, **required**)
- `country` (text, optional)
- `program` (localized richText sk/en, optional)
- `collaborators[]` (text, optional)
- `ticketUrl` (url, optional)
- `status` (draft/confirmed/cancelled, **required**, default draft)
- `featureOnHome` (checkbox, optional)

### 3) `mediaItems`
- `title` (localized text sk/en, **required**)
- `type` (youtube/spotify/imageGallery/document/link, **required**)
- `externalUrl` (url, **required** for youtube/spotify/link)
- `coverImage` (image, optional)
- `galleryImages[]` (image, **required** for imageGallery)
- `description` (localized richText sk/en, optional)
- `publishedAt` (date, optional)
- `featureOnHome` (checkbox, optional)

### 4) `projects`
- `title` (localized text sk/en, **required**)
- `category` (artistic/pedagogy/vsmu/podcast/other, **required**)
- `summary` (localized textarea sk/en, **required**)
- `body` (localized richText sk/en, optional)
- `links[]` (label/url, optional)
- `relatedInstitution` (relation -> institutions, optional)
- `startDate`/`endDate` (date, optional)

### 5) `institutions`
- `name` (text, **required**)
- `role` (localized text sk/en, optional)
- `url` (url, optional)
- `logo` (image, optional)
- `sortOrder` (number, optional)

---

## Derived listing rules
- **Upcoming performances:** `startDate >= now` and `status=confirmed`, sort ASC.
- **Archive performances:** `startDate < now` and `status!=cancelled`, sort DESC.

## Notes
- Embed-first media policy for MVP (YouTube/Spotify links over large uploads).
- SK/EN are mandatory publishing languages for launch.
