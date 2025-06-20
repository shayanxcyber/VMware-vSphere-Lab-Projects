# Lab 1: VMware ESXi Installation and Virtual Machine Deployment

### Objective
The goal of this lab was to build the foundational layer of a virtualised environment. This involved installing VMware ESXi as a virtual machine itself and then using its web client to deploy and manage a guest virtual machine.

### Key Activities Performed

1.  **ESXi Host Installation:**
    *   Deployed a new virtual machine within VMware Workstation designated to become an ESXi host.
    *   Configured the VM with specific hardware parameters (2 vCPUs, 4GB RAM, 4 NICs).
    *   Mounted an ESXi installer ISO and completed the installation process.
2.  **Network Configuration:**
    *   Accessed the ESXi Direct Console User Interface (DCUI) post-installation.
    *   Configured a static IP address, subnet mask, and gateway for the management network to ensure stable connectivity.
3.  **VM Deployment on ESXi:**
    *   Connected to the new ESXi host via its web-based vSphere Host Client.
    *   Created a new guest virtual machine (`YourName-vm1`) on the host.
    *   Configured the guest VM's properties, including Guest OS type (Ubuntu Linux), memory, and thin-provisioned storage.
    *   Powered on the guest VM and accessed its console through the browser.

### Core Concepts & Skills Demonstrated

*   **Hypervisor Installation:** Hands-on experience with installing a Type-1 hypervisor (VMware ESXi).
*   **Nested Virtualisation:** Understanding and implementing a hypervisor within another hypervisor (ESXi inside VMware Workstation).
*   **Virtual Networking:** Basic configuration of a virtual machine's management network.
*   **VMware vSphere Client:** Proficiency in using the primary web interface for managing a standalone ESXi host.
*   **Virtual Machine Provisioning:** Understanding the process of creating, configuring, and running virtual machines on a hypervisor.

---
*This lab was completed as part of the 41891 Cloud Computing Infrastructure course.*
