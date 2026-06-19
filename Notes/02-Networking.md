# 🌐 Networking Fundamentals

## 1. OSI Model Layers & Functions
The Open Systems Interconnection (OSI) model characterizes and standardizes communication functions across 7 distinct layers.

| Layer Number | Layer Name | Primary Function | Core Protocol / Data Unit |
| :--- | :--- | :--- | :--- |
| 7 | **Application** | Network process to application | HTTP, HTTPS, FTP, DNS (Data) |
| 6 | **Presentation**| Data representation and encryption | SSL, TLS, JPEG, ASCII (Data) |
| 5 | **Session** | Interhost communication / Sessions | RPC, NetBIOS (Data) |
| 4 | **Transport** | End-to-end connections and reliability | TCP, UDP (Segments) |
| 3 | **Network** | Path determination and logical addressing| IP, ICMP, IPsec (Packets) |
| 2 | **Data Link** | Physical addressing and media access | Ethernet, MAC, ARP (Frames) |
| 1 | **Physical** | Binary transmission over physical media | Cables, Hubs, Bits (Bits) |

---

## 2. TCP/IP Protocol Suite
The TCP/IP model is a simplified 4-layer architecture practically utilized on modern networks.

*   **Application Layer:** Handles high-level protocols (HTTP, FTP, SMTP, DNS).
*   **Transport Layer:** Manages host-to-host communication.
    *   **TCP (Transmission Control Protocol):** Connection-oriented, guarantees packet delivery using a **3-Way Handshake** (SYN ➡️ SYN-ACK ⬅️ ACK ➡️).
    *   **UDP (User Datagram Protocol):** Connectionless, fast, unreliable (no verification of delivery).
*   **Internet Layer:** Handles packet routing and logical addressing (IP).
*   **Network Access Layer:** Direct physical mappings (Ethernet, MAC).

---

## 3. DNS & HTTP/HTTPS Deep Dive
*   **DNS (Domain Name System):** Resolves human-readable domain names (e.g., `google.com`) into computer-readable IP addresses. Operates over UDP port 53.
*   **HTTP (Hypertext Transfer Protocol):** Clear-text web communication protocol. Operates on port 80. Completely insecure against sniffing attacks.
*   **HTTPS (HTTP Secure):** Encrypts normal HTTP traffic using SSL/TLS. Operates on port 443. Protects data in transit from eavesdropping.

---

## 4. IP Addressing, Subnetting, and NAT
*   **IPv4 Address:** A 32-bit logical address broken into 4 octets (e.g., `192.168.1.1`).
*   **Subnetting:** The process of dividing a large network into smaller, manageable sub-networks (subnets). Masking balances the Network ID versus Host ID allocation space.
*   **NAT (Network Address Translation):** Translates private, non-routable IP addresses within an internal network into a single public IP address before forwarding packets to the internet, preserving IPv4 address space.
