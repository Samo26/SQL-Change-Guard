# SQL Change Guard

SQL Change Guard is a secure and compliant SQL change management solution designed for enterprise environments where auditability, validation, and control are essential. Built with WPF and SQL Server technologies, it enables organizations to analyze, validate, approve, and execute SQL scripts with full transparency and minimal risk.

## Overview

SQL Change Guard prevents unauthorized or risky SQL deployments by enforcing structured change validation workflows. It helps institutions meet internal policies, COBIT and ITIL compliance, and external regulatory requirements such as SOX and GDPR.

## Key Features

- Pre-deployment validation of SQL scripts
- Detection of unsafe patterns (e.g. DELETE/UPDATE without WHERE)
- Script lifecycle: Pending, Executed, Rejected, Re-tested
- Approval-based execution flow (CAB or change management integration)
- Audit logs for each change and operator
- WPF-based secure deployment interface
- Supports GO-based batch splitting in single transactions
- Automatic rollback if any batch fails
- Sandbox testing environment support

## Installation & Requirements

- Windows OS with .NET Framework 4.7.2 or higher
- SQL Server 2016 or higher
- Visual Studio (for development usage)
- Two separate SQL Server connections (sandbox & production)

## Usage

1. Prepare your SQL script as a `.sql` file.
2. Import the script into SQL Change Guard interface.
3. The system analyzes the script and shows:
   - Command types
   - Risky statements (if any)
   - Estimated impact scope
4. Review and validate the script.
5. Submit for approval if necessary (CAB/ITIL process).
6. Execute script securely across environments.
7. All execution logs and decisions are stored and can be audited.

## Compliance

SQL Change Guard aligns with the following frameworks:

- COBIT (Control Objectives for Information and Related Technologies)
- ITIL (Information Technology Infrastructure Library)
- GDPR (General Data Protection Regulation)
- SOX (Sarbanes–Oxley Act)

## Contact

- Website: https://sqlchangeguard.com  
- LinkedIn: https://linkedin.com/company/sqlchangeguard  
- Email: info@sqlchangeguard.com  

---
