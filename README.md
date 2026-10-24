# happy birthday akeel 🏁

A nine-slide, mobile-first birthday site. 25 October 2026.

Tap through: landing → words → constellation → the academic graph →
the things-you-like line → Red Bull & F1 in 3D → the serious bit →
the age ceremony → the button.

## Running it

Plain HTML, CSS and JavaScript. No build step, no install.
Open `index.html`, or serve the folder:

    npx http-server . -p 8080

## Layout

    index.html         the whole site
    assets/img/        photos (1–5) + square thumbs (t1–t5) + vaishnav.jpg
    assets/audio/      background track goes here (see its README)

## Notes

- **Music** is wired but not supplied. Drop `assets/audio/track.mp3` in
  and it plays, fixed and looping at 22% volume across every slide.
  It starts on the first tap — every mobile browser blocks audio before
  a user gesture.
- **The 3D models** (Red Bull can, F1 car) are built from primitives in
  three.js, not downloaded. A licensed model could not be redistributed
  here, and a free `.glb` would be a 5–20 MB dependency on a page that
  has to open on a phone. These are a few hundred bytes of geometry.
  three.js itself is fetched only when that slide is first opened.
- **The constellation** currently carries five photos. To add more, drop
  `N.jpg` + `tN.jpg` into `assets/img/` and extend the `PHOTOS` array in
  `index.html`.
- Per-slide animation loops start on enter and stop on leave, so only
  the visible slide costs battery.
