# NEPS Digital — Repository Summary & Status Report Resources

This document contains copy-pasteable assets for Lead DevOps Engineer **Damien Nsoh Ayine** to share with project coordinator **Dr. Linda Banning** and the NEPS Board of Directors for status reporting and partner engagement.

---

## 1. Chat/Email Message Template

**Subject:** NEPS Digital Platform — November 2026 Public Status Mirror & V3.2 Technical Progress

Hi Dr. Linda Banning,

I trust you are doing well.

I have updated the publicly accessible status mirror for the NEPS Digital platform to reflect the significant progress achieved following the **Master CRF V3.1 Handover** in October, as well as our recent integration of **Mr. Bernard Arhin's REDCap Data Dictionary Version 3.2** (dated 26-OCT-2026).

This page allows institutional partners, ethics boards, and external coordinators to monitor our architectural milestones and active dependencies without accessing the private codebase organization:

*   **Live Public Status Page (Hosted on GitHub Pages):** [https://nepsdigitalsystem.github.io/neps-public-site/](https://nepsdigitalsystem.github.io/neps-public-site/)
*   **Public Repository Mirror:** [https://github.com/nepsdigitalsystem/neps-public-site](https://github.com/nepsdigitalsystem/neps-public-site)

### Key Technical Achievements (Track A Baseline Scope):
1.  **V3.1 Handover & V3.2 Integration:** The full 227-variable REDCap data dictionary is now integrated across all tiers. This includes automated age calculation from Date of Birth (`dob`), explicit consent gating (`survey_consent`), automated survey timestamping (`tdate`), and 12–24 age-eligibility validation.
2.  **Scoring Warehouse Live:** The data platform scoring engine successfully ingests and computes the 9 psychometric scales (K6 MHDI, BRS, MSPSS, GSE, EPI, ESI, SBI, PFI, and the NSES composite score) across all 150 baseline cohort records with 100% mathematical parity against golden fixtures.
3.  **Hardened Authentication & Scoped Portals:** The backend provides hardened JWT authentication (`POST /api/auth/login`) with country-level scoping (Ghana, Sierra Leone, Tanzania) and role-based access control powering the Next.js clinical dashboards.
4.  **Disaster Recovery Verified:** The Point-In-Time-Recovery (PITR) operational runbook is formally tested and documented (`neps-infrastructure/docs/pitr-runbook.md`).
5.  **ML/AI Direct Warehouse Link:** The ML/AI repository now reads directly from the live PostgreSQL warehouse (`nds_v31_source` / `nds_v31_derived`) and trains on a verified 240-column baseline dataset.

### Current External Dependencies (Track B Scope):
*   **Track B Longitudinal CRFs:** We are awaiting the clinical team's finalization of the Case Report Forms for the 24-month monthly follow-ups (M1–M24, 14 parameters) and wave schedules (M06, M12, M18, M24).
*   **Production REDCap Credentials:** KATH/KCHR (`https://kchr.org`) live API token issuance will follow when field recruitment starts. Development continues smoothly against the V3.2 mock server.
*   **Institutional TLS Certificate:** Awaiting final SSL certificate procurement from KNUST IT for the on-premise server stack.

Please let me know if you would like me to adjust any details for the board briefing.

Best regards,

**Damien Nsoh Ayine**  
Lead DevOps & Infrastructure Engineer, NEPS Digital System

---

## 2. Repository Status Table for Report

*Note: You can copy and paste the Markdown table below directly into any Markdown editor or import it into Word/PDF reports.*

| Repository | Purpose & Core Milestones | Lead Developer | Last Activity | Status |
| :--- | :--- | :--- | :---: | :--- |
| **`neps-infrastructure`** | 17-container Docker stack, 4-tier network isolation, PITR WAL archiving, automated runbook, Discord alerting | Damien Nsoh Ayine | Nov 2026 | **Live / Active Ops** |
| **`neps-backend`** | FastAPI API, JWT auth (`/api/auth/login`), RBAC, country scoping, V3.1/V3.2 baseline & dictionary endpoints | Samuel | Nov 2026 | **Live (Baseline) / Active Dev** |
| **`neps-data-platform`** | ETL warehouse, Alembic 004 integrity, 9-scale scoring engine (100% golden parity), 150 baseline cohort | Frank / Isaac | Nov 2026 | **Live** |
| **`neps-portal`** | Next.js 16 portal, role dashboards (Admin, PI, Leads, Enums), mock API server, V3.2 entry form | Eric / Ama / Ghazi | Nov 2026 | **Active Dev** |
| **`neps-ml-ai`** | Direct PostgreSQL warehouse reader, 240-feature baseline dataset, 2,000-record multimodal NLP dataset | Yasmine | Nov 2026 | **Active Dev** |
| **`neps-docs`** | Operational runbooks, data ethics plans, pipeline testing guides, signed confidentiality register | Salamatu | Nov 2026 | **Active Dev** |
| **`mock-redcap-service`** | Hosted simulated REDCap API sandbox on Render, V3.2 consent/DOB generator, 150 participants | All Teams | Nov 2026 | **Live on Render** |
