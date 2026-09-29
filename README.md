# Altitude — Guided Mountain Expeditions

A single-page, animated landing page for a guided mountain-expedition
company, built as one self-contained HTML file (no build step, no
dependencies to install).

## Features

- 5 full-screen sections with scroll-snap (`Hero`, `Expeditions`,
  `Why Altitude`, `Your journey`, `Book`) — great for quickly
  screenshotting each screen
- A full scroll-driven scene: sky gradient, sun/moon, drifting clouds,
  a twinkling starfield and three parallax mountain ridges that all
  shift together as you scroll — like climbing from valley to summit
- An "altitude meter" on the right edge that reads out your scroll
  position in meters and doubles as a 5-stop jump menu
- A hand-drawn trail line across the "Your journey" panel that draws
  itself in with way-points and a summit flag when the section comes
  into view
- Kinetic hero title where each letter drops into place
- Scroll-triggered reveal animations that replay both scrolling down
  *and* scrolling back up (`IntersectionObserver`)
- Animated stat counters (years guiding, climbers guided, success
  rate, group size) that count up on view
- Day / Night theme toggle (changes the whole scene, not just colors)
- English (default) / Russian language toggle, saved in `localStorage`
- Respects `prefers-reduced-motion`
- Zero build tools, zero external images — just HTML, CSS and vanilla
  JS/SVG in one file

## Getting started

1. Clone or download this repo.
2. Open `index.html` directly in a browser — that's it, no install
   step.

## Deploying with GitHub Pages

1. Make sure the site file is named `index.html` and sits in the root
   of the repo (or in a `/docs` folder).
2. Go to **Settings → Pages** in this repository.
3. Under **Source**, choose the branch (e.g. `main`) and folder
   (`/root` or `/docs`), then save.
4. GitHub will publish the site at your repo's Pages URL.

## Customizing

All content lives in one file. To personalize it:

- Update the brand name, hero tagline and CTA buttons in the **Hero**
  section.
- Replace the three trip cards (destination, days, difficulty, price)
  in **Expeditions**.
- Swap the four stats and the three chips in **Why Altitude**.
- Edit the four day markers in **Your journey**; the trail SVG itself
  is a single `<path>` you can reshape if you want a different route
  silhouette.
- Update departure dates, routes and remaining spots in **Book**, plus
  the contact email.
- Both languages (English/Russian) live in a single `dict` object near
  the top of the `<script>` tag — edit the strings there to change
  copy in either language.
- Scene and accent colors are CSS custom properties at the top of the
  `<style>` block, with a separate set under `:root[data-mode="night"]`
  for the night theme.

## Tech stack

- HTML5 + CSS (custom properties for theming, no framework)
- Inline SVG for the mountain layers and the hand-drawn trail
- Vanilla JavaScript (`IntersectionObserver`, `requestAnimationFrame`
  for scroll-linked parallax and the counters)
- Google Fonts: [Big Shoulders Display](https://fonts.google.com/specimen/Big+Shoulders+Display) +
  [DM Sans](https://fonts.google.com/specimen/DM+Sans)

## License

Feel free to use and adapt this template for your own outdoor,
travel or expedition business.
