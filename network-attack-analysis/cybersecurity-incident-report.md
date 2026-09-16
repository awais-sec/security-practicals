# Cybersecurity Incident Report: SYN Flood Attack

## Section 1: Identify the type of attack that may have caused this network interruption

One potential explanation for the website's connection timeout error is that users aren't able to connect because the web server is down for some reason. The logs show that this started at log entry no. 52, when the attacker first sent SYN packets to the web server. This event could be a SYN flood attack.

## Section 2: Explain how the attack is causing the website to malfunction

When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. The three steps of the handshake are:

1. The user sends a SYN to the web server on port 443 (HTTPS).
2. The web server checks whether the IP is authorized and sends a SYN-ACK packet back to the user.
3. The user sends a packet with ACK to the web server, and the handshake is acknowledged.

But when a malicious attacker sends a large number of SYN packets at once, the web server can become overwhelmed, which leads to a downed network. The logs indicate that a malicious IP, 203.0.113.0, started sending SYN packets to the web server, which can be seen at log entry 52 of the Wireshark TCP/HTTP log.

---
*Awais Ahmed's own completed work.*
