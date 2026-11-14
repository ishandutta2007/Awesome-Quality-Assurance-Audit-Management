# Awesome-Quality-Assurance-Audit-Management

# Awesome Quality Assurance & Audit Management

> A curated list of top Quality Assurance and Audit Management platforms — both SaaS/Hosted commercial QMS solutions and open-source alternatives for managing nonconformities, CAPA, audits, and compliance evidence.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [MasterControl](#mastercontrol)
  - [Veeva Vault QMS](#veeva-vault-qms)
  - [TrackWise](#trackwise)
  - [Qualio](#qualio)
  - [ETQ Reliance](#etq-reliance)
  - [ComplianceQuest](#compliancequest)
- [Open-Source Software](#-open-source-software)
  - [DearAuditor QMS Baseline](#dearauditor-qms-baseline)
  - [AuditSym](#auditsym)
  - [Dolibarr CAPA & Deviation Manager](#dolibarr-capa--deviation-manager)
  - [Autonomous EHS Management](#autonomous-ehs-management)
  - [Odoo Management System (OCA)](#odoo-management-system-oca)
  - [grc-lake](#grc-lake)
  - [pHKapa](#phkapa)
  - [OpenWatch](#openwatch)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Quality Assurance and Audit Management platforms. These are not open-source but are included as reference points for feature comparison.

### MasterControl
**Type:** Enterprise QMS with document control and audit management
MasterControl is a long-standing enterprise QMS platform covering document control, training, CAPA, nonconformances, audits, and supplier management. It is widely deployed in medical device, pharmaceutical, and life sciences organizations requiring FDA 21 CFR Part 11 compliance and rigorous audit trails.

### Veeva Vault QMS
**Type:** Life sciences QMS within Veeva Vault
Veeva Vault QMS provides quality management for life sciences, covering deviations, CAPA, change control, audits, and supplier quality. It is tightly integrated with Veeva's regulatory and clinical platforms, making it the natural choice for organizations already standardized on Veeva.

### TrackWise
**Type:** Enterprise QMS with CAPA and audit focus
TrackWise (Honeywell) is a mature enterprise QMS known for its strength in CAPA management, audit management, and regulatory compliance. It is often deployed in pharmaceutical and medical device organizations with complex quality workflows.

### Qualio
**Type:** Cloud QMS for life sciences
Qualio is a modern cloud QMS designed for life sciences startups and scale-ups, covering document control, training, CAPA, nonconformances, and audits. It emphasizes ease of use and rapid deployment compared to legacy enterprise QMS platforms.

### ETQ Reliance
**Type:** Enterprise QMS and EHS management
ETQ Reliance provides QMS, EHS, and compliance management in a unified platform, covering document control, CAPA, audits, nonconformances, and risk management. Suited for mid-market to enterprise organizations across manufacturing and life sciences.

### ComplianceQuest
**Type:** Cloud QMS on Salesforce platform
ComplianceQuest provides QMS and EHS capabilities built natively on Salesforce, covering document control, CAPA, audits, supplier quality, and training. It is the natural choice for organizations already invested in the Salesforce ecosystem.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Quality Assurance and Audit Management tools. The open-source ecosystem spans **GitHub-native eQMS baselines**, **offline-first audit platforms**, **ERP-integrated CAPA modules**, and **compliance evidence engines**.

### DearAuditor QMS Baseline
**Stack:** GitHub (Issues/PRs/Actions/Releases) | **License:** Open Source
DearAuditor QMS Baseline is an open-source, **GitHub-native eQMS baseline** for medical device and regulated software teams, using Issues, PRs, Actions, and Releases as the quality system of record [citation:1]. It covers **ISO 9001, ISO 13485, ISO 14971, IEC 62304, IEC 62366-1, ISO/IEC 27001, ISO/IEC 42001, GDPR/nFADP**, plus an optional **GAMP 5 / 21 CFR Part 11** overlay [citation:1]. The baseline ships with **1 published Quality Manual, 23 published SOPs, and 2 published WIs**, including SOP-002 CAPA, SOP-003 Internal Audit, and SOP-004 Management Review [citation:1]. Training and role navigation are managed through GitHub issues, with a training matrix mapping GitHub users to roles [citation:1]. **Important:** This is a controlled content baseline and workflow automation framework, not a hosted application—adoption requires configuring your own GitHub repository as the system of record [citation:1].
**Best for:** Medical device and regulated software teams already using GitHub who want a standards-mapped eQMS foundation without a separate platform vendor, accepting the GitHub-native workflow model.

### AuditSym
**Stack:** HTML/JavaScript / LocalStorage / AI providers | **License:** Open Source
AuditSym is an **offline-first GRC platform with integrated AI** for audits against **NIST CSF 2.0, ISO 27001, CIS Controls v8, and COBIT 2019** [citation:2]. Key features include:
- **Multi-framework audit engine** with risk-weighted scoring and AI-generated executive narrative
- **Remediation Hub** with a priority matrix (Quick Wins, Critical, Opportunities, Strategic) and full finding lifecycle (Open → Assigned → In Progress → Pending Validation → Closed) [citation:2]
- **Risk Acceptance workflow** with formal approval, justification, and review date (ISO 27001/SOX compliant) [citation:2]
- **Local RAG** for semantic search of PDF policies, with 5 AI providers including local Ollama and a deterministic fallback for offline use [citation:2]
- **Professional PDF audit reports** with executive summary and evidence annex [citation:2]

Runs entirely in the browser with LocalStorage persistence, requiring no backend server [citation:2].
**Best for:** Internal audit and GRC teams wanting a portable, offline-capable audit platform with AI assistance and professional reporting, accepting browser-based storage rather than a server database.

### Dolibarr CAPA & Deviation Manager
**Stack:** PHP / Dolibarr / MySQL | **License:** Open Source (module)
CAPA & Deviation Manager is a Dolibarr module for managing quality deviations, investigations, root cause analysis, corrective and preventive actions, effectiveness checks, and audit trails [citation:3]. The workflow follows **Open → Investigation → CAPA → Effectiveness → Closed**, with **5 Why root cause analysis** built in [citation:3]. Key features include severity management (Minor/Major/Critical), automatic reference numbering, file attachments with audit trail, and professional PDF reports [citation:3]. It integrates with **LabQC Pro** (FAIL/OOS QC tests can generate CAPA deviations) and **Calibration & Equipment Pro** (failed calibrations can generate deviations) [citation:3]. A deviation cannot be closed until the effectiveness check is completed and an effectiveness status is selected [citation:3].
**Best for:** Laboratories, pharmaceutical environments, and manufacturing quality departments already using Dolibarr wanting a structured CAPA and deviation workflow with audit trails, accepting the Dolibarr ERP dependency.

### Autonomous EHS Management
**Stack:** Node.js / PostgreSQL / Docker | **License:** Apache 2.0
Autonomous EHS Management is a self-hosted **environmental, health and safety (EHS) console** for incident management, **corrective and preventive actions (CAPA)**, and **TRIR reporting**, with PostgreSQL as the system of record [citation:7]. The core workflow links incident records to corrective actions and human verification—a person closes the record, with optional AI suggesting wording but never auto-deciding [citation:7]. TRIR calculation uses `(recordable count × 200,000) / hours worked`, requiring a complete 12-month hours grid or an annual total to compute [citation:7]. The project explicitly states it does not claim OSHA certification and is not an official filing tool [citation:7].
**Best for:** Organizations needing self-hosted EHS incident and CAPA management with TRIR reporting, accepting that it is EHS-focused rather than a full QMS.

### Odoo Management System (OCA)
**Stack:** Python / Odoo / PostgreSQL | **License:** AGPL-3.0 (OCA)
The Odoo Community Association's Management System modules provide **nonconformity management** for quality (ISO 9001), environment (ISO 14001), information security (ISO 27001), health and safety (ISO 45001), and IT services (ISO 20000) [citation:10]. The nonconformity workflow covers creation, analysis (root causes, severity), action plan (immediate, corrective, preventive actions), and effectiveness evaluation before closure . Actions have deadlines, responsible persons, and types, with email notifications sent when actions are created . **Important:** This is an Odoo module, not a standalone platform—it requires an existing Odoo deployment .
**Best for:** Organizations already using Odoo wanting integrated nonconformity and CAPA management within their existing ERP, accepting the Odoo ecosystem dependency.

### grc-lake
**Stack:** Python / Docker / Helm | **License:** Open Source
grc-lake is an open-source, self-hosted **GRC evidence engine** that turns security evidence into traceable control assessments and reviewable audit workpapers [citation:11]. It reads evidence from existing systems, evaluates versioned rules, and preserves the evidence and review decisions behind each result. Features include **framework coverage tracking** (assessed vs. mapped vs. reviewed requirements), **evidence freshness** monitoring, **control worklists** with result filtering, and **snapshots with hash-chained ledgers** for audit integrity [citation:11]. It exposes the same evidence model via Console, REST API, CLI, and **MCP** for AI agent access [citation:11]. Deploys via Docker or Helm.
**Best for:** Security and compliance teams wanting an open-source evidence and audit workpaper engine that integrates with existing security data lakes, accepting the infrastructure requirements of a self-hosted server.

### pHKapa
**Stack:** PHP / CakePHP / MySQL | **License:** MIT
pHKapa is a nonconformity management software for quality assurance that generates **action plan (CAPA) requests** routed through register, review, plan/implement, and verification stages [citation:12]. It provides mechanisms to determine the source and cost of problems [citation:12]. **Important limitation:** The package requires PHP `>=5.6 && <8.0.0`, which is a legacy runtime constraint that may be incompatible with modern hosting environments [citation:12].
**Best for:** Small quality teams wanting a lightweight, MIT-licensed CAPA tool, accepting the legacy PHP version requirement and the need to verify maintenance status.

### OpenWatch
**Stack:** Go / PostgreSQL / React | **License:** GPL (Community) / Commercial (Pro)
OpenWatch is a **compliance and audit platform** for Linux fleets covering **STIG, CIS, NIST 800-53, PCI-DSS, and FedRAMP** simultaneously in one scan [citation:6]. Key audit-focused features include:
- **Temporal compliance queries** answering "were these hosts compliant on a specific date" backed by stored snapshots [citation:6]
- **Compliance drift detection** with automatic alerts when a passing rule starts failing [citation:6]
- **Exception workflows** (request, approve, reject, time-limit, revoke) with full audit trail [citation:6]
- **Audit-ready evidence exports** in CSV, JSON, and PDF, capturing exact commands, raw output, expected value, and actual value [citation:6]

Deploys in 10 minutes on Linux with PostgreSQL and 4 GB RAM, no containers required [citation:6].
**Best for:** Linux-centric organizations needing continuous compliance monitoring with audit-grade evidence and exception governance, accepting a Linux-specific scope.

---

## 📊 Comparison at a Glance

| Software | License | Stack | CAPA | Audit Management | Evidence/Audit Trail | Self-Hosted | Best For |
|----------|---------|-------|------|-------------------|----------------------|-------------|----------|
| **MasterControl** | Proprietary | Cloud | ✅ | ✅ | ✅ | ❌ | Enterprise life sciences QMS |
| **Veeva Vault QMS** | Proprietary | Cloud | ✅ | ✅ | ✅ | ❌ | Veeva ecosystem QMS |
| **Qualio** | Proprietary | Cloud | ✅ | ✅ | ✅ | ❌ | Life sciences startups |
| **DearAuditor** | Open Source | GitHub | ✅ SOP-002 | ✅ SOP-003 | ✅ Releases | ✅ (GitHub) | GitHub-native eQMS baseline |
| **AuditSym** | Open Source | Browser | (Remediation) | ✅ Multi-framework | ✅ PDF + LocalStorage | ✅ (Browser) | Offline audit + AI |
| **Dolibarr CAPA** | Open Source | PHP/Dolibarr | ✅ Deep | (Audit trail) | ✅ | ✅ | Lab/manufacturing CAPA |
| **Autonomous EHS** | Apache 2.0 | Node.js/Postgres | ✅ | (Incident) | ✅ PostgreSQL | ✅ | EHS incident + CAPA |
| **Odoo Mgmt System** | AGPL-3.0 | Python/Odoo | ✅ | (NC workflow) | ✅ | ✅ | Odoo nonconformity |
| **grc-lake** | Open Source | Python/Docker | ❌ | ✅ Workpapers | ✅ Hash-chained | ✅ | Evidence + audit workpapers |
| **pHKapa** | MIT | PHP/MySQL | ✅ | (Verification) | (Check) | ✅ | Lightweight CAPA (legacy PHP) |
| **OpenWatch** | GPL/Commercial | Go/Postgres | ❌ | ✅ Drift + exceptions | ✅ CSV/JSON/PDF | ✅ | Linux compliance evidence |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Quality Assurance or Audit Management tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits** between **eQMS baselines for regulated teams** (DearAuditor, mapped to ISO 9001/13485/14971/62304), **audit and evidence platforms** (AuditSym for multi-framework audits, grc-lake for evidence workpapers, OpenWatch for Linux compliance), and **ERP-integrated CAPA modules** (Dolibarr, Odoo, Autonomous EHS). **DearAuditor** is the most comprehensive open-source eQMS baseline for medical device teams, shipping 23 SOPs with standards mapping [citation:1]. **AuditSym** is the strongest choice for internal audit teams wanting a portable, AI-assisted multi-framework platform [citation:2]. For CAPA specifically, **Dolibarr CAPA & Deviation Manager** offers the deepest structured workflow with 5 Why analysis and effectiveness checks [citation:3].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
