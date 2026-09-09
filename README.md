# Fifi's Portfolio Website

A multi-page portfolio website built.

## Overview

The site has five pages — Home, About, Courses, Projects and Contact —
sharing one navigation menu and footer. It introduces Tshifhiwa Makherana's ,
lists, skills and completed courses/certificates, showcases three
projects, and offers a contact form. (Courses is an extra page beyond
the four required by the brief; About, Projects and Contact all still
meet their individual requirements on their own.)

## Issues Found

The starter project contained missing navigation, weak semantic
structure, missing image alt text, an incomplete skills table, an
incomplete project section, an underdeveloped contact form, missing form
labels and validation, missing navigation styling, limited CSS
selectors, poor responsive behaviour, weak box-model demonstration and
inconsistent code organisation. The original stylesheet path was also
incorrect. The issues identified during the debugging process are
documented in `design/issues identified.txt`.

## Fixes implemented

- Rebuilt every page around semantic HTML5: `header`, `nav`, `main`,
  `section`, `article`, `footer`.
- Added one shared, accessible navigation menu (with `aria-current`
  for the active page) to all five pages.
- Wrote descriptive `alt` text for every image (13 across the site).
- Built the missing skills `<table>` on the About page (`thead`,
  `tbody`, `th`, `td`).
- Rebuilt the contact form with seven input types (text, email, tel,
  select, textarea, radio, checkbox), a `<label>` on every field, and
  `required`/`minlength`/`pattern` validation.
- Fixed the broken stylesheet path and expanded CSS selector variety
  (element, class, ID, descendant, attribute, pseudo-class).
- Fixed colour contrast so all text meets WCAG AA (verified — every
  text/background pair is 6:1 or higher).
- Styled the navigation, table and form, added hover/focus states, and
  demonstrated the box model consistently throughout.
- Added a mobile breakpoint (`@media (max-width: 700px)`) that stacks
  the layout on narrow screens.
- Kept non-semantic `<div>` use to a minimum: footer wrappers now use
  `<section>` and `<hr>` instead of stacked `<div>`s, so no page uses
  more than 2.

## HTML Structure

The main pages are `index.html`, `about.html`, `projects.html` and
`contact.html`. An additional `courses.html` page is also included. The
pages use `header`, `nav`, `main`, `section`, `article`, `figure` and
`footer` elements where appropriate. The About page contains the
required skills table, while the Contact page contains the accessible
form.

## CSS Styling

The stylesheet in `css/styles.css` uses a shared colour palette,
consistent typography, Flexbox layouts, spacing, borders, hover/focus
states, card styling, table styling and responsive media queries. CSS
comments divide the stylesheet into logical sections and explain
important accessibility and selector choices.

## Accessibility improvements

Skip-to-content link, semantic landmarks, a labelled and validated
form, descriptive alt text throughout, visible `:focus` states on
every interactive element (distinct from `:hover`), and text/background
contrast checked to stay at or above 4.5:1.

No build step is required.

## How to View

1.  Download or clone the repository.
2.  Open the project folder.
3.  Open `index.html` in a browser, or serve the folder with a local web
    server.
4.  Use the navigation menu to move between pages.

## Screenshots

See the `screenshots/` folder for the full set. Highlights:

- Homepage — `screenshots/Desktop view 1.png`
- Courses page — `screenshots/Desktop view 4.png`
- Styled table (About page) — `screenshots/Desktop view 3.png`
- Certificates cards — `screenshots/Desktop view 5.png`
- Projects grid — `screenshots/Desktop view 6.png`
- Contact form —  `screenshots/Desktop view 7.png` , `screenshots/Desktop view 8.png` & `screenshots/Desktop view 9.png`
- Mobile views — `screenshots/Mobile View 1.png`, `Mobile view 2.png`
- Before/after — `screenshots/Original home page.png` vs.
  `screenshots/Desktop view 1.png`

## Reflection

The trickiest part wasn't any single bug but the accumulation of
small ones hiding the bigger structural problems — the missing
`<meta viewport>` tag, for instance, meant the responsive layout looked
broken even after the media query was written correctly, until the tag
itself was added. Rebuilding the contact form's accessibility (labels,
validation, grouped radios in a nested `fieldset`) took the most
iteration, since it's easy to satisfy the letter of "add labels"
without actually making the field order and grouping easy to follow
with a keyboard or screen reader. Auditing colour contrast
mathematically rather than by eye also caught a couple of pairings
that looked fine but weren't.

