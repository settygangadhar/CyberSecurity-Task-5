## 📡 Network Traffic Analysis with Wireshark (macOS)

**Author:** Gangadhar J  
**Date:** September 29, 2025  
**Platform:** macOS (Wi-Fi interface `en0`)  
**Tool:** Wireshark

### 🎯 Objective
Capture live network traffic and analyze basic protocols using Wireshark. This hands-on exercise demonstrates packet inspection, protocol filtering, and traffic awareness.

---

### 🛠️ Setup & Execution

1. **Installed Wireshark** via official `.dmg` on macOS.
2. **Selected active interface** (`en0`) for Wi-Fi.
3. **Generated traffic** by:
   - Browsing `https://example.com`
   - Running `ping google.com` in Terminal
4. **Captured for 1 minute**, then stopped.
5. **Filtered packets** using:
   - `http`
   - `dns`
   - `icmp`
   - `tcp`
6. **Saved capture** as `macos_network_capture_task5.pcap`

---

### 🔍 Protocols Identified

| Protocol | Description | Sample Packet Count |
|----------|-------------|----------------------|
| **HTTP** | Web traffic (GET/POST requests) | 52 |
| **DNS**  | Domain name resolution queries | 28 |
| **ICMP** | Ping requests/replies | 12 |
| **TCP**  | Transport layer communication | 110 |

---

### 📊 Observations

- DNS queries resolved domain names before HTTP requests.
- TCP handshake observed (SYN → SYN-ACK → ACK).
- ICMP packets confirmed connectivity to external servers.
- HTTP packets showed GET requests to `example.com` and response headers.

---

### 📁 Files

- `macos_network_capture_task5.pcap` – Raw packet capture
- `screenshots/` – Annotated Wireshark views:
  - Interface selection
  - Filtered HTTP traffic
  - Expanded packet layers

---

### 💡 Skills Demonstrated

- Protocol identification (HTTP, DNS, ICMP, TCP)
- Packet filtering and inspection
- Hands-on use of Wireshark on macOS
- Basic traffic generation and analysis

---

### 🚀 Next Steps

- Perform deeper inspection (e.g., TLS handshake, HTTP headers)
- Compare traffic across different interfaces (Ethernet vs Wi-Fi)
- Document packet flags and payloads for advanced analysis
