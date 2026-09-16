# Botium Toys: Scope, Goals, and Risk Assessment Report

## Scope and Goals of the Audit

**Scope:** the entire security program at Botium Toys. This means all assets need to be assessed alongside the internal processes and procedures related to the implementation of controls and compliance best practices.

**Goals:** assess existing assets and complete the controls and compliance checklist to determine which controls and compliance best practices need to be implemented to improve Botium Toys' security posture.

## Current Assets

Assets managed by the IT department include:
- On-premises equipment for in-office business needs
- Employee equipment: end-user devices (desktops/laptops, smartphones), remote workstations, headsets, cables, keyboards, mice, docking stations, surveillance cameras, etc.
- Storefront products available for retail sale on-site and online, stored in the company's adjoining warehouse
- Management of systems, software, and services: accounting, telecommunication, database, security, e-commerce, and inventory management
- Internet access
- Internal network
- Data retention and storage
- Legacy system maintenance: end-of-life systems that require human monitoring

## Risk Assessment

**Risk description:** currently, there is inadequate management of assets. Additionally, Botium Toys does not have all the proper controls in place and may not be fully compliant with U.S. and international regulations and standards.

**Control best practices:** the first of the five NIST CSF functions is Identify. Botium Toys will need to dedicate resources to identify assets so they can be appropriately managed. They will also need to classify existing assets and determine the impact of losing existing assets, including systems, on business continuity.

**Risk score:** on a scale of 1 to 10, the risk score is **8** — fairly high, due to a lack of controls and adherence to compliance best practices.

## Additional Comments

The potential impact from the loss of an asset is rated medium, because the IT department doesn't know which assets would be at risk. The risk of asset loss or fines from governing bodies is high, because Botium Toys does not have all the necessary controls in place and is not fully adhering to compliance best practices that keep critical data private and secure. Specific findings:

- Currently, all Botium Toys employees have access to internally stored data and may be able to access cardholder data and customers' PII/SPII.
- Encryption is not currently used to ensure confidentiality of customers' credit card information, which is accepted, processed, transmitted, and stored locally in the company's internal database.
- Access controls pertaining to least privilege and separation of duties have not been implemented.
- The IT department has ensured availability and integrated controls to ensure data integrity.
- The IT department has a firewall that blocks traffic based on an appropriately defined set of security rules.
- Antivirus software is installed and monitored regularly by the IT department.
- The IT department has not installed an intrusion detection system (IDS).
- There are no disaster recovery plans currently in place, and the company does not have backups of critical data.
- The IT department has established a plan to notify E.U. customers within 72 hours if there is a security breach. Privacy policies, procedures, and processes have been developed and are enforced among IT department members and other employees to properly document and maintain data.
- Although a password policy exists, its requirements are minimal and not in line with current minimum password complexity requirements (e.g. at least eight characters, a combination of letters and at least one number, special characters).
- There is no centralized password management system that enforces the password policy's minimum requirements, which sometimes affects productivity when employees/vendors submit a ticket to the IT department to recover or reset a password.
- While legacy systems are monitored and maintained, there is no regular schedule in place for these tasks, and intervention methods are unclear.
- The store's physical location — Botium Toys' main offices, storefront, and warehouse of products — has sufficient locks, up-to-date CCTV surveillance, and functioning fire detection/prevention systems.

*(See `controls-and-compliance-checklist.md` for the corresponding assessment checklist.)*
