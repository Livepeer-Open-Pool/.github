# Open Pool: A Public Decentralized Compute Pool for Livepeer

Welcome to **Open Pool**, a public decentralized compute pool specifically built to expand the capacity of the [Livepeer](https://livepeer.org/) network. Open Pool allows **Livepeer Orchestrators** to easily aggregate GPU resources from external **Workers**, thereby offering more scalable video transcoding and AI inference services.

Below is a detailed overview of Open Pool—how it works, who it benefits, and how you can get involved.

---

## Table of Contents
1. [Introduction](#introduction)  
2. [Why Open Pool?](#why-open-pool)  
3. [Key Features & Benefits](#key-features--benefits)  
4. [Business Model & Incentives](#business-model--incentives)  
5. [Performance & Benchmarking](#performance--benchmarking)  
6. [Onboarding Guide](#onboarding-guide)  
   - [For Orchestrators](#for-orchestrators)  
   - [For Workers](#for-workers)  
   - [For Delegators](#for-delegators)  
7. [Use Cases: Beyond Transcoding](#use-cases-beyond-transcoding)  
8. [Future Plans](#future-plans)  
9. [Conclusion](#conclusion)

---

## Introduction

Livepeer is a decentralized video transcoding and streaming platform that leverages a network of **up to 100 active Orchestrators** at any given time. Each Orchestrator stakes or receives staked **LPT (Livepeer Token)**, processes transcoding requests, and earns rewards plus fees.

**Open Pool** was created to solve a critical need: **scaling**. Since there’s a cap of 100 Orchestrators, each one must be able to handle increasingly large volumes of transcoding and AI inference work. This is where Open Pool steps in:

- **Orchestrators** can **invite external GPU Workers** to join their pool.  
- **Workers** can easily plug their GPU into the Livepeer network without needing to set up a full Orchestrator node.  
- **Delegators** can stake their LPT on an Orchestrator that’s part of Open Pool, effectively supporting the growth and decentralization of the entire network.

---

## Why Open Pool?

1. **Scalability**: Livepeer is poised for massive growth. By pooling GPUs, one Orchestrator can accommodate 10x or 100x more compute than they could on their own.  
2. **Decentralization**: More independent workers = less reliance on a few “super operators,” making Livepeer more resilient to failures or attacks.  
3. **Earn Rewards & Fees**:  
   - **Workers** earn a share of transcoding fees for their GPU power.  
   - **Orchestrators** can expand their capacity (and revenue) without owning every GPU.  
   - **Delegators** can stake their LPT on Orchestrators contributing to a stronger, more scalable network.  
4. **Simplified Management**: Open Pool provides out-of-the-box solutions for:  
   - Dashboards and metrics  
   - Fee sharing  
   - Event logs and data pipelines  

---

## Key Features & Benefits

1. **Open Source & Customizable**  
   - **Open Pool** is fully open source, allowing anyone to deploy a pool—public or private.  
   - Hooks enable **custom revenue-sharing** logic or feature extensions.

2. **Transparent Dashboard & Metrics**  
   - An **event log** records all Orchestrator and Worker activities.  
   - Operators can generate real-time dashboards showing earnings, job counts, and performance.

3. **Flexible Fee Sharing**  
   - **Default setting**: 25% commission for the pool, 75% payout to Workers.  
   - This can be **reconfigured** easily in a YAML file or environment variable.

4. **AI Inference Ready**  
   - From **speech-to-text**, **image recognition**, **content moderation**, to **large language models**, the platform can handle GPU-intensive AI tasks.  
   - Helps Livepeer move **beyond video transcoding** into a general-purpose decentralized compute marketplace.

5. **Worker Performance Tracking**  
   - Response times, transcoding speed, and real-time ratios are tracked.  
   - Underperforming or malicious Workers can be deprioritized or removed.

---

## Business Model & Incentives

### How Orchestrators Earn

1. **Inflationary LPT Rewards**: Livepeer mints LPT tokens that are distributed to Orchestrators (and their Delegators).  
2. **Transcoding Fees**: Paid in ETH or another token, based on actual jobs processed.

Orchestrators can set:  
- **Reward Cut**: The share of LPT inflation they retain versus distribute to Delegators.  
- **Fee Cut**: The percentage of transcoding fees they keep before paying Workers.

### How Workers Earn

- **Transcoding Fees**: By default, 75% of transcoding fees go to Workers, with a 25% pool commission.  
- In the future, Orchestrators can customize to share **LPT rewards** as well, incentivizing Worker loyalty.

### For Delegators

- **Stake LPT** on an Orchestrator running Open Pool to help them scale.  
- Earn a portion of inflationary LPT (minus the Orchestrator’s reward cut).  
- Support a more **resilient** and **scalable** Livepeer infrastructure.

---

## Performance & Benchmarking

- **Event-Log-Based Metrics**: Every job’s performance (e.g., real-time ratio, response time) is recorded.  
- **Dashboards & Alerts**: Run your own monitoring tools (like Grafana) to spot anomalies or track historical data.  
- **Fair Work Distribution**: High-performing Workers get prioritized for future tasks, incentivizing good behavior and hardware maintenance.

---

## Onboarding Guide

### For Orchestrators

1. **Deploy Open Pool**:  
   - Clone the repository and follow the documentation to set up your Orchestrator node with the Open Pool software.  
   - Configure your commission rate and decide whether (and how) you want to share LPT rewards.

2. **Connect Workers**:  
   - Publicly advertise your pool so Workers know how to join, or keep it private if you want a curated group.

3. **Monitor & Scale**:  
   - Use the dashboard to track job throughput, Worker performance, and earnings.

### For Workers

1. **Prepare Your GPU Environment**:  
   - **NVIDIA**: Install CUDA, cuDNN, and drivers as needed.  
   - **Other GPUs**: Follow recommended drivers or open-source libraries for compatibility.

2. **Run the Open Pool Worker**:  
   - Initial versions may require manual installation.  
   - **(Upcoming)**: A Docker container will simplify setup by bundling drivers/libraries.

3. **Start Earning**:  
   - Your Worker node will receive jobs from the Orchestrator.  
   - Monitor your payouts in the pool’s dashboard.

### For Delegators

1. **Stake Your LPT**:  
   - Delegate LPT to an Orchestrator node running Open Pool.  
2. **Earn Inflationary Rewards**:  
   - Receive a share of the newly minted LPT minus the reward cut set by the Orchestrator.  
3. **Contribute to Scalability**:  
   - By delegating to pools, you help ensure the network can handle more transcoding and AI tasks.

---

## Use Cases: Beyond Transcoding

Open Pool is not limited to video transcoding. It supports **GPU-intensive AI workloads**, such as:

- **Text-to-Speech** & **Speech-to-Text**  
- **Image-to-Text** (OCR) & **Image Segmentation**  
- **Object Detection** & **Content Moderation**  
- **Large Language Model (LLM) Inference**  
- **Real-Time Video Analysis**

As demand for AI solutions grows, Open Pool enables Orchestrators to seamlessly scale their GPU capacity without spinning up separate infrastructure.

---

## Future Plans

- **Dockerized Onboarding**: Simplify Worker setup via a pre-configured container.  
- **Optional LPT Payouts**: Allow Orchestrators to swap ETH fees for LPT and pay Workers directly in LPT.  
- **Automated Provisioning**: Provide scripts or CLI tools to automate driver checks, system configurations, etc.  
- **Community-Driven Enhancements**: Invite the Livepeer community to contribute new features, bug fixes, or custom revenue-sharing logic.

---

## Conclusion

**Open Pool** is your gateway to a more scalable, decentralized, and AI-ready Livepeer network. By uniting Orchestrators, Workers, and Delegators under a flexible, open-source framework, it unlocks new possibilities for:

- **Massive GPU scaling** beyond the 100-orchestrator limit.  
- **Transparent revenue sharing** and performance tracking.  
- **Diverse AI workloads** handled alongside video transcoding.

If you’re an **Orchestrator** seeking to expand your capacity, a **Worker** ready to monetize your GPU, or a **Delegator** looking to support the network’s growth, Open Pool offers the tools, transparency, and incentives to make it happen.

Join us in building the next phase of Livepeer’s decentralized compute future!
