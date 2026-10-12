# backstageessentials.com

Static site for Backstage Essentials LLC. Hosted on Cloudflare Pages, which
deploys automatically on every commit to `main`.

## Structure

Five pages. Every page is an `index.html` inside its own folder, except the
homepage, which sits at the root.

| Page | File | Sheet |
|---|---|---|
| Home / index | `index.html` | 1 |
| Teaching | `teaching/index.html` | 2 |
| Backstage Essentials | `book/index.html` | 3 |
| Lighting design | `lighting/index.html` | 4 |
| Curriculum vitae | `cv/index.html` | 5 |

**All five files are named `index.html`.** Uploading one to the wrong folder
replaces a different page. Check the path, not the filename.

## Everything else lives at the root

- `favicon.ico`, `favicon-16.png`, `favicon-32.png`, `favicon-512.png`,
  `apple-touch-icon.png` — must stay at the root; the pages link to `/favicon.ico`
- `share-card.jpg` — 1200x630 link preview image for Open Graph and Twitter
- `plot-strega-detail.webp` — light plot detail on the homepage
- `book-cover-art.webp` — cover art
- Production photographs: `west-side-story`, `spider-woman`, `the-birds`,
  `legacy-of-light`, `img-1775`, `img-1783`, `elf-jr` (all `.webp`)
- `Larsen_CV_FINAL.pdf` — linked from the CV and teaching pages
- `robots.txt`, `sitemap.xml` — sitemap lists all five pages
- `_redirects` — legacy Squarespace URLs, read by Cloudflare Pages

## Deploying

Commit to `main`. Cloudflare rebuilds on its own.

Uploading through the GitHub web interface sometimes drops folders when files
are dragged in. To add a page, open its folder in GitHub first, then
**Add file → Upload files** from inside it. The file lands in the right place
and the path cannot go wrong.

After a deploy that changes page content, purge the Cloudflare cache
(**Caching → Configuration → Purge Everything**) and check the result in a
private browser window.

## Design

Paper, drafting grid, blueline ink. Courier Prime carries the paperwork layer
(headings, schedules, title blocks, numbers). Public Sans carries reading text.
Caveat appears only on the homepage, for handwritten annotation.

Colors are declared once as custom properties at the top of each page's
`<style>` block: `--paper`, `--blue`, `--red`, `--graphite`, `--mat`.

The homepage is the marked-up working copy — drafting tape, a coffee ring, a
stamp, elements a fraction off square. The four interior sheets are clean. Keep
that split.

## Images

Keep production photographs under about 200 KB. Resize to 1600 px on the long
edge and save as WebP at quality 84.
