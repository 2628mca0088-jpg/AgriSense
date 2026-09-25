# AgriSense (Pure HTML + CSS Version)

This is a **100% HTML + CSS** version of the AgriSense project.
No React, no Tailwind, no JavaScript, no build tools, no npm install —
just open a file in your browser.

## How to run it
1. Open the `AgriSense-Simple` folder.
2. Double-click `index.html` to open it in your browser.
3. Click the nav links to move between pages (Home, Crop Explorer, Market Finder).

That's it — no server, no installation needed.

## Folder Structure

```
AgriSense-Simple/
│
├── index.html            -> Home page
├── crops.html             -> Crop Explorer page (shows all 12 crops)
├── markets.html            -> Market Finder page (shows all 12 markets)
│
├── css/
│   └── style.css           -> ALL the styling for every page (one file)
│
└── images/
    ├── banner-home.jpg      -> Banner picture on the Home page hero
    ├── banner-crops.jpg      -> Banner picture on the Crop Explorer header
    └── banner-markets.jpg     -> Banner picture on the Market Finder header
```

## Important: no JavaScript
You asked for a pure HTML + CSS project, so this version has **no `.js` files
at all**. That means a couple of things behave differently from the original:

- **Mobile hamburger menu** — still works! It's done with a pure CSS trick
  (a hidden checkbox + a `<label>`), no JavaScript needed. Shrink your
  browser window and try clicking the ☰ icon.
- **Search box / filter dropdowns** on the Crop Explorer and Market Finder
  pages are shown for the look of the design, but they don't actually
  filter the list — doing that needs JavaScript, which this version
  intentionally does not use. All 12 crops and all 12 markets are simply
  listed directly in the HTML.

## How to edit things

- **Change colors** → open `css/style.css`, edit the values at the very top
  under `:root { ... }` (for example `--color-primary`).
- **Add a new crop or market card** → open `crops.html` or `markets.html`,
  find a `<div class="crop-card">...</div>` (or `.market-card`) block,
  copy it, paste it, and change the text inside.
- **Change any text on a page** → open that page's `.html` file and edit
  the text directly, it's plain HTML.
- **Change/replace a banner image** → put your own picture in the `images`
  folder and update the matching `<img src="...">` tag (home page) or the
  `background-image` line in `style.css` (Crop Explorer / Market Finder
  page headers).
- **Change layout spacing/size** → everything uses simple Flexbox
  (`display: flex`), so look for `.some-class { display: flex; ... }` in
  `style.css`. No CSS Grid is used anywhere, to keep things simple.

## Notes
- Class and ID names are written in plain English (e.g. `.crop-card`,
  `.navbar-toggle`, `.page-header`) so it's easy to tell what each one does.
- Only basic, beginner-friendly CSS properties are used: `display: flex`,
  `padding`, `margin`, `border`, `border-radius`, `background-color`,
  `color`, `font-size`, `font-weight`.
