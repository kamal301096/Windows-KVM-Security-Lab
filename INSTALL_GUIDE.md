# 🛠️ Technical Installation Steps (KVM)

## 1. Host Preparation
Ensure hardware virtualization is enabled and install the KVM stack:

sudo apt update
sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients virt-manager bridge-utils

2. VirtIO Driver Integration
Windows does not natively "see" KVM VirtIO disks. You must sideload the drivers during installation:

Download the virtio-win.iso.

Add a second CD-ROM drive in virt-manager pointing to this ISO.

During Windows Setup, click "Load Driver" and point to viostor\2k22\amd64.

3. Sysmon Deployment
To enable professional monitoring, install Sysmon with a hardened configuration:

Download: Sysinternals Suite.

Config: Apply the SwiftOnSecurity XML.

Command: .\Sysmon64.exe -i sysmonconfig-export.xml -accepteula

4. Verification
Run a test command to verify the "Detection Engine" is recording:

# Run a test process
C:\Windows\System32\ping.exe google.com

# Check Event Viewer
# Path: Applications and Services Logs > Microsoft > Windows > Sysmon > Operational

---

### 💡 Why this is a "Win" for you:
1.  **GitHub History:** When you apply for jobs in Australia, they will see you started this in **February 2026**. Long history = More trust.
2.  **Clean Code:** Using the "Code Blocks" (the grey boxes) shows you know how to document technical steps for other engineers.

**Shall I help you upload these files to GitHub now, or would you like to add a "Troubleshooting" section first about the VirtIO driver issue you fixed yesterday?** (It would show you are a great problem solver!) 🚀📂
