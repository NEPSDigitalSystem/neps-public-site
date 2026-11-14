# NEPS Public Site

Public-facing project and technical status page for the **NEPS Digital System** — an adolescent and youth mental health research surveillance platform across Ghana, Sierra Leone, and Tanzania.

## Purpose

This repository contains a static HTML site automatically deployed via GitHub Pages. It provides external stakeholders, funders, ethics review boards, and institutional partners with a transparent, read-only technical overview of the platform architecture, implemented baseline systems, and active governance dependencies without exposing private source code, secrets, or sensitive participant records.

## Deployment

This site is automatically deployed via GitHub Pages from the `main` branch.

**Live URL:** `https://nepsdigitalsystem.github.io/neps-public-site`

## Evolution & Governance Provenance

*   **August 2026 (Initial Release):** Early architectural scaffolding; technical progress was paused behind critical external dependencies (absence of official CRFs, wireframes, and API credentials).
*   **September 2026 (Factual Realignment):** Factual corrections applied to accurately reflect live codebase states (e.g., scaffolding vs. live binding).
*   **October 2026 (Baseline V3.1 Handover):** The NEPS Board of Directors and NDS Team delivered the official **Master CRF V3.1 Handover package** (223-item dictionary, 73 core clinical psychometric items, and golden fixtures), establishing **Track A (Baseline Scope)**.
*   **November 2026 (V3.2 Data Dictionary Integration):** Received and implemented **REDCap Data Dictionary Version 3.2** from Bernard Arhin (KATH / REDCap Field Validation Committee), expanding to 227 variables with automated Date-of-Birth age calculation, explicit consent gating (`survey_consent`), and survey date automation (`tdate`).

## Updating Content

To update the site:

1. Edit `index.html` directly
2. Commit and push to `main`
3. GitHub Pages deployment updates within 1–2 minutes

### Content Guidelines
*   **Status Indicators:** Use qualitative statuses (`Live`, `Active Dev`, `Partial Dev`, `Drafting`, `Blocked`) rather than arbitrary percentages to maintain verifiable claims.
*   **Public Repository Safety:** Never commit database credentials, REDCap API tokens, internal server IP addresses, or unanonymized participant data.
*   **Clinical Scope Separation:** Clearly distinguish between **Track A (Verified Baseline Scope)** and **Track B (Provisional Longitudinal Layer)**.

## Structure

```
.
├── index.html               # Main self-contained status report (academic light palette)
├── neps_report_summary.md   # Copy-pasteable status report summaries and templates for leadership
├── README.md                # This documentation file
└── .gitignore               # Standard ignore rules
```
