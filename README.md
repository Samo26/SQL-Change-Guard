# SQL Change Guard

SQL Change Guard is a secure and auditable SQL change management solution designed for enterprise environments that demand compliance, traceability, and control. Built with WPF and SQL Server technologies, it enables organizations to analyze, validate, approve, and execute SQL scripts with full transparency and minimum risk.

## Overview

Designed for industries like banking, finance, and insurance, SQL Change Guard ensures all SQL scripts go through a strict review and validation process before being executed in production. It supports COBIT, ITIL, and internal audit standards, helping organizations meet regulatory requirements such as SOX and GDPR.

## Key Features

- Pre-deployment validation of SQL scripts
- Detection of risky commands (e.g., DELETE/UPDATE without WHERE)
- COBIT/ITIL-compliant change approval process
- Script lifecycle management: Pending, Executed, Rejected
- Audit log generation and secure execution records
- WPF-based UI for dashboard and change tracking
- Supports transactional execution with GO-splitting
- Sandbox environment support before production deployment
- Secure dual-connection handling (sandbox and production)

## Use Cases

- A bank needs to audit every SQL deployment for regulatory reporting.
- A fintech startup wants to prevent accidental data loss through unmanaged scripts.
- A corporate IT department needs to enforce CAB-approved change controls.
  
## Architecture Overview

SQL Change Guard is designed as a modular WPF application with a layered architecture:

- **Presentation Layer:** WPF dashboard for script management and execution monitoring.
- **Business Logic Layer:** Core validation engine handling script parsing, risk analysis, and policy enforcement.
- **Data Access Layer:** Responsible for interactions with sandbox and production SQL Server instances.
- **Audit & Logging Module:** Maintains full audit trails and execution logs in a dedicated database.
- **Integration Layer:** (Planned) API endpoints for CI/CD pipeline integration and automated approvals.

This modular design allows easy maintenance, testing, and future scalability.

## Sample Input and Output

**Input SQL Script:**
```sql
DELETE FROM Customers
Analysis Output:

Warning: DELETE without WHERE clause detected.

Action: Script blocked until reviewed and approved.

Installation & Requirements
Windows OS with .NET Framework 4.7.2 or higher

Microsoft SQL Server (2016 or higher recommended)

Visual Studio (optional, for developers)

Two database connections: sandbox and production

Usage
Import a SQL script into the SQL Change Guard interface.

The script is automatically analyzed for risky or non-compliant statements.

A visual report of findings is presented to the reviewer.

The reviewer can approve, reject, or request modifications.

Once approved, the script is executed securely with audit trail creation.

All activity is logged in the request database and is audit-ready.

FAQ
Q: Is this tool open source?
A: No, this repository is for demonstration and documentation purposes. Contact us for licensing options.

Q: Does it support databases other than SQL Server?
A: Currently only Microsoft SQL Server is supported. Other engines are under evaluation.

Q: Can it integrate with DevOps or CI/CD tools?
A: CLI and API integrations are planned for future releases.

Q: Can we run it in a non-banking context?
A: Absolutely. Any organization needing safe and auditable SQL deployments can benefit.

Compliance
SQL Change Guard is designed in accordance with the following frameworks:

COBIT (Control Objectives for Information and Related Technologies)

ITIL (Information Technology Infrastructure Library)

GDPR (General Data Protection Regulation)

SOX (Sarbanes–Oxley Act)

License
This repository is intended for demonstration and evaluation purposes only.
All rights reserved to the author. For enterprise licensing, please contact us directly.

Contact
Website: https://sqlchangeguard.com

LinkedIn: https://linkedin.com/company/sqlchangeguard

Email: info@sqlchangeguard.com
