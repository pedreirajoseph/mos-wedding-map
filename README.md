# Mountain Of Stone Media — Wedding Venue Map

An interactive map of every venue and church we've filmed weddings at, embedded at the top of the Films page on mountainofstonemedia.com.

## Files
- **index.html** — the map itself (this is what gets hosted and embedded).

## How updating works (three independent layers)
- **What's on the map (venues):** a Google Sheet. Add a row, the map updates on its own. See the setup guide.
- **How the map looks (colors, dots, captions):** the code in `index.html`.
- **How big it is on the page:** dragged in the Wix editor. The map auto-fits its box, so resizing won't break it.

## Connecting the Google Sheet
1. Publish the sheet to the web as CSV (see the setup guide).
2. In `index.html`, paste that link between the quotes on the `CSV_URL` line near the top of the script.
3. Save. Until a link is set, the map uses the built-in venue list in the file.

The sheet's columns are read by name: **Venue, City, Latitude, Longitude, Film Links (comma-separated).** Multiple YouTube links in the Film Links cell become multiple clickable films on that dot.

## Hosting & embedding
- Hosted free via **GitHub Pages** (Settings → Pages → deploy from `main`, root).
- Embedded on the Wix Films page as a site/iframe pointing at the Pages URL — so future code changes never require editing Wix again.
