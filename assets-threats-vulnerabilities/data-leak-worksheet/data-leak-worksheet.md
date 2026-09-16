# Data Leak Worksheet

## Incident Summary

A sales manager shared access to a folder of internal-only documents with their team during a meeting. The folder contained files associated with a new product that had not yet been publicly announced, along with customer analytics and promotional materials. After the meeting, the manager did not revoke access to the internal folder, but warned the team to wait for approval before sharing the promotional materials with others.

During a video call with a business partner, a member of the sales team forgot the manager's warning. The sales representative intended to share a link to the promotional materials so the business partner could circulate them to their customers. Instead, the representative accidentally shared a link to the internal folder. The business partner then posted the link on their company's social media page, assuming it was the promotional materials.

## Control Analysis

| Field | Details |
|---|---|
| **Control** | Least privilege |
| **Issue(s)** | Lack of training leads to an increase in human error; the incident shows that the whole team hadn't been applying the least privilege principle. |
| **Review** | NIST SP 800-53: AC-6 addresses the principle of least privilege — allowing only the access necessary to achieve a goal for the organization. |
| **Recommendation(s)** | Two control enhancements that might have prevented the data leak: reviewing user privileges and reviewing privileged accounts. |
| **Justification** | Training and implementation of least privilege is necessary for all members of the organization. If this principle had been implemented, the manager would have removed the internal folder access for employees right after the meeting. |

## Security Plan Snapshot

The NIST Cybersecurity Framework (CSF) uses a hierarchical, tree-like structure to organize information. From left to right, it describes a broad security function, then becomes more specific as it branches into a category, subcategory, and individual security controls.

| Function | Category | Subcategory | Reference(s) |
|---|---|---|---|
| Protect | PR.DS: Data Security | PR.DS-5: Protections against data leaks | NIST SP 800-53: AC-6 |

In this example, the controls used to protect against data leaks are defined in NIST SP 800-53 — a set of guidelines for securing the privacy of information systems.

### NIST SP 800-53: AC-6 — Least Privilege

NIST developed SP 800-53 to give businesses a customizable information privacy plan. It's a comprehensive resource describing a wide range of control categories. Each control provides:

- **Control** — a definition of the security control
- **Discussion** — a description of how the control should be implemented
- **Control enhancements** — a list of suggestions to improve the effectiveness of the control

**AC-6 (Least Privilege):**
- **Control:** only the minimal access and authorization required to complete a task or function should be provided to users.
- **Discussion:** processes, user accounts, and roles should be enforced as necessary to achieve least privilege. The intention is to prevent a user from operating at privilege levels higher than what is necessary to accomplish business objectives.
- **Control enhancements:**
  - Restrict access to sensitive resources based on user role
  - Automatically revoke access to information after a period of time
  - Keep activity logs of provisioned user accounts
  - Regularly audit user privileges

*Note: in the access controls category, SP 800-53 lists least privilege sixth, i.e. AC-6.*
