# Resource: Control Categories

Reading material provided alongside the Security Audit exercise (context for `controls-and-compliance-checklist.md`).

## Control Categories

Controls within cybersecurity are grouped into three main categories:

- **Administrative/Managerial controls** — address the human component of cybersecurity: policies and procedures that define how an organization manages data and employee responsibilities, including their role in protecting the organization. While typically policy-based, enforcing these policies may require technical or physical controls.
- **Technical controls** — solutions such as firewalls, IDS, IPS, antivirus, and encryption, used in various ways to meet organizational goals.
- **Physical/Operational controls** — door locks, cabinet locks, surveillance cameras, badge readers, etc., used to limit physical access to assets by unauthorized personnel.

## Control Types

Control types include (but aren't limited to):

1. **Preventative** — designed to prevent an incident from occurring in the first place
2. **Corrective** — used to restore an asset after an incident
3. **Detective** — implemented to determine whether an incident has occurred or is in progress
4. **Deterrent** — designed to discourage attacks

These work together to provide defense in depth.

### Administrative/Managerial Controls

| Control Name | Control Type | Control Purpose |
|---|---|---|
| Least Privilege | Preventative | Reduce risk and overall impact of a malicious insider or compromised account |
| Disaster recovery plans | Corrective | Provide business continuity |
| Password policies | Preventative | Reduce likelihood of account compromise via brute force or dictionary attack |
| Access control policies | Preventative | Bolster confidentiality and integrity by defining which groups can access or modify data |
| Account management policies | Preventative | Manage account lifecycle, reduce attack surface, limit impact from disgruntled former employees and default account usage |
| Separation of duties | Preventative | Reduce risk and overall impact of a malicious insider or compromised account |

### Technical Controls

| Control Name | Control Type | Control Purpose |
|---|---|---|
| Firewall | Preventative | Filter unwanted or malicious traffic from entering the network |
| IDS/IPS | Detective | Detect and prevent anomalous traffic that matches a signature or rule |
| Encryption | Deterrent | Provide confidentiality for sensitive information |
| Backups | Corrective | Restore/recover from an event |
| Password management | Preventative | Reduce password fatigue |
| Antivirus (AV) software | Corrective | Detect and quarantine known threats |
| Manual monitoring, maintenance, and intervention | Preventative | Identify and manage threats, risks, or vulnerabilities in out-of-date systems |

### Physical/Operational Controls

| Control Name | Control Type | Control Purpose |
|---|---|---|
| Time-controlled safe | Deterrent | Reduce attack surface and overall impact from physical threats |
| Adequate lighting | Deterrent | Deter threats by limiting "hiding" places |
| Closed-circuit television (CCTV) | Preventative/Detective | Reduces risk of certain events occurring, and can be used after an event to inform on event conditions |
| Locking cabinets (for network gear) | Preventative | Bolster integrity by preventing unauthorized access to or modification of network infrastructure |
| Signage indicating alarm service provider | Deterrent | Deter certain threats by making a successful attack seem unlikely |
| Locks | Deterrent/Preventative | Bolster integrity by deterring/preventing unauthorized physical access to assets |
| Fire detection and prevention (fire alarm, sprinkler system, etc.) | Detective/Preventative | Detect fire and prevent damage to physical assets such as inventory, servers, etc. |
