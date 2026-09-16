# Resource: How to Read the tcpdump Traffic Log

This reading explains how to identify the brute force attack described in the OS Hardening exercise using tcpdump.

The first section of the DNS & HTTP traffic log file shows the source computer (`your.machine.52444`) using port 52444 to send a DNS resolution request to the DNS server (`dns.google.domain`) for the destination URL (`yummyrecipesforme.com`). The reply comes back from the DNS server to the source computer with the IP address of the destination URL (`203.0.113.22`).

The next section shows the source computer sending a connection request (Flags `[S]`) from the source computer (`your.machine.36086`) using port 36086 directly to the destination (`yummyrecipesforme.com.http`). The `.http` suffix is the port number; HTTP is commonly associated with port 80. The reply shows the destination acknowledging it received the connection request (Flags `[S.]`). The communication between the source and the intended destination continues for about 2 minutes, based on the timestamps between this block (14:18) and the next DNS resolution request (14:20).

**TCP flag codes include:**

| Flag | Meaning |
|---|---|
| `[S]` | Connection Start |
| `[F]` | Connection Finish |
| `[P]` | Data Push |
| `[R]` | Connection Reset |
| `[.]` | Acknowledgment |

The log entry `HTTP: GET / HTTP/1.1` shows the browser requesting data from `yummyrecipesforme.com` using the HTTP GET method over HTTP/1.1 — this could be the download request for the malicious file.

Then a sudden change happens in the logs. Traffic is routed from the source computer to the DNS server again using port `.52444` to make another DNS resolution request. This time, the DNS server routes traffic to a new IP address (`192.0.2.172`) and its associated URL (`greatrecipesforme.com.http`). Traffic changes to a route between the source computer and the spoofed website (outgoing: `your.machine.56378 > greatrecipesforme.com.http`; incoming: `greatrecipesforme.com.http > your.machine.56378`). Note that the port number on the source computer (`.56378`) has changed again after being redirected to the new website.

## Further Reading Referenced in This Resource

- An introduction to using tcpdump at the Linux command line
- tcpdump Cheat Sheet
- What is a computer port? | Ports in networking
- Service Name and Transport Protocol Port Number Registry
- How to Capture and Analyze Network Traffic with tcpdump?
- Masterclass – Tcpdump – Interpreting Output

---
*Source: provided course reading material for the OS Hardening exercise, not Awais's own work.*
