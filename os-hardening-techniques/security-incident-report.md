# Security Incident Report: OS Hardening (Brute Force Attack)

## Section 1: Identify the network protocol involved in the incident

The records of the incident show that DNS and HTTP protocols were involved.

## Section 2: Document the incident

A brute force attack was carried out against the website "yummyrecipesforme.com" and succeeded. The attacker then injected JavaScript into the site's source code, which prompted users to download a "free recipe" file — but this redirected them to a fake website named "greatrecipesforme.com."

## Section 3: Recommend one remediation for brute force attacks

Reducing the attack surface is the best option to help mitigate this risk. MFA (or 2FA) is the best defense against brute force attacks. Other measures — strong password policies, firewall configuration, and source code audits — should also be part of a strong security posture.
