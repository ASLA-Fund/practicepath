# Path to Practice

**Studio. Practice. License.** A LABash resource.

Path to Practice is a guide for landscape architecture students and emerging professionals, from the classroom to career and licensure. It brings together programs from ASLA, CELA, CLARB, CSLA, LAAB, and LAF, organized by where you are on the path. It is maintained by ASLA.

Live site: https://asla-fund.github.io/practicepath/

## Updating content (no coding needed)

The site reads two spreadsheet files in this repository. Edit them in Excel or Google Sheets, export as CSV with the same column headers, and upload them here (Add file › Upload files). The site updates within a minute or two.

### `resources.csv`: one row per program

- **Stage columns** (Study, Fund, Gain Experience, Graduate & Start Working, Prepare for the LARE, Get Licensed): put `Y` on every stop where the resource belongs.
- **Featured On Stops:** the stop numbers (1 to 6) where the resource appears in the top six cards, separated by semicolons. Example: `2;5`.
- **Status:** set to `Retired` to hide a row without deleting it.

### `deadlines.csv`: one row per date

- **Date** and **End Date** use `YYYY-MM-DD`. Leave End Date blank for single-day deadlines.
- Past dates disappear from the site automatically, and the next four upcoming dates fill the "Coming up" cards.

### Stop checklists

The "Start here" checklists for each stop are in `index.html`. Search for `todo:` to find them.

## Settings

Near the top of `index.html` there is a `PP_CONFIG` block with two settings:

- **`ga4`:** paste a Google Analytics 4 measurement ID to turn on analytics. The site then reports stop selections, searches, need filters, calendar adds, printed checklists, copied links, and every click out to a partner site, with the resource and organization.
- **`contactEmail`:** add an address to show "Suggest a resource" and "Contact" links in the footer.

## Links, QR codes, and tracking

Every stop has its own link:

| Stop | Link |
|---|---|
| Study | `#study` |
| Fund | `#fund` |
| Gain Experience | `#experience` |
| Graduate & Start Working | `#graduate` |
| Prepare for the L.A.R.E. | `#lare` |
| Get Licensed | `#licensed` |

For example: `https://asla-fund.github.io/practicepath/#lare`

Add `?src=` to any link or QR code to see where visitors came from. For example, `https://asla-fund.github.io/practicepath/?src=flyer#lare`.

Links out to partner sites carry `utm_source=pathtopractice`, so each organization can see Path to Practice traffic in its own analytics.

When `PathToPractice.org` is set up, point it here with a permanent (301) redirect, and update `SITE_URL` in `index.html` so copied stop links and printouts use the new address.

## Files

- `index.html`: the site. It also contains a backup copy of the data, used only if the CSV files can't be loaded.
- `resources.csv`, `deadlines.csv`: the live content.
- `og-image.png`: the image shown when the link is shared in Teams, email, or social media.
