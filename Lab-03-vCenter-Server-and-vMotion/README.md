# Lab 3: vCenter Server Deployment and vMotion

### Objective
The objective of this lab was to centralise the management of the virtual environment by deploying vCenter Server Appliance (VCSA). Once the hosts were managed by vCenter, the lab demonstrated one of its most powerful features: Storage vMotion and live VM migration (vMotion).

### Key Activities Performed

1.  **vCenter Server Deployment:**
    *   Deployed and configured the vCenter Server Appliance (VCSA) VM.
    *   Accessed the vCenter management portal and performed initial setup, including connecting to the ESXi hosts.
2.  **Centralised Management:**
    *   Created a new Datacenter object within vCenter.
    *   Added the two existing ESXi hosts to the vCenter inventory, enabling unified management from a single interface.
3.  **Storage vMotion (Live Storage Migration):**
    *   Selected a running VM located on a local ESXi datastore.
    *   Initiated a 'Change storage only' migration to move the VM's files to the shared iSCSI datastore created in the previous lab, all while the VM remained powered on and operational.
4.  **vMotion (Live Compute Migration):**
    *   With the VM now residing on shared storage, initiated a 'Change compute resource only' migration.
    *   Successfully moved the running state (CPU and memory) of the virtual machine from one ESXi host to the other with no downtime or service interruption.
    *   Configured the vMotion kernel port (`vmk0`) on the ESXi hosts' management network to enable this functionality.

### Core Concepts & Skills Demonstrated

*   **Centralised Infrastructure Management:** Proficiency in deploying and using vCenter Server to manage multiple hosts.
*   **VMware vMotion:** Practical execution and understanding of live migration technology, a cornerstone of modern data centers.
*   **Zero-Downtime Maintenance:** Demonstrated a key use case for vMotion, which allows for host maintenance without impacting running services.
*   **VMkernel Networking:** Configuration of VMkernel adapters for specialised services like vMotion.

---
*This lab was completed as part of the 41891 Cloud Computing Infrastructure course.*
