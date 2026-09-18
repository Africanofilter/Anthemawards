[README.md](https://github.com/user-attachments/files/32387334/README.md)
# Correct The Map

A scrolling story page built for Africa No Filter's (ANF) **Anthem Awards submission**, telling the story of the **#CorrectTheMap** campaign — from a 450-year-old cartographic distortion to a unanimous UN General Assembly vote backing the Equal Earth Projection.

**Live site:** _add your GitHub Pages URL here once it's live, e.g. `https://your-username.github.io/correct-the-map/`_

## What's in this repo

```
.
├── index.html          # the entire page (self-contained HTML/CSS/JS)
└── images/              # media clippings, campaign photos, and the AU emblem
    ├── mercator-vs-equalearth.png
    ├── un-podium-dussey.png
    ├── reuters-headline.png
    ├── ft-headline.png
    ├── ap-headline.png
    ├── globeandmail-headline.png
    ├── aljazeera-headline.png
    ├── bbc-headline.png
    └── au-emblem.png
```

No build step, no dependencies, no framework — just plain HTML, CSS, and a small vanilla JavaScript snippet that drives the scroll-pinned "Our Approach" section.

## Viewing it locally

Just open `index.html` in a browser. Because it references images via relative paths (`images/...`), keep the `images/` folder alongside it rather than moving the HTML file on its own.

## Publishing with GitHub Pages

1. Push this repo to GitHub (public repos get Pages for free).
2. Go to **Settings → Pages** in the repo.
3. Under **Source**, choose the branch this code lives on (usually `main`) and the root folder (`/`).
4. Save. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two.
5. Share that link with anyone — no GitHub or Claude account needed to view it.

If you'd rather use a custom domain (e.g. a subdomain of `correctthemap.org`), add a `CNAME` file with that domain to the repo root and configure the DNS records per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Editing the content

Everything — text, colors, layout — lives inline in `index.html`. There's no CMS or data file to edit separately:

- **Copy changes**: find the relevant `<p>`, `<h2>`, or `<h3>` tag and edit the text directly.
- **Images**: replace the file in `images/` (keep the same filename) or update the `src="images/..."` path if you rename it.
- **Colors**: the palette is applied via inline `style` attributes rather than CSS variables, so a global palette swap means a find-and-replace across the file. The main colors used are:
  - Navy `#0C1B3A` (dark section backgrounds)
  - Orange `#E0562A` (primary accent)
  - Teal `#0E7C61` (secondary accent)
  - Gold `#F4B93E` (tertiary accent)
- **The scroll-pin section** ("Our Approach"): the four phase panels are `<div id="phase-0">` through `<div id="phase-3">`, and the small `<script>` block near the bottom of the file handles fading between them based on scroll position.

## Image credits

- Mercator vs. Equal Earth projection overlay: Mike Bostock / Observable
- News headlines: Reuters, Financial Times, Associated Press, The Globe and Mail, Al Jazeera, BBC (used here as editorial screenshots documenting media coverage of the campaign)
- African Union emblem: African Union

## About the campaign

#CorrectTheMap is a campaign led by Africa No Filter and Speak Up Africa challenging the Mercator Projection's distortion of Africa's true size, and advocating for the adoption of the Equal Earth Projection. On 4 September 2026, 164 countries voted at the UN General Assembly to back a fairer world map.

Learn more at [correctthemap.org](https://correctthemap.org/).
