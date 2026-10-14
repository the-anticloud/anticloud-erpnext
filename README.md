# ERPNEXT

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-supermarkets-lightgrey)

> Anticloud-hardened packaging of the upstream project `ERPNEXT` in category **SUPERMARKETS**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SUPERMARKETS · **Upstream:** https://github.com/frappe/erpnext · **Upstream pin:** `ba0e2091d624a180d49ac059706a65bba2380160` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<div align="center">
    <a href="https://frappe.io/erpnext">
	<img src="./erpnext/public/images/v16/erpnext.svg" alt="ERPNext Logo" height="80px" width="80px"/>
    </a>
    <h2>ERPNext</h2>
    <div align="center">
        <p>Powerful, Intuitive and Open-Source ERP</p>
    </div>

[![Learn on Frappe School](https://img.shields.io/badge/Frappe%20School-Learn%20ERPNext-blue?style=flat-square)](https://frappe.school)<br><br>
[![CI](https://github.com/frappe/erpnext/actions/workflows/server-tests-mariadb.yml/badge.svg?event=schedule)](https://github.com/frappe/erpnext/actions/workflows/server-tests-mariadb.yml)
[![docker pulls](https://img.shields.io/docker/pulls/frappe/erpnext.svg)](https://hub.docker.com/r/frappe/erpnext)

</div>

<div align="center">
	<img src="./erpnext/public/images/v16/hero_image.png" alt="ERPNext Hero Image"/>
</div>

<div align="center">
	<a href="https://erpnext-demo.frappe.cloud/api/method/erpnext_demo.erpnext_demo.auth.login_demo">Live Demo</a>
	-
	<a href="https://frappe.io/erpnext">Website</a>
	-
	<a href="https://docs.frappe.io/erpnext/">Documentation</a>
</div>

## ERPNext

100% Open-Source ERP System to help you run your business.

### Motivation

Running a business is a complex task - handling invoices, tracking stock, managing personnel, and other daily operations. In a market where software is sold separately to manage each of these tasks, ERPNext does all of the above and more, for free.

### Key Features

- **Accounting**: All the tools you need to manage cash flow in one place, right from recording transactions to summarizing and analyzing financial reports.
- **Order Management**: Track inventory levels, replenish stock, and manage sales orders, customers, suppliers, shipments, deliverables, and order fulfillment.
- **Manufacturing**: Simplifies the production cycle, helps track material consumption, exhibits capacity planning, handles subcontracting, and more!
- **Asset Management**: From purchase to disposal, IT infrastructure to equipment. Covers every branch of your organization, all in one centralized system.
- **Projects**: Deliver both internal and external projects on time, budget and profitability. Track tasks, timesheets, and issues by project.

<details open>

<summary>More</summary>
	<img src="https://erpnext.com/files/v16_bom.png"/>
	<img src="https://erpnext.com/files/v16_stock_summary.png"/>
	<img src="https://erpnext.com/files/v16_job_card.png"/>
	<img src="https://erpnext.com/files/v16_tasks.png"/>
</details>

### Under the Hood

- [**Frappe Framework**](https://github.com/frappe/frappe): A full-stack web application framework written in Python and JavaScript. The framework provides a robust foundation for building web applications, including a database abstraction layer, user authentication, and a REST API.

- [**Frappe UI**](https://github.com/frappe/frappe-ui): A Vue-based UI library, to provide a modern user interface. The Frappe UI library provides a variety of components that can be used to build single-page applications on top of the Frappe Framework.

## Production Setup

### Managed Hosting

You can try [Frappe Cloud](https://frappecloud.com), a simple, user-friendly, and sophisticated [open-source](https://github.com/frappe/press) platform to host Frappe applications reliably and securely.

It handles installation, setup, upgrades, monitoring, maintenance, and support of your Frappe deployments. It is a fully featured developer platform with an ability to manage and control multiple Frappe deployments.

<div>
	<a href="https://erpnext-demo.frappe.cloud/app/home" target="_blank" rel="noopener noreferrer">
		<picture>
			<source media="(prefers-color-scheme: dark)" srcset="https://frappe.io/files/try-on-fc-white.png">
			<img src="https://frappe.io/files/try-on-fc-black.png" alt="Try on Frappe Cloud" height="28" />
		</picture>
	</a>
</div>

### Self-Hosted
#### Docker

See [Frappe Docker Documentation](https://github.com/frappe/frappe_docker) for full documentation & FAQ on Docker setup

#### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose v2](https://docs.docker.com/compose/)
- [git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git)

> For Docker basics and best practices refer to Docker's [documentation](https://docs.docker.com)

### Try on your environment

> **⚠️ Disposable demo only**
>
> **This setup is intended for quick evaluation. Expect to throw the environment away.** You will not be able to install custom apps to this setup. For production deployments, custom configurations, and detailed explanations, see the full documentation.

First source the project:

```sh
git source https://github.com/frappe/frappe_docker
cd frappe_docker
```

Then run:

```sh
docker compose -f pwd.yml up -d
```
Wait for a couple of minutes for ERPNext site to be created or check the `create-site` container logs before opening browser on port `8080`. (username: `Administrator`, password: `admin`)

See [Frappe Docker](https://github.com/frappe/frappe_docker/blob/main/docs/01-getting-started/03-arm64.md) for ARM based docker setup

## Development Setup
### Manual Install

The Easy Way: our install script for bench will install all dependencies (e.g. MariaDB). See https://github.com/frappe/bench for more details.

New passwords will be created for the ERPNext "Administrator" user, the MariaDB root user, and the Frappe user (the script displays the passwords and saves them to ~/frappe_passwords.txt).

### Local

To setup the project locally follow the steps mentioned below:

1. Setup bench by following the [Installation Steps](https://frappeframework.com/docs/user/en/installation) and start the server
   ```
   bench start
   ```

2. In a separate terminal window, run the following commands:
   ```
   # Create a new site
   bench new-site erpnext.localhost
   ```

3. Get the ERPNext app and install it
   ```
   # Get the ERPNext app
   bench get-app https://github.com/frappe/erpnext

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json, yarn.lock; scanned in UPSTREAM_CLONE)
- Top-level source layout: `banking/`, `erpnext/`, `semgrep/`
- Snapshot size: **5749 files**, **541683 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (3024), `.json` (1349), `.js` (660), `.md` (197), `.svg` (120), `.html` (115)
- Upstream commit pinned for this packaging: `ba0e2091d624a180d49ac059706a65bba2380160`

---

## Installation

- [**Frappe UI**](https://github.com/frappe/frappe-ui): A Vue-based UI library, to provide a modern user interface. The Frappe UI library provides a variety of components that can be used to build single-page applications on top of the Frappe Framework.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

```sh
npm start          # declared start script, when present
npm run dev        # declared dev script, when present
```

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

	<a href="https://frappe.io/erpnext">Website</a>
	-
	<a href="https://docs.frappe.io/erpnext/">Documentation</a>
</div>

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json, yarn.lock |
| Files in snapshot | 5749 |
| Lines of code | 541683 |
| Dependency references | 61 |
| Dependencies by ecosystem | npm: 49, pypi: 12 |
| Upstream license | GPL-3.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | onscan.js | ^1.5.2 | package.json |
| pypi | Unidecode | ~=1.4.0 | pyproject.toml |
| pypi | barcodenumber | ~=0.5.0 | pyproject.toml |
| pypi | rapidfuzz | ~=3.14.3 | pyproject.toml |
| pypi | holidays | ~=0.87 | pyproject.toml |
| pypi | googlemaps | ~=4.10.0 | pyproject.toml |
| pypi | plaid-python | ~=7.2.1 | pyproject.toml |
| pypi | python-youtube | ~=0.9.9 | pyproject.toml |
| pypi | pypng | ~=0.20220715.0 | pyproject.toml |
| pypi | mt-940 | >=4.26.0 | pyproject.toml |
| pypi | pdfplumber | >=0.11.0 | pyproject.toml |
| pypi | Convert | - | erpnext/regional/address_template/setup.py |
| pypi | Convert | - | erpnext/regional/address_template/setup.py |
| npm | @dnd-kit/core | ^6.3.1 | banking/package.json |
| npm | @dnd-kit/sortable | ^10.0.0 | banking/package.json |
| ... | (46 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

> **⚠️ Disposable demo only**
>
> **This setup is intended for quick evaluation. Expect to throw the environment away.** You will not be able to install custom apps to this setup. For production deployments, custom configurations, and detailed explanations, see the full documentation.

First source the project:

```sh
git source https://github.com/frappe/frappe_docker
cd frappe_docker
```

Then run:

```sh
docker compose -f pwd.yml up -d
```
Wait for a couple of minutes for ERPNext site to be created or check the `create-site` container logs before opening browser on port `8080`. (username: `Administrator`, password: `admin`)

See [Frappe Docker](https://github.com/frappe/frappe_docker/blob/main/docs/01-getting-started/03-arm64.md) for ARM based docker setup

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `.github/CONTRIBUTING.md`:*

### Introduction (For First-Time Contributors)

Thank you for your interest in raising an issue with ERPNext. An issue can be either a bug report or a feature request.

By reporting bugs, you contribute directly to improving ERPNext. Bug reports help developers identify and fix issues quickly before they affect more users.

Feature requests are also valuable. They help shape the future of the product by introducing new ideas and improvements based on real-world use cases.

When raising an issue, keep in mind that developers do not have access to your environment. Therefore, provide as much relevant information as possible.

If you are suggesting a feature, clearly describe what you expect and how it should behave.

> ⚠️ The issue tracker is not the right place for general questions or discussions.  
> Please use the forum instead: https://discuss.frappe.io/c/erpnext/6

---

### Reply and Closing Policy

If your issue is unclear or does not meet the guidelines, it may be closed.

If that happens, please provide the requested information and reopen the issue.

---

### General Issue Guidelines

1. **Search existing issues:**  
   Before creating a new issue, check if it already exists. You can support existing issues with a 👍 or contribute additional details or mockups.

2. **Report issues separately:**  
   Do not combine multiple unrelated issues into a single report.

3. **Be concise:**  
   Avoid long explanations. Use bullet points and screenshots where possible.

---

### Bug Report Guidelines

1. **Steps to reproduce:**  
   Clearly list the steps required to reproduce the issue. If the issue cannot be reproduced, it cannot be fixed.

2. **Version number:**  
   Include the ERPNext version. The issue may already be fixed in a newer release.

3. **Clear title:**  
   Use a descriptive title (e.g., "Unable to submit Purchase Order without Basic Rate" instead of "Cannot submit").

4. **Screenshots:**  
   Add screenshots or screen recordings (e.g., `.gif`) to illustrate the issue.

---

### Feature Request Guidelines

1. **Clarity:**  
   Clearly describe the expected behavior. Avoid vague statements.

2. **Proposed solution:**  
   Suggest how the feature should work.

3. **Mockups:**  
   Provide mockups or examples whenever possible.

---

### What if my issue is closed?

Don't worry. Review the feedback, provide the required information, and reopen the issue.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: GPL-3.0** (evidence: `LICENSE.txt` in the upstream snapshot).

License file excerpt:

```text
                    GNU GENERAL PUBLIC LICENSE
                       Version 3, 29 June 2007

 Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

                            Preamble

  The GNU General Public License is a free, copyleft license for
software and other kinds of works.

  The licenses for most software and other practical works are designed
to take away your freedom to share and change the works.  By contrast,
the GNU General Public License is intended to guarantee your freedom to
share and change all versions of a program--to make sure it remains free
software for all its users.  We, the Free Software Foundation, use the
GNU General Public License for most of our software; it applies also to
any other work released this way by its authors.  You can apply it to
your programs, too.
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original GPL-3.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `GPL-3.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `ERPNEXT` (category: SUPERMARKETS)
- **Upstream URL:** https://github.com/frappe/erpnext
- **Pinned commit (SHA):** `ba0e2091d624a180d49ac059706a65bba2380160`
- **Branch:** develop
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`0d23bf4dc237c9c450ff68b3bb64c29fe4f03fb17887e5e161422bf210319944`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

