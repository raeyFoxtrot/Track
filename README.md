# BNAF 2027 — Final Flight Edition

## Open the website

Extract the ZIP first. Open `index.html` in Chrome, Edge, Firefox or Safari. Keep all files and the assets folder together. No npm, build command, API key or backend is needed.

Each navigation item opens a separate HTML page in the same browser tab. Google Fonts and Google Forms require internet; system fonts are used when Google Fonts is unavailable.

For development you can also serve the folder with `python -m http.server 8000` and open `http://localhost:8000`.

## Light theme (current)

The site now uses a light palette drawn from the reference board: white and cream backgrounds, beige and golden-beige accents, and shades of blue (navy, royal, icy) for contrast. All colours are variables at the top of `styles.css` (`--cream`, `--beige`, `--gold`, `--blue-700`, `--navy`, and so on); change them there.

## Shared footer

Every page uses the same footer: a "Presented by the Aeromodelling Club, IIT Kanpur, in association with Techkriti ’27" block, a Quick Links column, a Follow Us column with the three Instagram links, and "© 2027 IIT Kanpur. All rights reserved." A flight lane runs along its top edge, with flowing dashes and three aircraft crossing continuously. It is CSS only and stays still when the device asks for reduced motion. Footer styles live in `styles.css`, not in the pages. If you edit the footer, copy the change into all five HTML files.

## Design

- Typography: Barlow Condensed for headlines, DM Sans for text. 18px body text on desktop, 17px on mobile.
- Homepage: full-screen BORN TO TAKE FLIGHT hero with the supplied film under a cream wash, animated orbit and flight path, and a blue aircraft strip.
- A 1.25-second first-visit arrival sequence; dismiss with Skip intro or Escape.
- Cross-page transitions in browsers that support them; ordinary navigation everywhere else.
- Device reduced-motion and data-saving preferences are respected.

## File guide

- `index.html`: homepage and cinematic video background.
- `workshops.html`: workshops; soft-blue theme.
- `gallery.html`: photo archive; golden-beige theme.
- `team.html`: organisers; periwinkle-blue theme.
- `register.html`: Google Form registration; golden-beige theme.
- `styles.css`: light-theme colours, typography, header, footer, animation and responsive layouts.
- `script.js`: navigation, accordions, seamless scrolling strip and Google Form integration.
- `config.js`: event details, contact email, workshops, team, gallery and Google Form links.
- `assets/`: supplied festival video, extracted poster, supplied logo artwork and favicon.

## Connect your Google Form

1. In Google Forms, make your form available to the intended respondents and copy its responder link.
2. Open `config.js` in a text editor.
3. Paste it between the quotes after `googleFormUrl`. Full Google Forms `/viewform` URLs and `https://forms.gle/...` short links are supported.
4. For an embedded form, paste the FULL responder URL after `googleFormEmbedUrl`. Do not paste iframe HTML or an `/edit` URL. The script adds `embedded=true` automatically. If `googleFormUrl` already contains a full responder URL, no second link is necessary.
5. Save and reload. The registration card will show “Open registration form” and, when possible, “Fill the form on this page”. The iframe only loads when requested.

The Google Form owns its fields and responses. This site does not submit, store, or email registration data. Google account restrictions and form availability are controlled in Google Forms. A short link alone can open in a new tab but cannot be embedded.

The form URL has not been provided, so the delivered version honestly displays “Registration details will be announced soon.” No test form or fake submission has been added.

## Change content

Edit the clearly labelled values in `config.js`:

- `dates`, `venue`, `organizer`, `email`
- `workshops`: title, tag and description
- `team`: name, role, bio and optional photo path
- `gallery`: image path, accessible description and caption

Place images in `assets/` and reference them as `assets/your-image.jpg`. Use normal quotes and keep commas between entries. Do not put private information or credentials in public website files. The team editor from the old sample stored changes in one visitor's browser; this version uses a central configuration so published edits are consistent for all visitors.

For headlines and other static wording, edit the corresponding HTML page. For the palette, edit the variables at the top of `styles.css`. The event name and year also appear in the title, metadata, navigation, registration card and footer; update those together for a later edition.


## Media and content status

The homepage background uses the supplied video. The gallery is reserved for photographs; its previous video player has been removed. The poster is a frame from the supplied video. The uploaded logo artwork is no longer displayed. Its blue palette inspires the page themes. Original images remain in assets for optional future use. Reference websites inspired the presentation; their graphics and code were not copied.

Dates and venue remain unannounced as in the source. The source's example contact email and “Full Name” team entries have been replaced with honest empty states. Add confirmed contacts, team details and archive photographs before launch. Workshop subjects are retained from the original sample; confirm the programme before publishing.

## Hosting

Upload all five HTML pages, `styles.css`, `script.js`, `config.js` and `assets/` together to your static website host. `index.html` should be at the root. Keep filenames unchanged so navigation continues to work. This delivery does not deploy or replace a live website.

## Accessibility and verification

Includes a keyboard skip link, semantic sections, native workshop disclosures, responsive menu with Escape support, visible focus states, reduced-motion handling. The homepage uses the supplied video with a poster fallback. The CSS has been rebuilt as one coherent stylesheet instead of accumulating overrides. Reduced-motion and data-saving preferences disable automatic playback. Background video pauses off-screen, when the tab is hidden.

JavaScript syntax and all five pages’ local asset, navigation and anchor consistency were checked. Browser access to the local preview was blocked in this environment, so final visual and interaction checks should be made after opening the files locally. A real Google Form cannot be verified until its link is supplied.
