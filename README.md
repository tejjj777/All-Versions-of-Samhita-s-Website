[README.md](https://github.com/user-attachments/files/32348723/README.md)
# Samhitha Ayyagari — culinary portfolio

A two-page portfolio for a Culinary Management student in Chicago: 18 plated dishes, a résumé that
prints out of a kitchen printer, three colour themes, and a 3D knife and fork in the hero.

Plain HTML, CSS and JavaScript. No framework, no build step, no dependencies.

## Run it

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy it

Push to GitHub and turn on Pages (main branch, root). Any static host works — upload the folder and
keep the layout. Serve over HTTPS so clicking her email copies it to the clipboard.

## What's in here

| Path | What it is |
| --- | --- |
| `index.html` | Home: hero, about, experience, dish preview, résumé, contact |
| `work.html` | All 18 dishes, with a pop-up for each |
| `images/` | Dish photos (3 sizes each), about photo, theme previews, link-preview image |
| `three.min.js` | three.js r128 (MIT), self-hosted for the 3D knife and fork |
| `Samhitha-Ayyagari-Resume.pdf` | The file the download button hands over |
| `CLAUDE.md` | Full context, house rules and open items — read this before editing |

## Some of what it does

- **Three themes** — black + pink, black + gold, red + black. Chosen once, remembered after that.
- **A cloche intro** on a first visit. Skippable, and skipped for anyone who prefers less motion.
- **A résumé as a kitchen ticket** that feeds out of an expo printer as you scroll to it.
- **Steam** rising off the dish photos on hover.
- **Two hidden extras.** One of them is for the person who built it. Type things and see.

## Credits

Built by me, her husband. Photos by her. three.js is MIT-licensed; fonts come from Google Fonts.


[CLAUDE.md](https://github.com/user-attachments/files/32348746/CLAUDE.md)# Samhitha Ayyagari — culinary portfolio

Context for whoever picks this up (human or Claude Code). Read this before changing anything.

## What this is

A two-page portfolio site for Samhitha Ayyagari, a Culinary Management student at Kendall College
(National Louis University) in Chicago. It exists so hiring managers can see her plated dishes,
read her résumé and contact her. She is open to part-time **expeditor, line cook and prep cook**
roles. Tone: a fine-dining menu — dark, serif, unhurried, with a few jokes hidden in it.

## How it is built

Plain static files. **No build step, no framework, no package manager, no dependencies to install.**
All CSS and JavaScript is inline in the two HTML files. To change something, edit the HTML directly.

```
index.html                     home page (~104 KB, everything inline)
work.html                      dish gallery (~82 KB, everything inline)
three.min.js                   three.js r128, MIT, self-hosted so there is no CDN dependency
Samhitha-Ayyagari-Resume.pdf   the résumé the button downloads
images/                        18 dishes (3 sizes each), about photo, 3 theme previews,
                               share.jpg (link preview), utensils.webp (phone still)
```

Only outside request: Google Fonts (DM Serif Display, Lora, Playfair Display, IBM Plex Mono).

## Deploying

GitHub Pages from the repo root works as is. So does Netlify, Vercel or any static host —
upload the folder, keep the layout. The site must be served over HTTPS for the
"click the email to copy it" behaviour to use the clipboard (there is a fallback).

## How things work

**Themes.** Three: `blossom` (black + pink, default), `gold`, `red`. Set as `data-theme` on `<html>`
and driven by CSS custom properties (`--accent`, `--accent-fill`, `--ink`, `--base`, `--line` …).
A script in `<head>` applies the saved theme before the first paint so there is no flash.
A picker opens once on a visitor's first visit; the Theme button in the nav opens it any time.

**Stored in the visitor's browser** (localStorage): `sa-theme` (chosen theme), `sa-theme-seen`
(the picker has been offered), `sa-intro` (the intro has played), `sa-special` (last featured dish,
so it does not repeat).

**The moving parts.** Silver cloche intro on a first visit (skippable, desktop and phone).
A 3D knife and fork in the hero (three.js, desktop only — phones get `images/utensils.webp`).
Steam on dish photos on hover. A résumé that prints out of an expo printer when scrolled to.
A scroll progress bar with section ticks. "Tonight's special" card linking to a random dish.
A signature that draws itself above the footer. A rotating "Open to … roles" tag in the nav.

**Easter eggs.** Typing `chef` rains forks and knives. Typing `tej` starts a 15-second shower of
hearts and compliments that fakes ending at 5 seconds, then slams up "Oh, you thought I was done?"
at 6 seconds. Tapping the `<3` in the footer three times rains forks and knives (that is the phone
route, since phones have no keyboard). **Tej is her husband — the `tej` one is a private joke, keep it.**

**Deep links.** `work.html#dish-07` opens that dish's pop-up and clears the hash.

Everything with motion is turned off or shortened for visitors who have "reduce motion" on.

## House rules

- No framework, no build step, no npm. If a change seems to need one, it does not.
- Keep it working with JavaScript switched off: content first, effects layered on top.
- Keep all three themes working. Check colour contrast when touching colours.
- Test at 1440px, ~800px and 390px. The nav is tight between 640 and 900px — check it there.
- Do not add anything that delays the first screen. Phones must not download three.js.
- Verify visually before saying something is done. Screenshots, not assumptions.

## Open items

1. **Her own résumé PDF.** The one in the repo was generated from her résumé text. If she sends a
   new one, replace the file under the same name — nothing else changes. Her PDF still says
   "part-time server position" in the objective; the site now says expeditor / line cook / prep cook.
2. **Link previews use relative paths.** In both HTML files the `og:image`, `og:url` and
   `twitter:image` tags start with `./`. Once the domain is live, swap those for the full address
   (e.g. `https://samhithaayyagari.com/images/share.jpg`); some sites ignore relative ones.
3. **Dish text.** The 18 descriptions and "what was hard about it" lines are written in her voice.
   She should read them once and correct anything she would not say.
4. **Nice to have, not started:** a working QR code on the ticket (needs the final address), an
   allergen filter on the dishes, a print stylesheet, a custom 404 page, a "view as menu" switch.

   # Samhitha Ayyagari — culinary portfolio

Context for whoever picks this up (human or Claude Code). Read this before changing anything.

## What this is

A two-page portfolio site for Samhitha Ayyagari, a Culinary Management student at Kendall College
(National Louis University) in Chicago. It exists so hiring managers can see her plated dishes,
read her résumé and contact her. She is open to part-time **expeditor, line cook and prep cook**
roles. Tone: a fine-dining menu — dark, serif, unhurried, with a few jokes hidden in it.

## How it is built

Plain static files. **No build step, no framework, no package manager, no dependencies to install.**
All CSS and JavaScript is inline in the two HTML files. To change something, edit the HTML directly.

```
index.html                     home page (~104 KB, everything inline)
work.html                      dish gallery (~82 KB, everything inline)
three.min.js                   three.js r128, MIT, self-hosted so there is no CDN dependency
Samhitha-Ayyagari-Resume.pdf   the résumé the button downloads
images/                        18 dishes (3 sizes each), about photo, 3 theme previews,
                               share.jpg (link preview), utensils.webp (phone still)
```

Only outside request: Google Fonts (DM Serif Display, Lora, Playfair Display, IBM Plex Mono).

## Deploying

GitHub Pages from the repo root works as is. So does Netlify, Vercel or any static host —
upload the folder, keep the layout. The site must be served over HTTPS for the
"click the email to copy it" behaviour to use the clipboard (there is a fallback).

## How things work

**Themes.** Three: `blossom` (black + pink, default), `gold`, `red`. Set as `data-theme` on `<html>`
and driven by CSS custom properties (`--accent`, `--accent-fill`, `--ink`, `--base`, `--line` …).
A script in `<head>` applies the saved theme before the first paint so there is no flash.
A picker opens once on a visitor's first visit; the Theme button in the nav opens it any time.

**Stored in the visitor's browser** (localStorage): `sa-theme` (chosen theme), `sa-theme-seen`
(the picker has been offered), `sa-intro` (the intro has played), `sa-special` (last featured dish,
so it does not repeat).

**The moving parts.** Silver cloche intro on a first visit (skippable, desktop and phone).
A 3D knife and fork in the hero (three.js, desktop only — phones get `images/utensils.webp`).
Steam on dish photos on hover. A résumé that prints out of an expo printer when scrolled to.
A scroll progress bar with section ticks. "Tonight's special" card linking to a random dish.
A signature that draws itself above the footer. A rotating "Open to … roles" tag in the nav.

**Easter eggs.** Typing `chef` rains forks and knives. Typing `tej` starts a 15-second shower of
hearts and compliments that fakes ending at 5 seconds, then slams up "Oh, you thought I was done?"
at 6 seconds. Tapping the `<3` in the footer three times rains forks and knives (that is the phone
route, since phones have no keyboard). **Tej is her husband — the `tej` one is a private joke, keep it.**

**Deep links.** `work.html#dish-07` opens that dish's pop-up and clears the hash.

Everything with motion is turned off or shortened for visitors who have "reduce motion" on.

## House rules

- No framework, no build step, no npm. If a change seems to need one, it does not.
- Keep it working with JavaScript switched off: content first, effects layered on top.
- Keep all three themes working. Check colour contrast when touching colours.
- Test at 1440px, ~800px and 390px. The nav is tight between 640 and 900px — check it there.
- Do not add anything that delays the first screen. Phones must not download three.js.
- Verify visually before saying something is done. Screenshots, not assumptions.

## Open items

1. **Her own résumé PDF.** The one in the repo was generated from her résumé text. If she sends a
   new one, replace the file under the same name — nothing else changes. Her PDF still says
   "part-time server position" in the objective; the site now says expeditor / line cook / prep cook.
2. **Link previews use relative paths.** In both HTML files the `og:image`, `og:url` and
   `twitter:image` tags start with `./`. Once the domain is live, swap those for the full address
   (e.g. `https://samhithaayyagari.com/images/share.jpg`); some sites ignore relative ones.
3. **Dish text.** The 18 descriptions and "what was hard about it" lines are written in her voice.
   She should read them once and correct anything she would not say.
4. **Nice to have, not started:** a working QR code on the ticket (needs the final address), an
   allergen filter on the dishes, a print stylesheet, a custom 404 page, a "view as menu" switch.

