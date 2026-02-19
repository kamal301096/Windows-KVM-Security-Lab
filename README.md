# 🛡️ Enterprise Windows Lab on KVM/QEMU
### *Advanced Virtualization & Detection Engineering for Security Professionals*

## 📖 Overview
This repository documents the deployment of a **Windows Server 2022** environment on a **KVM/QEMU** hypervisor. This lab is designed to simulate a real-world enterprise server to study "Red Team" attack patterns and "Blue Team" defense mechanisms.

By choosing KVM over standard Type-2 hypervisors (like VirtualBox), this setup provides bare-metal performance and deeper control over the hardware abstraction layer.

## 🛠️ The Stack
* **Host OS:** Linux (Debian/Ubuntu based)
* **Hypervisor:** KVM / QEMU 
* **Virtualization API:** `libvirt` / `virt-manager`
* **Guest OS:** Windows Server 2022 (LTSC)
* **Drivers:** VirtIO (Optimized Paravirtualized I/O)
* **Monitoring:** Microsoft Sysmon with SwiftOnSecurity Configuration

## 🏗️ Lab Topology


## 🚀 Key Technical Features
* **VirtIO Optimization:** Custom bus configuration to prevent BSOD (Blue Screen of Death) and optimize disk throughput.
* **Detection Engineering:** Real-time logging of **Event IDs 1 (Process), 3 (Network), and 22 (DNS)**.
* **XML Analysis:** Deep-dive forensics using the Windows Event Viewer "Details" tab to track malicious hashes.

## 📈 Professional Goals
The objective of this lab is to prepare for **SOC Analyst** and **Security Engineer** roles by mastering:
1.  **Hardware Level Virtualization:** Managing VMs via CLI (`virsh`) and GUI.
2.  **Telemetry Collection:** Setting up "Black Box" recorders (Sysmon).
3.  **Vulnerability Management:** Identifying and patching OS-level flaws.

---
*Created by Kamalpreet Singh - 2026 Cybersecurity Roadmap*
