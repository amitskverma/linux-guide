# Episode 4: System Monitoring

A quick reference guide for essential Linux system monitoring commands.

---

## 🛠️ Command Cheat Sheet

| Command | Description | Example Usage |
| :--- | :--- | :--- |
| **`df -h`** | Check overall disk space usage in human-readable format (MB/GB) | `df -h` |
| **`du -sh`** | Display total size breakdown of a specific directory or folder | `du -sh /var/log` |
| **`free -h`** | Display free and used memory (RAM & Swap) | `free -h` |
| **`uptime`** | Show how long the system has been running, user count, and load averages | `uptime` |
| **`uname -a`** | Display detailed system, Linux kernel, and architecture information | `uname -a` |

---

## 📋 Detailed Explanation

### 1. `df -h` — Disk Space Usage
Shows available and used disk space on all mounted filesystems.
* `-h`: Formats output into human-readable units (`G` for Gigabytes, `M` for Megabytes).

### 2. `du -sh` — Folder Size Breakdown
Calculates total disk space used by a specific directory.
* `-s`: Summarize total size (instead of listing every file inside).
* `-h`: Human-readable format.

### 3. `free -h` — Memory / RAM Usage
Provides a quick snapshot of available physical memory and swap space.
* Helpful for diagnosing low memory or high swap usage issues.

### 4. `uptime`
Tells you how long the server/system has been running without a reboot, along with system load averages over 1, 5, and 15 minutes.

### 5. `uname -a`
Prints all system information including OS kernel version, hostname, and hardware architecture (e.g., `x86_64`).

---

## 🚀 Quick Usage Example

```bash
# Check memory availability
free -h

# Find out system kernel version
uname -a
```