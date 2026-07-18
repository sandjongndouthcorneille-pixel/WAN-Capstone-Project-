# Bill of Materials (BoM)

## Project
Meridian Bank WAN Design

## Description
This document contains the list of required network equipment and resources for the Meridian Bank WAN design project.

## Table of Contents

1. Acronyms Key
2. Site Information
3. WAN Links
4. Project Requirements
5. Router Equipment
6. SFP Transceivers
7. Fiber Optic Cabling
8. Copper Cabling
9. DCE/DTE Assignment
10.Clock Rate Configuration
11. Hardware Cost Estimation
12. Physical Installation Risks
13. Network Architecture Summary

## Acronyms Key


## Site Information

| Site | Location | Users | Role |
|---|---|---|---|
| HQ | Yaoundé | 500 | Headquarters and core banking servers |
| Branch A | Douala | 120 | Major commercial hub |
| Branch B | Buea | 60 | Regional office |
| Branch C | Garoua | 30 | Northern gateway |
| Branch D | Maroua | 15 | Remote presence |

## WAN Links

| Link | Distance |
|---|---|
| HQ - Douala | 200 km |
| HQ - Buea | 300 km |
| HQ - Garoua | 800 km |
| HQ - Maroua | 1000 km |

## Project Requirements

| Requirement | Description |
|---|---|
| Network Type | Wide Area Network (WAN) connecting HQ and four branch offices |
| Sites | HQ (Yaoundé), Douala, Buea, Garoua, and Maroua |
| Minimum Throughput | Minimum 10 Mbps required for all branch connections |
| Hardware Budget | Maximum hardware budget of $15,000 USD |
| Authentication | Layer 2 authentication using CHAP |
| Longest WAN Link | HQ (Yaoundé) - Maroua: 1000 km |
| Availability Requirement | HQ uptime target: 99.999% |

## Router Equipment

The router is the primary device responsible for connecting each Local Area Network (LAN) to the Wide Area Network (WAN).Router models are selected according to:
- Number of users at each site.
- Required WAN throughput.
- Reliability requirements.
- Project budget constraints.
- Compatibility with Cisco Packet Tracer simulation.

| Site | Users | Recommended Router | Quantity | Justification |
|---|---:|---|---:|---|
| HQ (Yaoundé) | 500 | Cisco ISR 4331 | 1 | High-performance router required for headquarters and core banking services. |
| Branch A (Douala) | 120 | Cisco ISR 4321 | 1 | Supports a large commercial branch with higher traffic requirements. |
| Branch B (Buea) | 60 | Cisco ISR 4321 | 1 | Suitable for a medium-sized regional office with reliable WAN connectivity. |
| Branch C (Garoua) | 30 | Cisco ISR 2911 | 1 | Suitable for a smaller branch office with moderate traffic requirements. |
| Branch D (Maroua) | 15 | Cisco ISR 1941 | 1 | Cost-effective router suitable for a remote branch with lower traffic needs. |
