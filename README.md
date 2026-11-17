# AegisCTI — Threat Intel Correlation Prototype

**Live demo:** https://aegisnetsecllc.github.io/cti-poc-test/

A single-file, front-end-only POC for a threat-intel correlation and triage dashboard. All data is mocked client-side (no backend, no real auth) — this is a UI/workflow prototype, not a production tool.

## What's in it

- **Correlated Triage** — mock CVE alerts correlated against internal assets, with risk scoring, CISA KEV / EPSS signals, and filters
- **Blast Radius Graph** — interactive SVG attack-path visualizer (threat actor → CVE → asset → crown jewel)
- **Connectors & APIs** / **Threat Intel & KEV** — mock integration hub, including a STIX/TAXII/RSS feed subscription flow
- **Internal Inventory** — mock asset/software table
- **Threat Memo generator** — builds a formatted, leadership-ready memo per alert (Exploit Details, IoCs, business impact, owning team) with a color-coded analyst risk rating, Copy/Download/Email actions, and a session Memo Archive
- **Settings** — honest platform status panel (no fake controls)

## Updating the live site

This repo has no build step — `index.html` is served directly via GitHub Pages. To publish a change:

```bash
git add index.html
git commit -m "..."
git push
```

GitHub Pages rebuilds automatically within about a minute of the push.
