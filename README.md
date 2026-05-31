Kali Linux VM — Network Troubleshooting

**Date:** 31 May 2025  
**Format:** STAR (Situation, Task, Action, Result)

---

## Overview

Diagnosed and resolved a DHCP connectivity issue on a Kali Linux VM 
running in VirtualBox NAT mode. This lab exercise demonstrates 
real-world Linux network troubleshooting using command-line tools.

---

## Environment

- **Guest OS:** Kali Linux (VirtualBox VM)
- **Hypervisor:** Oracle VirtualBox — NAT mode
- **Host OS:** Windows 10/11

---

## Problem (Situation)

On boot, the Kali Linux VM failed to obtain an IP address via DHCP, 
resulting in no network connectivity. Running `ip a` showed the 
network interface had no assigned IP.

---

## Task

Identify the root cause of the DHCP failure and restore network 
connectivity without reinstalling or reconfiguring VirtualBox.

---

## Steps Taken (Action)

1. Ran `ip a` to confirm the interface had no IP address
2. Checked the DHCP client service status using `systemctl`
3. Edited `/etc/dhcpcd.conf` using `nano` to correct configuration
4. Restarted the `dhcpcd` service via `systemctl`
5. Verified connectivity using `ping`

---

## Outcome (Result)

Network connectivity was successfully restored. The VM obtained an 
IP address via DHCP and was able to reach external hosts.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| `ip` | Check network interface status |
| `dhcpcd` | DHCP client daemon |
| `nano` | Edit config file |
| `systemctl` | Manage services |
| `ping` | Verify connectivity |

---

## Files

- `STAR-writeup.pdf` — Full STAR format write-up of this exercise
