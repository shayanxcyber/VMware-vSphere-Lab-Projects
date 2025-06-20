# Lab 4: vSphere Standard Switches and VLANs

### Objective
This lab explored the fundamentals of virtual networking within vSphere. The goal was to understand how to use vSphere Standard Switches (vSwitches) and Port Groups to segment network traffic using VLANs, a critical skill for creating secure, multi-tenant environments.

### Key Activities Performed

1.  **VM Deployment from OVF:**
    *   Deployed a new VM from an OVF/OVA template. This method is used for distributing pre-configured virtual appliances and ensures consistent deployments.
2.  **Network Segmentation with VLANs:**
    *   On the vCenter server, navigated to an ESXi host's virtual networking configuration.
    *   Created a new 'Virtual Machine Port Group' named 'Production' on the existing standard switch (`vSwitch0`).
    *   Assigned a specific VLAN ID (e.g., `100`) to this new port group.
3.  **Testing Connectivity:**
    *   Connected one VM to the default 'VM Network' port group (no VLAN ID) and a second VM to the new 'Production' port group (VLAN 100).
    *   Conducted ping tests between the two VMs. The pings failed, successfully demonstrating that VLANs logically isolate traffic at Layer 2, even when connected to the same physical switch.
4.  **Restoring Connectivity:**
    *   Created a second new port group ('Dev') without a VLAN ID.
    *   Moved the second VM from the 'Production' port group to the 'Dev' port group.
    *   Verified that connectivity was restored, as both VMs were now on the same broadcast domain (untagged traffic).

### Core Concepts & Skills Demonstrated

*   **Virtual Switching:** Understanding the role and function of a vSphere Standard Switch.
*   **VLANs (Virtual LANs):** Practical application of VLAN tagging (IEEE 802.1Q) to create logically isolated networks within a virtual environment.
*   **Network Security:** Demonstrated a fundamental network security practice by segmenting traffic between different groups of virtual machines.
*   **OVF/OVA Templates:** Experience with deploying virtual machines from standard template formats.

---
*This lab was completed as part of the 41891 Cloud Computing Infrastructure course.*
