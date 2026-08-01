# For LJ 💛 — International Girlfriend's Day site

A single-page site built around *discovery*: a loading screen, name-reveal
intro, floating photos/balloons/sparkles (tap a star for a memory), a
tap-to-play video memories section, flip-to-reveal gallery photos, a
60-note flower garden, four secrets hidden in scroll-triggered corners,
click-to-reveal "Reasons I Love You" and "If You Ever Doubt Yourself"
cards, a moments timeline, click-to-open letters, a rigged spin-to-win
wheel, a second "Spin Our Story" wheel with six genuinely random outcomes,
"Little Things You Never Knew" confessions, an "Open My Journal" button,
a progressive "Favourite Things About You" reveal, five labeled "open
when..." envelopes, a secret "Don't Press" button and a clickable finale
heart, random love-reminder toasts, and a full-screen closing message —
plus background music. Everything lives in one file: `index.html`.

## 1. Add your media

31 real photos, 4 real videos, and your song are already in `assets/photos/`,
`assets/videos/`, and `assets/audio/song.mp3`, wired into the site (see
each folder's README.txt for exactly where things are used, and which
extra photos aren't placed anywhere yet). Still missing: a solo photo of
you at `assets/photos/me.jpg`, used as the spin-wheel prize — until it's
added, the wheel just shows a 😏 emoji instead, so nothing is broken.

## 2. Edit the text

Open `index.html` and find the `CONFIG` block near the top of the
`<script>` tag (search for `const CONFIG`). Everything you'd want to
personalize lives there in plain arrays:

- `notes` — one per flower in the garden (60 currently)
- `photoSecrets` — the jokes revealed when she flips a gallery photo (hover on desktop, tap on mobile); a gallery entry can also set its own `secret` directly to override this
- `hiddenCorners` — the secrets hidden in the corners of the flower garden, revealed as she scrolls
- `reasons` / `affirmations` / `littleThings` — the click-to-reveal card grids
- `timelineMoments` — the vertical timeline entries, also what a clicked star pulls from
- `favouriteThings` — revealed one at a time via the "Reveal Another" button, also feeds the journal button and two "Spin Our Story" slices
- `places` — used by the "A Place We'll Visit Together" slice on the second wheel
- `envelopes` — the 5 labeled "open when..." letters, also feeds the "A Love Letter" slice on the second wheel
- `loadingLines` / `reminders` / `compliments` — loading screen text, periodic toasts, and the random line under the hero
- `secretReveal` — what the "Don't Press" button says once pressed
- `heartReveal` — what shows when the heart in the finale is tapped
- `wheelPrizes` — the labels on the rigged spin-to-win wheel
- `gallery` / `floatPhotos` — which photos go where, and gallery captions
- `videos` — the tap-to-play video cards (file, poster image, caption)
- `memories` — long-form click-to-open letters (title + array of paragraphs); add more here any time
- `winText` — what shows when she "wins" the rigged wheel
- `endingMessage` — the full-screen closing message

You don't need to touch anything below `/* ===== */` — that's layout code.

## 3. Preview it locally

```bash
cd ~/loni-girlfriends-day && python3 -m http.server 8080
```

Then open http://localhost:8080 in a browser.

## 4. It's already live

Deployed via GitHub Pages, repo named just `loni` for the cleanest possible
free URL:

```
https://demolafc-netizen.github.io/loni/
```

To push future changes: edit `index.html`, then from this folder:

```bash
cd ~/loni-girlfriends-day
git add -A
git commit -m "describe the change"
git push origin main
```

It goes live within a minute or two of pushing. Note this is a **public**
repo (required for free GitHub Pages) — the photos/videos in it are
technically visible to anyone who finds the repo on GitHub, not just via
the QR code.

## 5. Turn the URL into a QR code

Ask me to generate the QR code (or use
any QR generator) — I'll produce a PNG you can print or send her directly.
