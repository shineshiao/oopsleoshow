# oopsleoshow.shineshiao.com

The website of **Oops, Leo!** (`@oopsleoshow`), a daily English-lesson channel by
[Shineshiao](https://shineshiao.com). It's the channel's home page and its link-in-bio
page, plus the three policy pages that the Meta and Google apps of the publishing tool
link to. Plain HTML and CSS, no build step, served by GitHub Pages from `main`.

| Page | Path |
| --- | --- |
| Home and link-in-bio | `/` |
| Privacy Policy | `/privacy/` |
| Terms of Service | `/terms/` |
| Data Deletion Instructions | `/data-deletion/` |

The policy texts come from `ai-english-channel/04-system/publish-app-pages.md` in the
`youtubeSelfRunning` repository: change them there and here together. Meta and Google
link to these exact paths, so don't move them.

## Domain

The custom domain is set in the repository's **Settings → Pages**, which adds a `CNAME`
file holding `oopsleoshow.shineshiao.com`. DNS is on Cloudflare: a `CNAME` record
`oopsleoshow` → `shineshiao.github.io`, **DNS only (grey cloud)**, so GitHub can issue
the HTTPS certificate. The old address https://shineshiao.github.io/oopsleoshow/ redirects
here by itself. Paths are relative, so the pages also work at that old address.

## Adding a lesson

Each lesson is one `<li class="lesson">` in `index.html`, newest first, with its cover in
`assets/lessons/` (the video's `day-NN-topic-cover.jpg`, resized to 432×768 WebP).
`data-at` is the 7 pm slot in Melbourne time; until then the card shows "Coming".

## Preview

```bash
python3 -m http.server 8000      # http://localhost:8000
```
