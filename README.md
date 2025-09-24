# SAN Digital Twin: Software-Based Replica for Real-Time Failure Injection and Recovery Simulation

---

## Base Paper (Related Work)

**A Self-Healing and Fault-Tolerant Cloud-based Digital Twin Processing Management Model (SF-DTM)**  
*Deepika Saxena, Ashutosh Kumar Singh (2025)*  

This work proposes a model for digital twin processing in the cloud, emphasizing self-healing and fault tolerance, using federated learning and pattern analytics. While it doesn’t target SAN specifically, many of its methods are applicable (failure prediction, recovery, simulation).

---

## Abstract

Building resilient storage systems is critical in modern data centers, especially in Storage Area Network (SAN) environments where any failure can lead to severe data loss or downtime.  

In this paper, we present **SAN Digital Twin: Software-Based Replica for Real-Time Failure Injection and Recovery Simulation**, a framework designed to simulate SAN behavior under realistic workloads and inject failures dynamically to test recovery strategies.  

Leveraging virtualized SAN components, the twin monitors performance metrics such as throughput, latency, queue depths, and path availability in real time.  

Our novel contribution is integrating a **predictive failure module using machine learning** that identifies early indicators of impending SAN component failures (e.g., path failures, disk I/O degradation) and triggers automated recovery simulation, such as path failover, data re-striping, or rerouting before catastrophic failure.  

We evaluate our framework under multiple failure scenarios on synthetic and replayed SAN workloads. Results demonstrate that predictive failure detection reduces recovery time by up to **35%**, improves availability under failure by **20%**, and helps maintain performance (latency and throughput) significantly better compared to reactive recovery only.  

This **software-only digital twin framework** provides a test bed for SAN administrators and researchers to experiment with failure handling strategies, tune recovery policies, and understand trade-offs, without needing expensive hardware deployments.

---

## Key Novel Features

- **Predictive failure module**  
  Using ML to spot failing SAN components before they fail (instead of only reacting post-failure).

- **Real-time failure injection**  
  The twin supports injecting failures at runtime in various SAN components (paths, disks, storage nodes) in a virtualized/emulated environment.

- **Automated recovery simulation**  
  Once prediction or failure occurs, different recovery strategies are triggered automatically and compared (failover, mirrored path, data rebalancing/striping).

- **Performance metrics under workload**  
  Evaluate not just whether recovery “works”, but how much performance degrades (latency, throughput) and how fast it returns to “normal”.
