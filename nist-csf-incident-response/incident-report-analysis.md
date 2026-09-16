# Incident Report Analysis: DDoS Attack (NIST CSF)

## Summary

Our organization recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved. Network services stopped due to an incoming flood of ICMP packets. On investigation, it was found that a malicious actor took advantage of an unconfigured firewall and flooded the company's network with ICMP pings. To address this lack of firewall configuration, a new firewall rule was implemented to limit the rate of incoming ICMP packets, and source IP address verification was also implemented on the firewall so an attacker can't spoof an incoming ICMP packet's IP address.

## Identify

The flooded ICMP traffic from different IP addresses led to a DDoS attack, with symptoms including network services going down. It was found that this happened because there was no firewall rule to limit the rate of incoming ICMP packets, and the attacker took advantage of this gap.

## Protect

New firewall rules were implemented — for example, if any device sends repeated messages, its IP is blocked, and if the same type of packet (like ICMP) keeps arriving, the firewall blocks it. An IDS/IPS system was also added to filter out ICMP traffic based on suspicious characteristics.

## Detect

Key measures to take:
- **Security continuous monitoring** — using SIEM tools to monitor all logs so anomalies can be detected
- **Detection process** — tools like IDS/IPS should be used
- **Firewall** — only authorized and authenticated traffic should be allowed access

## Respond

Responding to an attack should follow a playbook. First, top-priority assets should be secured and maintained. All security measures should be audited. A plan should be created to help prevent this type of attack in the future.

## Recover

Ensure all resources are restored and all services are back up. Anything infected should be inspected and kept separate, since it may still contain malware left by the attacker. Recovery of all services should be confirmed, since the organization's availability is important so clients can regain access.
