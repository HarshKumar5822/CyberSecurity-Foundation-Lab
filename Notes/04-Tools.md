### `Notes/04-Tools.md`

```markdown
# 🛠️ Penetration Testing Tool Familiarization

## 1. Wireshark (Packet Capture & Analysis)
Wireshark is a graphical network protocol analyzer that allows real-time packet capture and inspection.

*   **Primary Use Case:** Traffic monitoring, malware analysis, network debugging, and credential sniffing on insecure protocols.
*   **Key Filters:**
    *   `ip.addr == 192.168.56.101`: Filters for traffic moving to or from that host.
    *   `http` or `tcp.port == 80`: Isolates insecure web server traffic.
    *   `icmp`: Displays only ping traffic.

---

## 2. Nmap (Network Reconnaissance)
Network Mapper (Nmap) is a terminal utility used for network discovery and vulnerability auditing.

*   **Core Execution Commands:**
    *   `nmap -F <target>`: Fast port scan (Scans top 100 common ports).
    *   `nmap -sV <target>`: Probes open ports to determine service name and software version info.
    *   `nmap -O <target>`: Remotely determines operating system identity via TCP/IP stack fingerprinting.

---

## 3. Burp Suite (Web Proxy & Interception)
Burp Suite functions as an inline intercepting proxy tool evaluating web application attack paths.

*   **How it Works:** Acts as a Man-in-the-Middle (MitM) agent standing directly between the pen-tester's browser and the target web server.
*   **Core Modules:**
    *   **Proxy/Intercept:** Allows the security analyst to catch a live outgoing HTTP request, edit parameter values (manipulating cookies, headers, input vectors), and forward the modified request to the target.
    *   **Repeater:** Manually resends single specific requests to experiment with parameters repeatedly without recapturing.

---

## 4. Netcat (Network Debugging & Swiss Army Knife)
Netcat (`nc`) reads and writes data across network connections using TCP or UDP protocols.

*   **Key Security Use Cases:**
    *   **Banner Grabbing:** Checking version strings running on remote ports.
```bash
        nc -nv <target_ip> 80
        ```
    *   **Port Listening (Setting up simple backdoors/reverse shells):**
```bash
        nc -lvp 4444
        ```
