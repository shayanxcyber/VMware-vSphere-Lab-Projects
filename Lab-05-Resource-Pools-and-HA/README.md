# Lab 5: vSphere Clusters, Resource Pools, and High Availability (HA)

### Objective
This lab focused on aggregating host resources and providing automated failover protection. The goals were to create a vSphere Cluster, manage resources with Resource Pools, and configure vSphere High Availability (HA) to automatically restart VMs in the event of a host failure.

### Key Activities Performed

1.  **Cluster Creation:**
    *   Created a new Cluster object in vCenter called `YourName-Cluster`.
    *   Dragged and dropped the two managed ESXi hosts into the cluster, pooling their CPU and memory resources.
2.  **Resource Pool Configuration:**
    *   Within the cluster, created two Resource Pools: 'Fast' (with High share values) and 'Slow' (with Low share values and a 500Mhz CPU limit).
    *   Placed one VM in each pool to observe how resource allocation policies affect performance under contention.
    *   Ran a CPU-intensive script (`cpubusy.sh`) on both VMs to demonstrate that the VM in the 'Fast' pool received more CPU resources.
3.  **vSphere HA Configuration:**
    *   Enabled vSphere HA on the cluster.
    *   Configured HA settings, including setting Heartbeat Datastores to be automatically selected.
4.  **Host Failure Simulation:**
    *   Identified the Master and Slave hosts in the HA cluster.
    *   Simulated a host failure by abruptly powering off the Slave host that was running a VM.
    *   Observed in vCenter as vSphere HA detected the failure, and automatically powered on the affected VM on the surviving Master host, demonstrating successful failover.

### Core Concepts & Skills Demonstrated

*   **vSphere Clustering:** Ability to create and manage a cluster to aggregate compute resources.
*   **Resource Management:** Hands-on experience with Resource Pools, Shares, and Limits to guarantee service levels and manage resource contention.
*   **High Availability (HA):** Deep understanding and practical configuration of automated failover for virtual machines, a critical component of business continuity.
*   **Fault Tolerance Concepts:** Demonstrated the ability to design and test a system that can withstand a hardware failure with minimal service disruption.

---
*This lab was completed as part of the 41891 Cloud Computing Infrastructure course.*
