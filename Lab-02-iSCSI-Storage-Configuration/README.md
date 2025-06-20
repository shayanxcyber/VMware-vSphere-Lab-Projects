# Lab 2: iSCSI Shared Storage Configuration

### Objective
This lab focused on configuring shared storage for the ESXi hosts. The objective was to move beyond local datastores by connecting two ESXi hosts to a central iSCSI target, a foundational step for advanced features like vMotion and High Availability.

### Key Activities Performed

1.  **iSCSI Target Preparation:**
    *   Verified the network configuration of a pre-configured FreeNAS VM acting as the iSCSI target.
2.  **iSCSI Initiator Configuration:**
    *   On each of the two ESXi hosts, configured the software iSCSI adapter.
    *   Added the IP address of the FreeNAS iSCSI server to the 'Dynamic targets' section of the initiator.
    *   Rescanned the storage adapter, which allowed the ESXi hosts to discover the new iSCSI LUNs (Logical Unit Numbers).
3.  **Datastore Creation:**
    *   Navigated to the 'Storage' section in the vSphere client and confirmed the new iSCSI disk device was visible.
    *   Created a new VMFS (Virtual Machine File System) datastore on the newly discovered iSCSI disk.
    *   Verified that this new shared datastore was accessible from both ESXi hosts simultaneously.

### Core Concepts & Skills Demonstrated

*   **Storage Area Networks (SAN):** Practical understanding of how block-level storage is shared over an IP network using the iSCSI protocol.
*   **iSCSI Configuration:** Hands-on experience configuring both iSCSI targets (server-side) and initiators (client-side on ESXi).
*   **VMFS Datastores:** Knowledge of VMware's clustered file system and how to create datastores on shared storage devices.
*   **Infrastructure for Scalability:** Demonstrated the ability to set up shared infrastructure, which is a prerequisite for clustering, resource pooling, and live migration.

---
*This lab was completed as part of the 41891 Cloud Computing Infrastructure course.*
