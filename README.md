# Tyler Stoeger personal website

Static website for GitHub Pages at `tylerstoeger.github.io`, configured for the custom domain `tylerstoeger.com`.

## Files

- `index.html`: main website content
- `styles.css`: visual styling
- `CNAME`: tells GitHub Pages to use `tylerstoeger.com`
- `assets/docs/`: put CV and job market paper PDFs here
- `assets/img/`: put a future headshot here

## Required PDF filenames

To avoid editing links, save your PDFs as:

- `assets/docs/Tyler_Stoeger_CV.pdf`
- `assets/docs/Tyler_Stoeger_JMP.pdf`

## Adding a headshot later

1. Save your photo as `assets/img/headshot.jpg`.
2. In `index.html`, replace:

```html
<div class="headshot-placeholder" aria-hidden="true">TS</div>
```

with:

```html
<img class="headshot" src="assets/img/headshot.jpg" alt="Tyler Stoeger">
```

## GitHub Pages settings

In the repository `tylerstoeger.github.io`:

1. Go to Settings > Pages.
2. Source: Deploy from a branch.
3. Branch: `main`; folder: `/root`.
4. Custom domain: `tylerstoeger.com`.
5. Enable HTTPS after DNS checks pass.

## Cloudflare DNS records

Add these DNS records for the apex domain:

| Type | Name | Content |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Add this DNS record for `www`:

| Type | Name | Content |
| --- | --- | --- |
| CNAME | www | tylerstoeger.github.io |

Use DNS only / unproxied if GitHub reports certificate or HTTPS problems.
