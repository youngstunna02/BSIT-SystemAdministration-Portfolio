# Week 03 – Ubuntu Server Installation and Configuration

## Project Overview

This Week 03 project focuses on installing and configuring an Ubuntu Server operating system inside a virtual machine. The activity demonstrates the basic process of deploying a Linux server environment using virtualization. It covers virtual machine creation, Ubuntu Server installation, system configuration, boot process concepts, and verification of the completed installation.

The project also provides an opportunity to understand how BIOS and UEFI firmware affect the boot process and how an operating system progresses from firmware initialization to the Linux kernel and system services.

## Learning Objectives

By completing this activity, the following objectives were achieved:

* Install Ubuntu Server in a virtual machine.
* Configure the basic settings of a Linux server.
* Understand the role of virtualization in server administration.
* Identify the differences between BIOS and UEFI.
* Understand the major stages of the Linux boot process.
* Verify that the installed Ubuntu Server system is functioning correctly.
* Develop basic troubleshooting and system administration skills.
* Document the installation and configuration process professionally.

## Virtual Machine Specifications

| Specification           | Details                                 |
| ----------------------- | --------------------------------------- |
| Virtualization Software | Oracle VM VirtualBox                    |
| Operating System        | Ubuntu Server                           |
| Architecture            | 64-bit                                  |
| CPU                     | 2 Virtual Processors                    |
| RAM                     | 4 GB                                    |
| Storage                 | 25 GB Virtual Disk                      |
| Network                 | NAT                                     |
| Firmware                | UEFI/BIOS depending on VM configuration |
| Installation Media      | Ubuntu Server ISO                       |

## Installation Summary

The Ubuntu Server virtual machine was created using Oracle VM VirtualBox. The virtual machine was configured with the required CPU, memory, storage, and network resources before starting the installation.

The Ubuntu Server ISO image was mounted as the virtual machine's installation media. During installation, the appropriate language, keyboard layout, storage configuration, hostname, username, and password were configured.

After the installation process completed, the ISO image was removed or detached from the virtual optical drive, and the virtual machine was restarted. The system successfully booted into the newly installed Ubuntu Server environment.

## Configuration Summary

After installation, the Ubuntu Server environment was configured and prepared for basic server administration. The following tasks were performed:

* Logged in using the created user account.
* Verified the hostname and operating system information.
* Checked the assigned network configuration.
* Verified available disk space.
* Checked system memory and CPU information.
* Updated the package information using the appropriate package management commands.
* Confirmed that the system could access the network.
* Verified that the installed system was able to boot normally after restarting.

## Verification Results

The installation and configuration were verified using basic Linux commands and system checks.

| Verification          | Expected Result                                        | Result |
| --------------------- | ------------------------------------------------------ | ------ |
| User login            | User successfully logs into Ubuntu Server              | Passed |
| OS verification       | Ubuntu Server information is displayed                 | Passed |
| Hostname verification | Correct hostname is displayed                          | Passed |
| CPU/Memory check      | Assigned virtual resources are detected                | Passed |
| Disk check            | Virtual disk is detected and usable                    | Passed |
| Network check         | Network interface is available                         | Passed |
| Internet connectivity | System can communicate with external network resources | Passed |
| Reboot test           | System boots successfully after restart                | Passed |

## BIOS vs UEFI Highlights

BIOS and UEFI are firmware interfaces responsible for initializing hardware and starting the operating system boot process.

| BIOS                                                 | UEFI                                               |
| ---------------------------------------------------- | -------------------------------------------------- |
| Older firmware standard                              | Modern firmware standard                           |
| Uses traditional MBR partitioning                    | Commonly uses GPT partitioning                     |
| Generally has a text-based interface                 | Can provide a more advanced graphical interface    |
| Has limitations with modern hardware and large disks | Supports modern hardware and large storage devices |
| Uses a traditional boot process                      | Uses an EFI System Partition and boot manager      |
| Generally slower and less flexible                   | Generally faster and more flexible                 |

UEFI is generally preferred for modern systems because it provides improved hardware compatibility, supports GPT, and offers additional security and boot-management features.

## Embedded Boot Process Flowchart

The Ubuntu Server boot process can be summarized as follows:

```text
┌──────────────────────┐
│ Power On / Restart   │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ BIOS / UEFI Firmware │
│ Hardware Initialize  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Boot Device Selected │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Bootloader           │
│ GRUB                 │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Linux Kernel         │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ systemd / Init       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ System Services      │
│ and Networking       │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Ubuntu Server Login  │
└──────────────────────┘
```

## Challenges Encountered

One of the challenges encountered during the activity was properly configuring the virtual machine before beginning the Ubuntu Server installation. The assigned RAM, CPU, storage, network adapter, and installation ISO had to be configured correctly to prevent installation problems.

Another challenge was understanding the difference between the virtual machine's firmware settings and the operating system's boot process. BIOS and UEFI perform similar fundamental functions, but their boot methods and partitioning requirements differ.

Troubleshooting network connectivity and verifying the system after installation also required careful checking. Using Linux commands to inspect system information helped confirm that the virtual hardware and Ubuntu Server installation were working correctly.

## Reflection

Completing Week 03 gave me a better understanding of how an operating system can be deployed and managed in a virtualized environment. Before performing this activity, I was more familiar with using operating systems from the perspective of a normal desktop user. Installing Ubuntu Server in VirtualBox allowed me to experience the process from a system administration perspective, where hardware resources, storage, networking, firmware, and the operating system all need to work together.

One of the most important things I learned was that virtualization makes it possible to create and test server environments without requiring a separate physical computer. By assigning virtual CPU, RAM, storage, and network resources, I was able to create a functional Ubuntu Server environment that could be used for future administration activities. This is useful because server administrators can test configurations and troubleshoot problems in a controlled environment before applying changes to production systems.

I also gained a clearer understanding of the Linux boot process. The flow from BIOS or UEFI to the bootloader, Linux kernel, systemd, system services, and finally the login environment helped me understand what happens when a computer starts. Learning the difference between BIOS and UEFI was also valuable because firmware configuration can affect how an operating system boots and how storage devices are organized.

The verification stage was another important part of the activity. Rather than assuming that the installation was successful, I learned to verify the operating system, hardware resources, storage, network connectivity, and reboot behavior. This approach is important in system administration because successful installation should always be followed by testing.

Overall, this activity improved my confidence in working with Linux and virtual machines. It also strengthened my troubleshooting and documentation skills. The experience will be useful for future activities involving server configuration, networking, security, and system administration.

## References

1. Ubuntu. (2026). *Ubuntu Server Documentation*. Canonical.
2. Oracle. (2026). *Oracle VM VirtualBox Documentation*. Oracle Corporation.
3. Ubuntu. (2026). *Ubuntu Documentation*. Canonical.
4. The Linux Kernel Organization. (2026). *The Linux Kernel Documentation*.
5. Unified Extensible Firmware Interface Forum. (2026). *UEFI Specifications*.
