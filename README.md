# Referral Dashboard

A public, read-only dashboard for Trip Hack Hub's affiliate/referral program
pipeline. Hosted free via GitHub Pages.

**Live:** https://zerotouchai.github.io/referral-dashboard/

## How it works

- The actual pipeline (research, scoring, status tracking) lives in a private
  companion repo and uses a GitHub Projects board as the editing surface.
- After each scan, that repo pushes a fresh `data/dashboardData.json` snapshot
  here.
- `index.html` is a static page (vanilla JS + Chart.js) that reads that JSON
  and renders it. No backend, no database, nothing to pay for.
- This dashboard is **view-only**. Editing status/marking a program applied
  still happens on the private Projects board — this page just displays the
  result.

## Note on what's public here

Only the fields needed for the dashboard are synced: program name, topic,
commission note, score, and status. Personal referral/tracking codes are
never included — the `signup_url` field is always the generic public
sign-up page for a program, not any tracking link.

## Versioning

The dashboard version is shown next to the title and is defined by
`APP_VERSION` near the top of the script in `index.html`. **Bump it on every
change** and add a line below.

## Changelog

- **v1.1.0** — Compass favicon, version badge, "Powered by zerotouchai.com"
  footer link, new **YouTube Ideas** page (reference video URLs used as
  inspiration for new videos).
- **v1.0.0** — Candidates, My Referrals, Search Requests, Video Ideas.
