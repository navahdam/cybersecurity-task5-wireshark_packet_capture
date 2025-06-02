
# 🧪 Network Traffic Analysis with Wireshark

## 📁 Task 5: Capture and Analyze Network Traffic

This task involved capturing live network traffic using Wireshark and identifying key network protocols. The objective was to develop hands-on skills in packet capture, protocol filtering, and traffic analysis.

---

## 🎯 Objective

- Capture live packets on the local network
- Generate traffic by browsing and pinging
- Identify at least 3 protocols from the capture
- Save the capture file and write a brief analysis

---

## 🔧 Tools Used

- **Wireshark** (Packet Capture and Analysis)
- **Command Line Tools** (`ping`, `nslookup`)
- **Web Browser** (to trigger HTTP/HTTPS/QUIC traffic)

---

## 📸 Captured File

- `network_capture1.pcap`  
  This file contains the raw network packets captured over a ~1-minute session using Wireshark.

---

## 🌐 Protocols Identified

| Protocol | Description |
|----------|-------------|
| **ARP**  | Address Resolution Protocol - used to resolve IP addresses to MAC addresses on the local network. |
| **QUIC** | A modern transport protocol used by Google and others; runs over UDP and is used in HTTP/3. |
| **DNS**  | Domain Name System - resolves domain names to IP addresses. |
| **HTTP** | HyperText Transfer Protocol - the foundation of data communication for the web (used when visiting unencrypted sites). |
| **TLS**  | Transport Layer Security - encrypts web traffic (HTTPS). |
| **TCP**  | Transmission Control Protocol - ensures reliable delivery of data between devices. |

---

## 🔍 Observations

- **ARP packets** appeared at the beginning as devices resolved IPs to MACs.
- **QUIC traffic** indicated modern browsers are using HTTP/3 (UDP-based) for sites like Google.
- **DNS queries** resolved domains like `google.com`.
- **HTTP** traffic was observed when visiting non-HTTPS websites or using tools that trigger it.
- **TLS** encrypted most modern web traffic.
- **TCP** underpinned many of these protocols, ensuring reliable transport.

---

## 🧪 Filters Used in Wireshark

Examples of display filters used during the analysis:
```plaintext
arp         --> Show ARP packets
quic        --> Show QUIC protocol traffic
http        --> Show HTTP requests/responses
dns         --> Show DNS queries and replies
tls         --> Show TLS-encrypted traffic (HTTPS)
tcp         --> Show all TCP traffic
