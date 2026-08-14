# NEPS Digital — Public Mirror & Status Page

Welcome to the public-facing read-only repository of the **NEPS Digital** platform.

## What is NEPS?
NEPS (**Navigating Educational Pressures and Stressors**) is a clinical-grade digital health surveillance platform designed to track and monitor the mental health, stress, and psychological resilience of youth (ages 10–24) across three African countries:
* 🇬🇭 **Ghana** (KNUST / CAIH - Kumasi, Accra, Ho, Tamale)
* 🇸🇱 **Sierra Leone** (Freetown)
* 🇹🇿 **Tanzania** (Dar es Salaam)

The system supports a **24-month longitudinal study** incorporating consent registries, psychosocial survey assessments (via REDCap sync), real-time safeguarding alerts (escalating cases of severe depression or suicidality), and AI/ML distress risk prediction models.

## Development & Security Policy
To ensure compliance with local and international data protection standards (including GDPR and national data retention policies), core development codebases, secure server configurations, database migration scripts, and questionnaire forms are hosted across private repositories in the **`NEPSDigitalSystem`** organization.

This repository serves as a **public index and status dashboard** to provide visibility to partners, researchers, and field coordinators into repository health and active work packages.

🔗 **View Live Status Page:** [NEPS Public Status Dashboard](https://nepsdigitalsystem.github.io/neps-public-site/)

---

## Repositories Index & Current Status

Here is the current implementation assessment of the NEPS Digital system (as of August 2026):

| Repository | Tech Stack | Lead Developer(s) | Status | Key Gaps / Next Steps |
| :--- | :--- | :--- | :---: | :--- |
| **neps-infrastructure** | Docker Compose, Nginx SSL, Prometheus, Grafana, Loki, Alertmanager, MinIO, Ofelia cron, WAL PITR | Damien Nsoh Ayine | **75%** | real HTTPS certs setup, Discord webhook secret configuration, restore drills. |
| **neps-backend** | Python, FastAPI, SQLAlchemy Postgres models, Alembic, APScheduler, Prometheus instrumentation | Samuel | **55%** | JWT authentication logic implementation, DB verification testing. |
| **neps-data-platform** | Python, ETL (Extract, Load, Transform), Upsert/On-Conflict rules, incremental synchronization | Frank / Isaac | **65%** | Unit test cases, logging refinements, error alert notifications. |
| **neps-portal** | Next.js 16, React 19, Tailwind CSS 4, NextAuth v5, Recharts, API integration | Eric / Ama / Ghazi | **40%** | Wire non-admin dashboards (PI, leads, enumerators), finalize layout sidebars. |
| **neps-ml-ai** | Python, Scikit-learn (TF-IDF + Logistic Regression), PKL pipelines | Yasmine | **30%** | Load PKL binaries into FastAPI, expose API predictions endpoints for the portal. |
| **neps-docs** | Markdown templates, architecture diagrams, deployment runbooks | Salamatu | **15%** | Detailed drafting of security policies, hosting runbooks, and recovery guides. |
| **mock-redcap-service** | Python, FastAPI sandbox, CSV dataset loading, hosted mock REDCap API | *External Utility* | **100%** | Active development sandbox hosted on Render. |

---

## Team Contact
* **Project Coordinator:** Dr. Linda A. Banning — [linda.banning@neps-health.org](mailto:linda.banning@neps-health.org)
* **Lead DevOps & Infrastructure Engineer:** Damien Nsoh Ayine (Lead DevOps responsible for orchestration and deployment health)
