# linux-command-cheatsheet
 A collection of essential Linux commands, practical examples, and notes documenting my Linux learning journey.

## Overview
This repository contains a practical collection of Linux commands grouped by task. It serves as a quick reference for common Linux administration and cybersecurity operations.

Each command includes a short explanation and an example of its usage.

## 1. File and Directory Management

| Command | Description | Example |
|---|---|---|
| `pwd` | Displays the current working directory. | `pwd` |
| `ls -la` | Lists all files, including hidden files. | `ls -la` |
| `cd` | Changes the current directory. | `cd /home/user` |
| `mkdir` | Creates a new directory. | `mkdir security-lab` |
| `touch` | Creates an empty file. | `touch notes.txt` |
| `cp` | Copies files or directories. | `cp notes.txt backup.txt` |
| `mv` | Moves or renames files. | `mv notes.txt report.txt` |
| `rm` | Removes a file. | `rm oldfile.txt` |
| `find` | Searches for files and directories. | `find /home -name "*.txt"` |

## 2. User and Group Management

| Command | Description | Example |
|---|---|---|
| `whoami` | Displays the current username. | `whoami` |
| `id` | Displays user and group IDs. | `id` |
| `who` | Shows currently logged-in users. | `who` |
| `useradd` | Creates a new user. | `sudo useradd analyst` |
| `passwd` | Changes a user's password. | `sudo passwd analyst` |
| `groups` | Displays the groups a user belongs to. | `groups` |
| `usermod` | Modifies user account settings. | `sudo usermod -aG sudo analyst` |
| `last` | Displays recent login sessions. | `last` |

## 3. File Permissions and Ownership

| Command | Description | Example |
|---|---|---|
| `ls -l` | Displays file permissions and ownership. | `ls -l notes.txt` |
| `chmod` | Changes file permissions. | `chmod 755 script.sh` |
| `chown` | Changes file ownership. | `sudo chown analyst notes.txt` |
| `chgrp` | Changes group ownership. | `sudo chgrp analysts notes.txt` |
| `umask` | Displays or changes default permission settings. | `umask` |

**Practical example:**

```bash
chmod 700 private.txt
```

This gives the file owner read, write and execute permissions while denying access to group members and others.

## 4. Process Management

| Command | Description | Example |
|---|---|---|
| `ps aux` | Displays running processes. | `ps aux` |
| `top` | Monitors system processes in real time. | `top` |
| `htop` | Provides an interactive process monitor (if installed). | `htop` |
| `pgrep` | Searches for processes by name. | `pgrep firefox` |
| `kill` | Sends a signal to a process. | `kill 1234` |
| `killall` | Terminates processes by name. | `killall firefox` |
| `nice` | Starts a process with a specified priority. | `nice -n 10 sleep 100` |

## 5. System Logs and Monitoring

| Command | Description | Example |
|---|---|---|
| `dmesg` | Displays kernel-related messages. | `dmesg` |
| `journalctl` | Displays system journal logs. | `journalctl -xe` |
| `tail` | Displays the end of a file. | `tail -n 20 /var/log/syslog` |
| `tail -f` | Monitors a log file in real time. | `tail -f /var/log/auth.log` |
| `grep` | Searches for matching text. | `grep "Failed" /var/log/auth.log` |
| `last` | Displays login history. | `last` |
| `uptime` | Displays system uptime and load averages. | `uptime` |

## 6. Networking Commands

| Command | Description | Example |
|---|---|---|
| `ip addr` | Displays network interface addresses. | `ip addr` |
| `ip route` | Displays routing information. | `ip route` |
| `ping` | Tests network connectivity. | `ping -c 4 8.8.8.8` |
| `ss -tulnp` | Displays listening network sockets. | `sudo ss -tulnp` |
| `curl` | Transfers data from a URL. | `curl -I https://example.com` |
| `traceroute` | Traces the route to a destination (if installed). | `traceroute example.com` |
| `nslookup` | Queries DNS information. | `nslookup example.com` |

## 7. Disk and Storage Management

| Command | Description | Example |
|---|---|---|
| `df -h` | Displays available disk space. | `df -h` |
| `du -sh` | Displays directory size. | `du -sh /home/user` |
| `lsblk` | Lists block devices. | `lsblk` |
| `mount` | Displays mounted filesystems. | `mount` |
| `free -h` | Displays memory usage. | `free -h` |

## 8. Package Management

| Command | Description | Example |
|---|---|---|
| `sudo apt update` | Updates package repository information. | `sudo apt update` |
| `sudo apt upgrade` | Upgrades installed packages. | `sudo apt upgrade` |
| `sudo apt install` | Installs a package. | `sudo apt install nmap` |
| `sudo apt remove` | Removes an installed package. | `sudo apt remove nmap` |
| `dpkg -l` | Lists installed packages. | `dpkg -l` |

## 9. Cybersecurity-Relevant Commands

| Command | Description | Example |
|---|---|---|
| `sha256sum` | Generates a SHA-256 file hash. | `sha256sum report.txt` |
| `md5sum` | Generates an MD5 hash. | `md5sum report.txt` |
| `sudo` | Executes commands with elevated privileges. | `sudo whoami` |
| `history` | Displays previously executed commands. | `history` |
| `strings` | Extracts readable strings from a file. | `strings suspicious.bin` |
| `file` | Identifies a file's type. | `file suspicious.bin` |
| `stat` | Displays file metadata. | `stat report.txt` |

## 10. Redirection and Pipes

| Command | Description | Example |
|---|---|---|
| `>` | Redirects output and overwrites a file. | `echo "Hello" > notes.txt` |
| `>>` | Appends output to a file. | `echo "Linux" >> notes.txt` |
| `|` | Passes output to another command. | `ps aux | grep ssh` |
| `2>` | Redirects error output. | `ls missing 2> errors.txt` |
| `tee` | Displays output while writing it to a file. | `echo "Test" | tee output.txt` |

---

## Learning and Practical Application

The commands in this repository are intended for practical Linux administration, troubleshooting, system monitoring and introductory cybersecurity investigations.

Examples can be tested in a Linux virtual machine, such as Ubuntu or Kali Linux.

**Important:** Some commands require elevated privileges, and commands that modify permissions, terminate processes or delete files should be used carefully.

## Disclaimer
This repository is for educational purposes and documents commands used in authorized Linux environments.
