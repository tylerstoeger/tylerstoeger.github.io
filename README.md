# Tyler Stoeger personal website

Personal academic website and economics job market site for Tyler Stoeger.

Live site: [https://tylerstoeger.com](https://tylerstoeger.com)

The site is a static HTML/CSS website hosted with GitHub Pages from the
`tylerstoeger.github.io` repository and served through the custom domain
`tylerstoeger.com`.

## Site structure

```text
.
├── index.html
├── styles.css
├── CNAME
├── robots.txt
├── sitemap.xml
│
├── teaching/
│   └── index.html
│
└── assets/
    ├── docs/
    │   ├── Tyler_Stoeger_CV.pdf
    │   ├── Tyler_Stoeger_JMP.pdf
    │   ├── Tyler_Stoeger_Resume.pdf
    │   └── teaching/
    │       ├── ECON300_Syllabus.pdf
    │       └── ECON300_Sample_Lecture_Regression_Discontinuity.pdf
    │
    └── images/
        ├── headshot_cropped2.JPEG
        ├── favicon.png
        └── og-image.png
```

## Main files

- `index.html` — homepage, research, job market paper, contact information, and links to job market materials
- `styles.css` — site-wide visual styling
- `teaching/index.html` — teaching experience and sample teaching materials
- `CNAME` — configures GitHub Pages to use `tylerstoeger.com`
- `robots.txt` — provides crawler instructions and points search engines to the sitemap
- `sitemap.xml` — lists the site's indexable HTML pages

## Documents

The site links directly to the following files:

- `assets/docs/Tyler_Stoeger_CV.pdf`
- `assets/docs/Tyler_Stoeger_JMP.pdf`
- `assets/docs/Tyler_Stoeger_Resume.pdf`
- `assets/docs/teaching/ECON300_Syllabus.pdf`
- `assets/docs/teaching/ECON300_Sample_Lecture_Regression_Discontinuity.pdf`

Keeping these filenames unchanged allows updated versions of the documents to
be uploaded without changing links in the HTML.

## Images

The site currently uses:

- `assets/images/headshot_cropped2.JPEG` — homepage headshot
- `assets/images/favicon.png` — browser/site icon
- `assets/images/og-image.png` — 1200 × 630 social-sharing image used by Open Graph and Twitter/X metadata

## URLs

The main public URLs are:

- `https://tylerstoeger.com/`
- `https://tylerstoeger.com/teaching/`
- `https://tylerstoeger.com/robots.txt`
- `https://tylerstoeger.com/sitemap.xml`

The teaching page uses the GitHub Pages directory convention
`teaching/index.html`, allowing it to be served at `/teaching/` rather than
`/teaching.html`.

## Updating the site

For most routine updates:

1. Edit `index.html` for homepage or research content.
2. Edit `teaching/index.html` for teaching content.
3. Edit `styles.css` for site-wide design changes.
4. Replace PDFs in `assets/docs/` while preserving their filenames.
5. Commit changes to the `main` branch.

GitHub Pages will automatically rebuild and publish the site after changes are
committed.

If a new HTML page is added, also add its canonical URL to `sitemap.xml`.

## GitHub Pages settings

In the `tylerstoeger.github.io` repository:

1. Go to **Settings → Pages**.
2. Set the source to **Deploy from a branch**.
3. Select the `main` branch and `/ (root)` folder.
4. Set the custom domain to `tylerstoeger.com`.
5. Enable **Enforce HTTPS**.

## Cloudflare DNS

The apex domain uses GitHub Pages' A records:

| Type | Name | Content |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

The `www` subdomain uses:

| Type | Name | Content |
| --- | --- | --- |
| CNAME | www | tylerstoeger.github.io |

If GitHub Pages reports certificate or HTTPS problems, the relevant Cloudflare
records should be set to **DNS only** rather than proxied.

## Search engine optimization

The homepage includes:

- canonical URL metadata
- Open Graph metadata
- Twitter/X card metadata
- `ProfilePage` and `Person` JSON-LD structured data
- descriptive page titles and meta descriptions

The repository also contains:

- `robots.txt`
- `sitemap.xml`

The domain is registered with Google Search Console, where the sitemap can be
submitted and important pages can be inspected or re-indexed after major
updates.
