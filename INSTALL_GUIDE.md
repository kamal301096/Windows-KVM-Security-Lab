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


<img width="1920" height="1080" alt="event" src="https://github.com/user-attachments/assets/38343ba2-7b32-4ba4-bc9e-ca827fdfd909" />
