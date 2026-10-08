# Sky Re — website design preview

The current approved design pass is a static, responsive preview with 20 page views. The dedicated News page has six equal cards in a grid; homepage news, portfolio and Team collections retain their sliders. Brand colours, original logo/pattern artwork, Cairo typography and existing motion are preserved.

Revision 06 uses the supplied `skyre-footer-logo.png` across all footers and `hero-icon-art.png` above the Home hero photograph. The crescent retains its original colours and proportions; its main tips align with the photograph's right and bottom midpoints as the layout resizes.

Revision 07 sets the video background pattern to 50% opacity. Photographs fit completely within their frames without stretching or zoom cropping; Home hero and story images use their natural proportions, while collection cards retain equal heights.

Revision 08 removes the artwork from all CTA sections and replaces the Contact location photograph with a muted interactive map of Riyadh. The map shows the city, without claiming an unconfirmed office address.

Revision 09 removes the About and Careers hero patterns. Eight new local Unsplash photographs replace the hero patterns on Portfolios, Partners, Broker Information, Claims Information, Contact, both Portfolio Detail pages and Legal & Regulatory. Photo heroes use natural proportions, fit the complete image and stack below 900 px. Credits and source links are in `ASSET-SOURCES.md`.

For Webflow, recreate the location block with a two-column Grid and place the iframe from the `location` renderer in a Code Embed. Keep its accessible title, map attribution and external map link. Apply the `.location-map` styles and stack the Grid below 900 px. This follows Webflow's [Code Embed workflow](https://help.webflow.com/hc/en-us/articles/33961332238611-Custom-code-embed) and OpenStreetMap's [iframe export](https://wiki.openstreetmap.org/wiki/Export); no custom map application is required. The map needs an internet connection. Replace the city extent with the approved office location when supplied.

## Publish on GitHub Pages

Upload the contents of this folder to the root of your GitHub repository, including `assets/`. Do not upload the local backup or the original proposal, RFP, brand kit, ZIP packages or earlier versions.

In your repository, open **Settings → Pages → Build and deployment**. Select **Deploy from a branch**, choose the branch containing these files (usually `main`), choose **/(root)**, then **Save**. GitHub provides the published site URL in the Pages settings. There is no build command, package installation or custom Actions workflow required.

Official instructions: [Configure a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), [Create a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## Files to keep

| File | Purpose |
| --- | --- |
| `index.html` | Website entry point and design review controls. Required at the repository root. |
| `content.js` | Content for all 20 page views. |
| `preview.js` | Page rendering, navigation, profiles, filters and dialogs. |
| `preview.css` | Brand styling, typography and responsive page layouts. |
| `fonts.css` | Locally hosted Cairo font definitions. |
| `motion.css`, `motion.js` | Entrance motion, portrait interactions and reduced-motion support. |
| `slider.css`, `slider.js` | Responsive sliders and the News page card-grid rules. |
| `assets/` | Only referenced photographs, original brand SVGs, video background, portraits, fonts and font licence notices. |
| `.nojekyll` | Keeps the Pages deployment as plain static files. |
| `ASSET-SOURCES.md` | Photo credits and disclosure of fictional generated portraits. |
| `README.md`, `.gitignore` | Publishing instructions and repository housekeeping. |

Keep the filenames and folder structure intact: all asset links are relative, so the preview works under a GitHub project URL such as `https://OWNER.github.io/REPOSITORY/`.

Page navigation currently uses hash URLs such as `/#home`, `/#team` and `/#news`. These are separate design views within the static preview. Dedicated production URLs and a CMS are part of the later implementation, not this GitHub Pages preview.

## Local preview

Open `index.html` directly, or serve this folder with any static web server. If Python is installed, run `python -m http.server 8773 --bind 127.0.0.1` here and open `http://127.0.0.1:8773/`.

## Content status

This is a design preview. Articles, product categories, profiles, biographies, addresses, contact emails and legal copy are illustrative. Saudi team portraits are generated fictional people, not actual employees. The video area is a poster and viewing-state demonstration; the final company film has not been supplied. The review toolbar is intentionally retained so this publishes the current review experience.

Previous verification covered all 20 views at desktop and mobile sizes. The latest News grid was additionally checked at 1440, 900 and 390 px, with six equal 600 px cards, no horizontal/content overflow and no News-page slider controls.

Revision 10 removes the artwork pattern from the News page hero.

Revision 11 removes the News article hero pattern and replaces the Vacancy Detail hero pattern with a local Unsplash workplace photograph, using the responsive photo layout.

Revision 12 rounds only the Home hero photograph's lower-right corner with a responsive CSS clip that follows the supplied crescent. Its edge overlaps beneath the artwork; the other corners remain square. The same CSS can be added through a Webflow custom-code embed.
