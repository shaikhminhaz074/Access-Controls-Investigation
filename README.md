# Access Control Incident Investigation

## Overview
This project documents a hands-on cybersecurity activity: investigating an unauthorized payroll
deposit incident by analyzing an event log, cross-referencing it against an employee directory,
identifying access control failures, and recommending mitigations.

## Scenario
A deposit was made from the business to an unknown bank account. The finance manager confirmed
they did not authorize it, though the payment was stopped in time. As the first cybersecurity
hire at the company, the task was to trace what happened and recommend controls to prevent a
repeat incident.

## Methodology
1. **Reviewed the event log** for the incident (Event ID 1227) to capture the who/when/where of
   the suspicious payroll change.
2. **Cross-referenced the log details** (user account, device, IP address) against the employee
   directory to spot mismatches.
3. **Identified access control issues** — gaps in authentication and authorization that allowed
   the incident to occur.
4. **Recommended mitigations** covering technical, operational, and managerial controls.

## Key Finding
The payroll change was made using a **`Legal\Administrator`** account — from the Legal
department, not Finance — from a device (`Up2-NoGud`) not tied to any known employee, adding a
transaction to an unrecognized bank record (`FAUX_BANK`). This points to excessive account
privileges and/or a compromised or improperly retained credential, compounded by a lack of
role-based permissions on the company's shared cloud drive.

## Deliverables
- Completed worksheet with notes, issues, and recommendations for the Authorization/Authentication access control
  category.

## Skills Demonstrated
- Event log analysis
- Cross-referencing data sources to profile a threat actor
- Identifying authentication/authorization weaknesses
- Recommending least-privilege, MFA, and access-review controls
