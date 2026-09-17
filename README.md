# Paws & Care Animal Shelter — Website

A multi-page website for a fictional Pretoria-based animal shelter, built for
WEDE5020 (POE). The site allows visitors to learn about the shelter, browse
adoptable animals, donate, and get in touch.

## Pages

| Page | File |
|---|---|
| Home | `index.html` |
| About Us | `about.html` |
| Adopt | `adopt.html` |
| Donate | `donate.html` |
| Contact | `contact.html` |

## Tech stack

- Semantic HTML5
- CSS3 — external stylesheet (`css/style.css`), CSS custom properties,
  Flexbox, CSS Grid, media queries
- Google Fonts (Quicksand, Lato)

## Project structure

```
ST10525380_Masoka_WEDE5020_POE_P1/
├── index.html
├── about.html
├── adopt.html
├── donate.html
├── contact.html
├── css/
│   └── style.css
├── js/
├── images/
└── README.md
```

> All page filenames are lowercase so that internal links resolve correctly
> on case-sensitive hosts such as GitHub Pages, not just on Windows.

## Responsive breakpoints

| Breakpoint | Width | Layout change |
|---|---|---|
| Desktop | > 768px | Multi-column grid (2–3 columns), full nav |
| Tablet | ≤ 768px | Grid drops to 2 columns, hero stacks, footer to 2 columns |
| Mobile | ≤ 480px | Single-column grid, stacked buttons and form fields |

## Screenshot evidence

> Add screenshots here showing the site at desktop, tablet and mobile widths
> (e.g. using browser DevTools' device toolbar, Ctrl/Cmd+Shift+M in Chrome
> or Edge). Include one set per page, or per key component (nav, hero,
> adopt grid, donate form), and paste the images directly into this section
> or link to an `/evidence` folder.

- Desktop (≥1200px):
- Tablet (768px):
- Mobile (375–480px):

## Changelog

### Part 2 — CSS styling, responsive design, and HTML fixes

**CSS styling**

- Created external stylesheet `css/style.css` and linked it from all five
  HTML pages.
- Added a CSS reset (box-sizing, margin/padding, list-style, image scaling)
  for consistent rendering across browsers.
- Defined a design-token layer using CSS custom properties (`:root`) for
  colour palette, typography scale, spacing scale and shared shadows/radius,
  so the cascade can be relied on with a minimum number of selectors.
- Applied base typography: Quicksand for headings, Lato for body text, a
  relative (rem-based) type scale, and consistent `line-height`/
  `letter-spacing`.
- Built the desktop layout using CSS Grid for page sections (`.grid`,
  `.grid-2`, `.grid-3`, `.footer-grid`, `.contact-grid`) and Flexbox for
  one-dimensional groups (`.nav`, `.hero-actions`, `.donate-options`).
- Styled visual components: navigation, buttons, hero, cards, timeline,
  forms, donate toggle/amount buttons, tags, and footer, using `color`,
  `background-color`, `border`, `border-radius` and `box-shadow`.
- Added interactive states with `:hover`, `:focus-visible` and `:active`
  pseudo-classes on links, buttons, donation-amount buttons and form fields.

**Responsive design**

- Breakpoints at `768px` (tablet) and `480px` (mobile) using media queries.
- Relative units (`rem`, `%`, `fr`) throughout instead of fixed pixel
  values for type, spacing and grid tracks.
- Grids collapse from 3 → 2 → 1 columns as the viewport narrows; the hero
  and contact layouts stack on smaller screens; the nav switches to a
  stacked, wrapping layout on tablet.
- Type scale (`--fs-2xl`, `--fs-xl`) and spacing scale (`--space-xl`,
  `--space-lg`) shrink at each breakpoint.
- Images set to `max-width: 100%` / `height: auto` so they scale within
  their containers at every breakpoint.
- Tested layout using browser DevTools' responsive/device toolbar across
  desktop, tablet and mobile widths.

**HTML structural fixes**

The previous export of this project had broken markup on every page
(missing header/nav opening tags, an empty logo link, unclosed anchor
tags around the "Enquire to adopt" buttons, a missing image on the Coco
card, and missing closing tags for the footer/body/html at the end of
every file). `index.html` in particular was cut off partway through the
homepage. These were corrected on all five pages:

- Rebuilt `index.html` in full (hero, impact stats, featured animals,
  testimonial, call-to-action, footer) — it previously ended mid-page.
- Restored the site logo/brand text ("Paws & Care") in the header and
  footer on every page.
- Closed the `<a>` tags around each "Enquire to adopt" button on
  `adopt.html` and added the missing photo for the Coco listing.
- Closed the remaining `</div>`, `</footer>`, `</body>` and `</html>`
  tags that were missing from the end of every page.
- Renamed all HTML files to lowercase and matched every internal `href`
  to the real filename, since three of the five files were previously
  capitalised (`Index.html`, `About.html`, `Donate.html`) while every
  link pointed to the lowercase version — this works on Windows but
  breaks navigation on case-sensitive hosts like GitHub Pages.
- Replaced two footer links that pointed at a `get-involved.html` page
  that doesn't exist in this project with links to `donate.html` and
  `contact.html`.

### Part 1 — Feedback edits

> _List the specific corrections made in response to your lecturer's Part 1
> feedback here, with enough detail for them to see exactly what changed
> (e.g. "Added missing `alt` text to adoption images", "Fixed heading
> hierarchy on the About page"). Copy the feedback comments/rubric items
> you received and note how each was addressed._

-
-
-

## References

- Mozilla Developer Network (MDN). n.d. *CSS: Cascading Style Sheets*.
  Available at: https://developer.mozilla.org/en-US/docs/Web/CSS
  [Accessed: 16 September 2026].
- Mozilla Developer Network (MDN). n.d. *CSS Grid Layout*.
  Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout
  [Accessed: 16 September 2026].
- Mozilla Developer Network (MDN). n.d. *CSS Flexible Box Layout*.
  Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout
  [Accessed: 16 September 2026].
- Mozilla Developer Network (MDN). n.d. *Using media queries*.
  Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries
  [Accessed: 16 September 2026].
- Google Fonts. n.d. *Quicksand* and *Lato*. Available at:
  https://fonts.google.com [Accessed: 16 September 2026].
- Unsplash. n.d. Stock photography used for animal images on the Home
  and Adopt pages. Available at: https://unsplash.com
  [Accessed: 16 September 2026].
