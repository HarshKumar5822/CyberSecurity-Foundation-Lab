# 🐧 Linux Fundamentals & Environment Setup

## 1. File System Navigation
Linux organizes files in a hierarchical tree structure starting from the root directory `/`.

*   `pwd` (Print Working Directory): Displays the absolute path of the current working directory.
*   `ls` (List): Lists directory contents. Common flags:
    *   `-l`: Long listing format (shows permissions, owner, size, and modification time).
    *   `-a`: Includes hidden files (files starting with a dot `.`).
*   `cd` (Change Directory): Navigates between directories.
    *   `cd ..`: Move up one level.
    *   `cd ~`: Move to the user's home directory.

## 2. File & Directory Permissions
Linux uses a security model that determines who can read, write, or execute a file.

### Permission Breakdown
Permissions are split into three categories: **User (u)**, **Group (g)**, and **Others (o)**.
*   `r` (Read) = 4
*   `w` (Write) = 2
*   `x` (Execute) = 1

### Modification Commands
*   `chmod`: Changes file access permissions.
    *   *Absolute Mode:* `chmod 755 script.sh` (User: rwx, Group: r-x, Others: r-x).
    *   *Symbolic Mode:* `chmod +x script.sh` (Grants execute permission to everyone).
*   `chown`: Changes file ownership.
    *   Syntax: `sudo chown root:root secret.txt` (Changes owner and group to root).

## 3. Package Management
Package managers automate installing, updating, configuring, and removing software packages.

*   `apt update`: Synchronizes local package index files from their repositories.
*   `apt upgrade`: Installs the newest versions of all packages currently installed.
*   `apt install <package_name>`: Downloads and installs a package along with dependencies.
*   `dpkg -i package.deb`: Manually installs a standalone Debian package file.

## 4. Basic Networking Commands
Essential utilities used to troubleshoot, check connectivity, and analyze network interfaces:
*   `ifconfig` / `ip a`: Displays active network interfaces, MAC addresses, and assigned IP addresses.
*   `ping`: Sends ICMP Echo Requests to verify network-level connectivity to a specific host.
*   `netstat -tunlp`: Shows active network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
*   `traceroute`: Tracks the route packets take from the local machine to a destination host, mapping out routers along the path.
