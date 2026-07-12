# European gay sauna directory - version 1.0 audit

This is a static prototype: no hosting bill, no database, no paid map tiles and no paid review API.

The 12 July 2026 audit classifies listings as `verified`, `partial`, or `unresolved`. Read `AUDIT-REPORT.md` before publishing updates. A verified listing means that its main visitor facts were supported by a current first-party page; coordinates are still approximate address points, not independently surveyed entrances.

## Open it

Open `index.html` in a modern browser while connected to the internet. The country outline is loaded from a free public JavaScript package; the venue data itself stays local in `venues.js`.

## Update a listing

1. Open `venues.js` in a text editor.
2. Find the venue by its `id`.
3. Update the field, `source`, and `verifiedAt` date.
4. Run `node validate.mjs` if Node.js is available.
5. Refresh `index.html`.

The schedule uses Sunday-to-Saturday arrays. Each time window is `[startHour, endHour]`; an end after 24 means after midnight. Leave `schedule` empty if the timetable is event-led or uncertain. The app will then avoid an unreliable Open now claim.

## Corrections workflow

Each venue has a **Suggest correction** button. It copies a small correction template containing the venue name, changed field, replacement value and source URL. For a public version, add a project email address or link that button to a free GitHub issue form.

## Data policy

- Prefer the venue's own website for hours, price, access policy and facilities.
- Use an established LGBTQ+ directory only when the venue has no usable current page.
- Store the exact fact source and the date checked.
- Recheck every 90-120 days and before major holiday periods.
- Do not copy Google ratings into this static dataset. The Google Maps link shows the current rating and review count directly.
- Treat coordinates as approximate address points and verify them before a production launch.

## Free publishing options

The folder can be published unchanged with GitHub Pages, Cloudflare Pages or Netlify's free tier. Their limits and terms can change, so review the current terms before choosing one.
