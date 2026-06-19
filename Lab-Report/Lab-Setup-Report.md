# 🔬 Virtual Penetration Testing Lab Setup Report

## 1. Architecture Overview
The lab is built using a **Host-Only Network** topology to ensure a safe, isolated environment. The attacker machine cannot leak exploits to the local home network, and the vulnerable targets are protected from internet exposure.

* **Network Subnet:** `192.168.56.0/24` (or whatever your VirtualBox Host-Only IP is)
* **Attacker:** Kali Linux 
* **Target:** Metasploitable2 / DVWA

---

## 2. Environment Installation Steps

### Step 1: Hypervisor Configuration
* VirtualBox/VMware installed.
* Created a Host-Only Network adapter to isolate the environment.

### Step 2: Hacking Machine (Kali Linux)
* Imported Kali Linux OVA/ISO.
* Configured Network Adapter 1 to **Host-Only**.
* **Verification:** Run `ip a` to confirm the internal IP.

> 📸 **[यहाँ अपना Kali Linux का `ip a` या डेस्कटॉप वाला Screenshot इन्सर्ट करें]** > `![Kali Linux Desktop](../screenshots/kali_desktop.png)`

### Step 3: Target Machine (Metasploitable2)
* Downloaded and extracted Metasploitable2.
* Set network adapter to **Host-Only**.
* Booted and verified connection via default credentials (`msfadmin` : `msfadmin`).

> 📸 **[यहाँ अपना Metasploitable2 बूट स्क्रीन का Screenshot इन्सर्ट करें]** > `![Metasploitable Boot](../screenshots/metasploitable_boot.png)`

---

## 3. Network & Tool Verification Tests

### Test 1: Connectivity (Ping Test)
Verifying that Kali Linux can communicate with Metasploitable2.
```bash
ping -c 4 <TARGET_IP>
