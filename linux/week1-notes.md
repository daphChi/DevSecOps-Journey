# 🐧 My Linux Learning Journey

This repo documents the commands I try, what they do, and scenarios where they’re useful.  
Think of it as my Linux study book + SOC/SecOps notes.

---

## 📂 Files & Directories
- `ls -la` → list files (with details & hidden ones).
- `cd path/` → change directory.
- `pwd` → print current working directory.
- `mkdir -p lab/a/b` → create nested directories.
- `touch file.txt` → create empty file.
- `echo "hi" > file.txt` → write text to file.
- `tree folder/` → view folder structure.

---

## 🔑 Permissions & Ownership
- `ls -l` → show file permissions.
- `chmod 644 file.txt` → owner can read/write, others read-only.
- `chmod 600 file.txt` → only owner can read/write.
- `chmod 755 script.sh` → owner full, others can read & execute.
- `umask` → show default permission mask.

---

## 🖥️ Processes
- `ps aux` → show all processes.
- `top` → live system monitor (`q` to quit).
- `htop` → nicer system monitor (if installed).
- `kill -9 <PID>` → force kill a process.
- `nice -n 10 command` → start with lower priority.
- `renice -n 5 -p <PID>` → change priority of running process.

---

## 📜 Logs
- `cat file.log` → show entire file.
- `less file.log` → scroll through a long file.
- `tail -f file.log` → follow live log updates.
- `journalctl --since "1 hour ago"` → system logs in last hour.
- `journalctl -u ssh` → logs for the SSH service.
- `journalctl --since "1 hour ago" | grep -i warning` → filter warnings (case-insensitive).

---

## 🌐 Networking
- `ip a` → show network interfaces + IPs.
- `ping 8.8.8.8` → test network reachability.
- `curl http://site.com` → fetch a web page (test connectivity).
- `dig domain.com` → DNS lookup (get IP, MX, TXT records).
- `ss -tulpn` → list open ports + processes.
- `traceroute site.com` → trace route packets take.

---

## 🌍 Lightweight Servers
- `python3 -m http.server 8080` → start simple HTTP server on port 8080.
  - Visit `http://localhost:8080` in browser.
- `tar -czf backup.tar.gz folder/` → archive & compress.
- `tar -xzf backup.tar.gz` → extract archive.

---

## 🔐 Security Basics
- `id` → show current user + groups.
- `sudo` → run command as root.
- `whoami` → print current logged-in user.
- `last` → show login history.
- `w` → show who is logged in & what they’re doing.

---

## 🚨 Troubleshooting Scenarios
- Web server not responding:
  - `ps aux | grep nginx` → check if nginx is running.
  - `ss -tulpn | grep :80` → check if listening on port 80.
  - `journalctl -u nginx` → check logs.
- Strange high CPU usage:
  - `top` or `htop` → find PID.
  - `kill -9 <PID>` → stop suspicious process.

---

## 📝 Notes
This section is for personal observations:
- `localhost` always = 127.0.0.1 (your machine).
- Ports are like “doors” (80 = web, 22 = SSH, 443 = HTTPS).
- Logs are the first place to check when something fails.

---
