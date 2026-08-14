# NEPS Public Site

Public-facing project page for the NEPS Digital System — a youth mental health research platform operating across Ghana, Sierra Leone, and Tanzania.

## Purpose

This repository contains a static HTML site deployed via GitHub Pages. It provides external stakeholders (funders, institutional partners, ethics boards) with a professional overview of the project without exposing private code, API endpoints, or sensitive infrastructure details.

## Deployment

This site is automatically deployed via GitHub Pages from the `main` branch.

**Live URL:** `https://nepsdigitalsystem.github.io/neps-public-site`

## Updating Content

To update the site:

1. Edit `index.html` directly
2. Commit and push to `main`
3. Changes reflect within 1–2 minutes

### What to Update
- Progress indicators when major milestones are reached
- Partner list if new institutions join
- Contact information if PI details change
- Dependency blockers when they are resolved

### What NOT to Include
- Internal architecture diagrams with IP addresses or ports
- API endpoints or URLs
- Team member personal contact details
- Links to private repositories
- REDCap tokens or database credentials
- Commit counts or fabricated metrics

## Structure

```
.
├── index.html      # Main site (self-contained, no external assets)
├── README.md       # This file
└── .gitignore      # Standard ignore rules
```

## Notes

- This is a **public** repository. Do not commit sensitive information.
- The site is intentionally single-file and self-contained to minimize maintenance.
- All styling is inline to avoid external CSS dependencies.
- Progress indicators use qualitative labels ("Foundation Laid", "Architecture Ready") rather than precise percentages to avoid unverifiable claims.
