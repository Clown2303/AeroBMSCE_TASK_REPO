# AeroBMSCE Web Development Recruitment Task

**Live site:** https://clown2303.github.io/AeroBMSCE_TASK_REPO/
**Repository:** https://github.com/Clown2303/AeroBMSCE_TASK_REPO

## 1. Flaws in the original website

- **Cropped group photo:** The hero photo cut off people's heads and faces, and the title box covered part of the team.
- **Tiny drone photo:** The drone was very small in a wide, empty grey strip, so the aircraft was hard to see.
- **Broken Contact link:** The Contact link opened a 404 "File not found" page because `contact.html` did not exist.
- **Crammed text:** "Who We Are" and "What We Do" were one block of text with no visual separation.
- **Hard-to-read text:** Body text was dark grey on a near-black background.
- **Stretched logo:** The logo was forced to a fixed size, which distorted it.

## 2. Design approach and UI/UX decisions

- **One stylesheet:** All colours and fonts are set once as variables in `style.css`, so every section uses the same palette and typography.
- **Single-page navigation:** The navbar links jump to sections on the same page, so none of them can lead to a missing page. Contact and Journey are separate pages that use the same navbar and styling.
- **Clear sections:** "Who We Are" has its own section with a photo. "What We Build" uses four cards instead of a bullet list, and the drone photo sits in a fixed frame so it can't stretch.
- **Hero layout:** The hero uses `object-position` to keep faces in view, and the title box sits in the top-left corner so it doesn't cover people.
- **Collapsible achievements:** Each achievement is a clickable title that opens its details and a competition photo. This keeps the page short and lets visitors open only what interests them.
- **Recruitment section:** Technical and Management roles are shown as cards side by side, with the recruitment poster and a contact box. The same card style is used throughout so the section matches the rest of the site.
- **Logo:** The navbar uses the full AEROBMSCE wordmark, so the club name is visible at the top of every page.

## 3. One problem I faced and how I solved it

The recruitment poster didn't show on the live site. The alt text appeared in its place, which meant the browser couldn't find the image. I checked the repository and found that the file was in the main folder rather than `images/`, and its name contained spaces and brackets, which broke the link. I renamed the file to `poster.png`, updated the `src` in `index.html` to match, and reloaded the live page to confirm it showed.

## Pages

- Home (hero, Who We Are, What We Build, Our Achievements, Recruitment, Partner With Us)
- Contact (separate page)
