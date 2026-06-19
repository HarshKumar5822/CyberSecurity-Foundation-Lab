# 🐧 Essential Linux Cheat-Sheet for Penetration Testers

## 1. File System Navigation
| Command | Description | Example |
| :--- | :--- | :--- |
| `pwd` | Present Working Directory (Check where you are) | `pwd` |
| `ls -la` | List all files including hidden files with details | `ls -la` |
| `cd` | Change directory | `cd /var/www/html` |
| `mkdir` | Create a new directory | `mkdir targets` |

## 2. File & Directory Permissions
* **Permissions Types:** `r` (Read = 4), `w` (Write = 2), `x` (Execute = 1)
* **User Categories:** `u` (User), `g` (Group), `o` (Others)

| Command | Description | Example |
| :--- | :--- | :--- |
| `chmod 755 file.sh` | Owner: Full, Group/Others: Read & Execute | `chmod +x script.sh` |
| `chmod 600 id_rsa` | Secure private key (Owner read/write only) | `chmod 600 ~/.ssh/id_rsa` |
| `chown root:root file`| Change owner and group to root | `sudo chown admin:admin report.txt` |

## 3. Package Management (Debian/Kali)
| Command | Description |
| :--- | :--- |
| `sudo apt update` | Update package lists from repositories |
| `sudo apt upgrade -y` | Upgrade all installed packages to latest version |
| `sudo apt install <pkg>`| Install a new tool (e.g., `sudo apt install seclists`) |
| `sudo dpkg -i file.deb`| Install a standalone `.deb` package |

## 4. Networking Commands
| Command | Description | Example |
| :--- | :--- | :--- |
| `ip a` / `ifconfig` | View IP addresses and interface configurations | `ip a` |
| `ping -c 4 <ip>` | Send 4 ICMP packets to test connectivity | `ping -c 4 10.0.2.15` |
| `netstat -tunlp` | View active connections and listening ports | `sudo netstat -tunlp` |
| `traceroute <ip>` | Trace the path packets take to reach a host | `traceroute google.com` |
