# Cybersecurity Incident Report: Network Traffic Analysis (DNS/ICMP)

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log

The UDP protocol reveals that the DNS server is unreachable. This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message "udp port 53 unreachable." The port noted in the error message is used for DNS. The most likely issue is with the DNS server. It is possible that this is an indication of a malicious attack on the DNS server.

## Part 2: Explain your analysis of the data and provide at least one cause of the incident

The incident occurred around noon, when several customers of the client reported that they were unable to access the client company's website, www.yummyrecipesforme.com, and saw the error "destination port unreachable" after waiting for the page to load. The network analyzer team responded and began running tests with the network protocol analyzer tool tcpdump. The resulting logs revealed that port 53, used for DNS traffic, was unreachable.

We are continuing to investigate the root cause of the issue to determine how we can restore access to the DNS. Our next steps include checking the firewall configuration to see if port 53 is blocked, and contacting the system administrator for the DNS server to have them check the system for signs of an attack. The team believes it is possible that an attacker with malicious intent made the website unreachable by tampering with the DNS server.

---
*Awais Ahmed's own completed work.*
