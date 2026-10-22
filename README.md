# Upgrade reports

Source of a static website: library upgrade reports written for AI agents. Plain files, no build step: what is in this folder is exactly what gets served.

| URL | File | What it is |
| --- | --- | --- |
| `/` | `index.html` | Homepage: one table row per report |
| `/llms.txt` | `llms.txt` | Entry point for AI agents: what the site is, every report and its JSON |
| `/robots.txt` | `robots.txt` | Allows all crawlers and AI agents |
| `/express/4-to-5` | `express/4-to-5.html` | Express 4 to 5 report |
| `/express/4-to-5.json` | `express/4-to-5.json` | The same findings as a JSON array |
| `/jspdf/3-to-4` | `jspdf/3-to-4.html` | jsPDF 3 to 4 report |
| `/jspdf/3-to-4.json` | `jspdf/3-to-4.json` | The same findings as a JSON array |
| any missing page | `404.html` | Points lost visitors to `/` and `/llms.txt` |
| | `.nojekyll` | Tells GitHub Pages to publish the files as they are |

## Adding a report

1. Add `<package>/<from>-to-<to>.html` and `<package>/<from>-to-<to>.json`, using the Express pair as the template. Keep the two identical: same findings, same order, same ids, same text.
2. Add a row at the top of the table in `index.html`.
3. Add the HTML and JSON links under `## Reports` in `llms.txt`.
4. Commit and push to the `main` branch. GitHub Pages republishes in a minute or two.
