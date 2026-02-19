# 🛠️ Technical Installation Steps (KVM)

## 1. Host Preparation
Ensure hardware virtualization is enabled and install the KVM stack:
```bash
sudo apt update
sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients virt-manager bridge-utils
