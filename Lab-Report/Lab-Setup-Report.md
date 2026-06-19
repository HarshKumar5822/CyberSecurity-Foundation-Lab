# 🔬 Virtual Penetration Testing Lab Setup Report

## 1. Architecture Overview
The lab is built using a **Host-Only Network** topology to ensure a safe, isolated environment. The attacker machine cannot leak exploits to the host or local home network, and the vulnerable targets are strictly protected from public internet exposure.

* **Network Subnet:** `192.168.56.0/24` (Adjust based on your local settings)
* **Attacker VM:** Kali Linux 
* **Target VM:** Metasploitable2 / DVWA

---

## 2. Environment Installation Steps

### Step 1: Hypervisor Configuration
* VirtualBox/VMware installed.
* Configured a Host-Only Network adapter to completely isolate the environment.

### Step 2: Hacking Machine (Kali Linux)
* Imported Kali Linux OVA.
* Configured Network Adapter 1 to **Host-Only**.
* **Verification:** Verified internal network interface configuration using `ip a`.

> 📸 **[Insert your Kali Linux Desktop/IP confirmation screenshot here]**
> `![Kali Linux Setup](../screenshots/kali_desktop.png)`

### Step 3: Target Machine (Metasploitable2)
* Extracted and booted the Metasploitable2 virtual machine.
* Configured network adapter to **Host-Only**.
* Logged in using default credentials (`msfadmin` : `msfadmin`).

> 📸 **[Insert your Metasploitable2 boot terminal screenshot here]**
> `![Metasploitable Boot](../screenshots/metasploitable_boot.png)`

---

## 3. Network & Tool Verification Tests

### Test 1: Connectivity (Ping Test)
Verifying that Kali Linux can communicate successfully with Metasploitable2 over the private network.
```bash
ping -c 4 <TARGET_IP>
