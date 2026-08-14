# NEPS Digital — Repository Summary & Status Report Resources

This document contains copy-pasteable assets for Lead DevOps Engineer **Damien Nsoh Ayine** to share with immediate project coordinator **Dr. Linda Banning** for her status report.

---

## 1. Chat/Email Message Template (Option 2)

**Subject:** Read-only access and status mirror for NEPS Digital repositories

Hi Dr. Linda Banning,

I trust you are doing well.

As requested, I have created a publicly accessible, read-only status and mirror page for the NEPS Digital platform. This allows external stakeholders and partners to monitor our repository architecture and development status without accessing the private codebase organization.

*   **Live Status Page (Hosted on GitHub Pages):** [https://nepsdigitalsystem.github.io/neps-public-site/](https://nepsdigitalsystem.github.io/neps-public-site/)
*   **Public Repository Mirror:** [https://github.com/nepsdigitalsystem/neps-public-site](https://github.com/nepsdigitalsystem/neps-public-site)

Here is a summary of the 6 core NEPS Digital repositories and their development leads:

*   **`neps-infrastructure`** — DevOps, CI/CD, monitoring telemetry, and PITR backups (Lead: **Damien Nsoh Ayine**)
*   **`neps-backend`** — FastAPI REST API, database schemas, and REDCap proxy sync (Lead: **Samuel**)
*   **`neps-data-platform`** — ETL warehouse pipelines, data validation, and load scripts (Leads: **Frank / Isaac**)
*   **`neps-portal`** — React Next.js frontend dashboards for PI, Leads, Admin, and Enumerators (Leads: **Eric / Ama / Ghazi**)
*   **`neps-ml-ai`** — ML engine for mental health distress risk modeling (Lead: **Yasmine**)
*   **`neps-docs`** — Architecture mapping and clinical workflows (Lead: **Salamatu**)

*Note: We also host a sandbox utility called **`mock-redcap-service`** to generate synthetic multi-country responses, allowing team members to test integration pathways before real REDCap data arrives.*

If you also need to add reviewers as read-only collaborators directly inside the private organization, please send me their GitHub usernames, and I will configure their access.

Best regards,

**Damien Nsoh Ayine**  
Lead DevOps & Infrastructure Engineer, NEPS Digital System

---

## 2. Repository Status Table for Report (Option 3)

*Note: You can copy and paste the Markdown table below directly into any Markdown editor or import it into Word/PDF reports.*

| Repository | Purpose | Lead Developer / Owner | Last Activity | Status |
| :--- | :--- | :--- | :---: | :--- |
| **neps-infrastructure** | Docker Compose stack, monitoring dashboards, PITR backups, SSL reverse proxy | Damien | Aug 2026 | Active Dev |
| **neps-backend** | FastAPI API services, SQLAlchemy schemas, scheduler, REDCap proxy routing | Samuel | Aug 2026 | Active Dev |
| **neps-data-platform** | ETL pipelines, raw data warehouse loaders, sync orchestration CLI | Frank / Isaac | Aug 2026 | Active Dev |
| **neps-portal** | React Next.js web client dashboards, user login authentication, graphs | Eric / Ama / Ghazi | Aug 2026 | Partial Dev |
| **neps-ml-ai** | Scikit-learn distress risk scoring models, NLP sentiment classifiers | Yasmine | Aug 2026 | Partial Dev |
| **neps-docs** | Architecture mapping, deployment runbooks, data safety guidelines | Salamatu | Jul 2026 | Drafting |
| **mock-redcap-service** | Hosted simulated REDCap server sandbox for offline validation | Utility | Aug 2026 | Live |
