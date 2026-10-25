# Week 3 Portfolio Project: Enterprise Server Deployment & Configuration

**Course:** ITEP 414 – System Administration and Maintenance  
**Author:** Student Administrator  
**Environment:** Oracle VM VirtualBox  

---

## Project Overview

This repository contains all deliverables, documentation, verification logs, and technical diagrams for the Week 3 Portfolio Project. The project focuses on enterprise server virtualization, firmware analysis (BIOS vs. UEFI), low-level boot architecture, and comparative evaluations of enterprise operating systems (Ubuntu Server and Windows Server Evaluation).

---

## Directory Structure

```text
Week03/
├── README.md                          # Comprehensive project documentation & reflection
├── Installation_Guide.pdf             # Step-by-step professional installation manual
├── BIOS_vs_UEFI_Comparison.pdf        # Comparative firmware analysis report
├── OS_Comparison_Report.pdf           # Deep-dive enterprise OS comparison report
├── diagrams/
│   ├── BootProcess_Flowchart.pdf      # Sequential 8-stage boot process (PDF)
│   └── BootProcess_Flowchart.png      # Sequential 8-stage boot process (PNG)
└── screenshots/
    ├── Verify Hostname.png            # Hostname and SSH status
    └── Verify IP Address.png          # IP config
    └── Test Internet Connectivity.png # ping
    └── Verify SSH Status.png          # SSH status
```

---

## Virtual Machine Specifications

| Virtual Machine | Hostname / Computer Name | RAM Allocation | Processor Cores | Storage Size | Firmware / OS Version |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Ubuntu Server** | `server01` | 4096 MB (4 GB) | 2 vCPUs | 40 GB | UEFI / Ubuntu Server 24.04 LTS |
| **Windows Server** | `WINSERVER01` | 4096 MB (4 GB) | 2 vCPUs | 50 GB | UEFI / Windows Server Evaluation |

---

## Key Deliverables & Summary

1. **Ubuntu Server Deployment:** Provisioned `server01`, configured dynamic networking, established OpenSSH remote shell access, and verified system package integrity.
2. **Firmware Analysis:** Contracted traditional BIOS (MBR, 2.2TB disk limit, 16-bit) with modern UEFI (GPT, Secure Boot, `.efi` binaries) via a comparative matrix.
3. **Boot Process Mapping:** Illustrated the 8-stage sequential boot cycle of Ubuntu Server (`Power On` $\rightarrow$ `POST` $\rightarrow$ `Boot Device Detection` $\rightarrow$ `GRUB2` $\rightarrow$ `Kernel` $\rightarrow$ `systemd` $\rightarrow$ `Services Start` $\rightarrow$ `Login Prompt`).
4. **Windows Server Evaluation:** Deployed Windows Server Evaluation, resolved installation partition allocation errors using `diskpart`, assigned computer name `WINSERVER01`, and verified configuration via Server Core (`SConfig`).
5. **OS Comparison Report:** Evaluated Windows Server, Ubuntu Server, and Rocky Linux across licensing, user interfaces, package management (`APT` vs. `DNF` vs. MSI), security (`SELinux` vs. `AppArmor`), and enterprise use cases.

---

## Verification & Troubleshooting

### Ubuntu Server Verification Commands
```bash
hostname                  # Confirms server01
ip addr                   # Validates enp0s3 network adapter & IP
ping -c 4 google.com      # Tests external internet connectivity
systemctl status ssh      # Confirms OpenSSH service is active
```

### Resolved Issues
* **Missing OpenSSH Package:** Resolved initial `Unit ssh.service could not be found` errors by updating package indexes and installing `openssh-server` via APT.
* **Windows Partition Error:** Cleared residual table metadata during Windows installation by deleting legacy partitions until the drive displayed entirely as unallocated space.

---

## Personal Reflection

Working through this week's portfolio project provided invaluable hands-on experience bridging theoretical enterprise architecture with practical system administration. Deploying virtualized instances side-by-side highlighted the stark operational differences between headless Linux environments—where mastery of the command line, package managers like APT, and system daemons is essential—and GUI/SConfig-driven Windows Server deployments. 

Mapping the low-level boot sequence and troubleshooting installation hurdles (such as partition table errors and missing SSH packages) reinforced the reality that successful system administration relies heavily on methodical problem-solving, meticulous documentation, and understanding how firmware, kernels, and user-space processes interact. This project solidifies foundational competencies required for managing scalable, secure enterprise cloud and on-premise infrastructure.

---

## References
* Canonical Ltd. (2026). *Ubuntu Server Documentation*.
* Microsoft Corporation (2026). *Windows Server Evaluation Documentation*.
* Oracle Corporation (2026). *Oracle VM VirtualBox User Manual*.