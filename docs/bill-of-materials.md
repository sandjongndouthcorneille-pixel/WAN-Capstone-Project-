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
10. Clock Rate Configuration
11. Hardware Cost Estimation
12. Physical Installation Risks
13. Network Architecture Summary

## Acronyms Key

| Acronym | Meaning |
|---|---|
| WAN | Wide Area Network |
| LAN | Local Area Network |
| HQ | Headquarters |
| BoM | Bill of Materials |
| TBD | To Be Determined |
| SFP | Small Form-factor Pluggable |
| SMF | Single-Mode Fiber |
| MMF | Multi-Mode Fiber |
| Mbps | Megabits per second |
| DCE | Data Circuit-terminating Equipment |
| DTE | Data Terminal Equipment |
| RJ-45 | Registered Jack 45 |
| V.35 | Serial WAN Interface Standard |
| RS-232 | Recommended Standard 232 |
| LC | Lucent Connector |
| SFP-ZX | Long-range Gigabit Ethernet SFP transceiver |

## Site Information

| Site | Location | Users | Role |
|---|---|---:|---|
| HQ | Yaoundé | 500 | Headquarters and core banking servers |
| Branch A | Douala | 120 | Major commercial hub |
| Branch B | Buea | 60 | Regional office |
| Branch C | Garoua | 30 | Northern gateway |
| Branch D | Maroua | 15 | Remote presence |

## WAN Links

| Link | Distance |
|---|---:|
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

The router is the primary device responsible for connecting each Local Area Network (LAN) to the Wide Area Network (WAN).

Router models are selected according to:

- Number of users at each site.
- Required WAN throughput.
- Reliability requirements.
- Project budget constraints.
- Compatibility with Cisco Packet Tracer simulation.

| Site | Users | Recommended Router | Quantity | Justification |
|---|---:|---|---:|---|
| HQ (Yaoundé) | 500 | Cisco ISR 4331 | 1 | High-performance router suitable for the headquarters and core banking services. |
| Branch A (Douala) | 120 | Cisco ISR 4321 | 1 | Suitable for a larger branch with higher traffic requirements. |
| Branch B (Buea) | 60 | Cisco ISR 4321 | 1 | Suitable for a medium-sized regional office. |
| Branch C (Garoua) | 30 | Cisco ISR 2911 | 1 | Suitable for a smaller branch with moderate traffic requirements. |
| Branch D (Maroua) | 15 | Cisco ISR 1941 | 1 | Suitable for a smaller remote branch with lower traffic requirements. |

## SFP Transceivers

SFP (Small Form-factor Pluggable) transceivers provide the optical interface between compatible network equipment and fiber optic connections.

For this project, long-distance transmission between cities is provided through carrier network infrastructure. The bank-side equipment requires compatible long-range optical modules for connection to the carrier demarcation points.

The selected SFP-ZX modules are intended for the bank-side optical interfaces. They do not directly provide 200 km to 1000 km of transmission on their own. The carrier network provides the extended long-distance transport between cities.

| WAN Link | Distance | Recommended SFP | Quantity | Justification |
|---|---:|---|---:|---|
| HQ (Yaoundé) - Douala | 200 km | Cisco SFP-ZX | 2 | Provides the optical interface between the bank-side equipment and the carrier network. |
| HQ (Yaoundé) - Buea | 300 km | Cisco SFP-ZX | 2 | Provides a long-range optical interface using Single-Mode Fiber. |
| HQ (Yaoundé) - Garoua | 800 km | Cisco SFP-ZX | 2 | Used at the bank-side connection while the carrier network provides extended-distance transport. |
| HQ (Yaoundé) - Maroua | 1000 km | Cisco SFP-ZX | 2 | Used at the bank-side connection for the longest WAN service; the carrier network provides the extended transport. |

## Fiber Optic Cabling

Single-Mode Fiber (SMF) is selected for the WAN optical connections because it is suitable for long-distance optical communication.

Multi-Mode Fiber (MMF) was considered but was not selected because the project requires long-distance WAN connectivity.

The bank-side fiber connection uses LC connectors where compatible with the selected optical modules.

| WAN Link | Fiber Type | Connector | Justification |
|---|---|---|---|
| HQ (Yaoundé) - Douala | SMF | LC | Suitable for long-distance optical connectivity. |
| HQ (Yaoundé) - Buea | SMF | LC | Suitable for optical connectivity with the selected SFP modules. |
| HQ (Yaoundé) - Garoua | SMF | LC | Suitable for long-distance optical connectivity. |
| HQ (Yaoundé) - Maroua | SMF | LC | Selected for the longest WAN connection. |

## Copper Cabling

Copper Ethernet cabling is used for local connections between network devices and end devices within each site. It is not used for the long-distance WAN connections.

Serial cables are included only for the Cisco Packet Tracer demonstration.

| Cable Type | Purpose | Quantity | Justification |
|---|---|---:|---|
| RJ-45 Ethernet Cable | Connect routers, switches, and end devices | TBD | Required for internal LAN connectivity at the sites. |
| V.35 Serial Cable | Serial WAN connection between routers | 4 | Used only for WAN link simulation in Cisco Packet Tracer. |
| RS-232 Console Cable | Router configuration and troubleshooting | 1 | Used for router configuration during the Packet Tracer demonstration. |

## DCE/DTE Assignment

Each serial WAN connection in the Cisco Packet Tracer simulation requires one router to operate as the DCE (Data Circuit-terminating Equipment) and the other as the DTE (Data Terminal Equipment).

The DCE side provides the clock signal required for serial communication.

For this demonstration, the HQ router is assigned as the DCE side for all four serial WAN connections.

| WAN Link | DCE Device | DTE Device | Justification |
|---|---|---|---|
| HQ (Yaoundé) - Douala | HQ Router | Douala Router | HQ is assigned as the DCE side for the Packet Tracer simulation. |
| HQ (Yaoundé) - Buea | HQ Router | Buea Router | HQ is assigned as the DCE side for the Packet Tracer simulation. |
| HQ (Yaoundé) - Garoua | HQ Router | Garoua Router | HQ is assigned as the DCE side for the Packet Tracer simulation. |
| HQ (Yaoundé) - Maroua | HQ Router | Maroua Router | HQ is assigned as the DCE side for the Packet Tracer simulation. |

## Clock Rate Configuration

The clock rate provides synchronization for serial WAN communication in the Cisco Packet Tracer simulation.

The clock rate is configured only on the DCE side of each serial link.

In this WAN design, HQ (Yaoundé) is assigned as the DCE side for all four simulated WAN connections.

The 64,000 bps clock rate is used only for serial synchronization in the Packet Tracer demonstration. It does not represent the required real-world WAN throughput of 10 Mbps.

| WAN Link | DCE Device | Clock Rate | Purpose |
|---|---|---:|---|
| HQ (Yaoundé) - Douala | HQ Router | 64000 bps | Provides synchronization for the simulated serial WAN link. |
| HQ (Yaoundé) - Buea | HQ Router | 64000 bps | Provides synchronization for the simulated serial WAN link. |
| HQ (Yaoundé) - Garoua | HQ Router | 64000 bps | Provides synchronization for the simulated serial WAN link. |
| HQ (Yaoundé) - Maroua | HQ Router | 64000 bps | Provides synchronization for the simulated serial WAN link. |

## Hardware Cost Estimation

The hardware cost estimation provides an approximate budget analysis to verify that the proposed WAN design remains within the maximum project budget of $15,000 USD.

| Equipment | Site/Usage | Quantity | Estimated Unit Cost (USD) | Estimated Total Cost (USD) |
|---|---|---:|---:|---:|
| Cisco ISR 4331 Router | HQ (Yaoundé) | 1 | TBD | TBD |
| Cisco ISR 4321 Router | Douala and Buea | 2 | TBD | TBD |
| Cisco ISR 2911 Router | Garoua | 1 | TBD | TBD |
| Cisco ISR 1941 Router | Maroua | 1 | TBD | TBD |
| Cisco SFP-ZX Transceiver | WAN Links | 8 | TBD | TBD |
| Single-Mode Fiber Cable | WAN Connections | TBD | TBD | TBD |
| RJ-45 Ethernet Cable | LAN Connections | TBD | TBD | TBD |
| V.35 Serial Cable | WAN Simulation | 4 | TBD | TBD |
| RS-232 Console Cable | Router Configuration | 1 | TBD | TBD |
| **Estimated Total** | | | | **TBD** |

## Physical Installation Risks

| Risk | Impact |
|---|---|
| Fiber bend loss | Weak signal or link failure. |
| Dirty fiber connector | Signal interruption. |
| Wrong SFP type (MMF/SMF mismatch) | WAN connection failure. |
| Loose cable connection | Unstable connectivity. |
| Incorrect DCE/DTE cable assignment | Serial link synchronization failure. |

## Network Architecture Summary

The Meridian Bank WAN design connects the Headquarters in Yaoundé with four branch offices using a Hub-and-Spoke WAN topology and fiber-based WAN connectivity through carrier infrastructure.

For the Cisco Packet Tracer demonstration, the real number of users will be reduced to a smaller simulated environment while maintaining the same WAN topology and core routing, authentication, and connectivity principles.

| Site | Real Users | Demo Users |
|---|---:|---:|
| HQ (Yaoundé) | 500 | 50 |
| Douala | 120 | 12 |
| Buea | 60 | 6 |
| Garoua | 30 | 3 |
| Maroua | 15 | 2 |

The demonstration will preserve the same WAN topology and core network principles while using a reduced number of simulated users.

### Network Architecture Diagrams

<img width="1536" height="1024" alt="Meridian Bank WAN Architecture Diagram" src="https://github.com/user-attachments/assets/bdbb68c0-8436-41c4-903e-4b048a8e540d" />

<img width="1536" height="1024" alt="Meridian Bank Hub-and-Spoke WAN Topology" src="https://github.com/user-attachments/assets/65415899-7994-4774-821b-c7340d6ff8a3" />

### Equipment Reference Images

The following images provide visual references for the main network equipment and cabling specified in the Meridian Bank WAN design.

#### 1. Cisco ISR Routers

The Cisco ISR routers provide WAN connectivity at the Headquarters and branch offices.

**Models used:**
- Cisco ISR 4331 – HQ (Yaoundé)
- Cisco ISR 4321 – Douala
- Cisco ISR 4321 – Buea
- Cisco ISR 2911 – Garoua
- Cisco ISR 1941 – Maroua

<img width="728" height="366" alt="Cisco ISR Router" src="https://github.com/user-attachments/assets/6d8ca7f5-c683-4446-af7d-fef1658148ba" />

#### 2. Cisco SFP-ZX Transceivers

Cisco SFP-ZX transceivers provide the optical interface for long-distance Single-Mode Fiber connectivity through the carrier network.

<img width="554" height="554" alt="Cisco SFP-ZX Transceiver" src="https://github.com/user-attachments/assets/4c0ce921-784e-4608-9c70-3d7ecdd4c229" />

#### 3. Single-Mode Fiber (SMF)

Single-Mode Fiber is used for the long-distance WAN connections. LC connectors are specified for the bank-side fiber connections.

<img width="400" height="400" alt="Single-Mode Fiber" src="https://github.com/user-attachments/assets/042ded3a-0b81-4677-ac01-a37e1904715a" />

#### 4. Copper Ethernet Cabling

Copper Ethernet cabling is used for local connections between network devices within each site. It is not used for the long-distance WAN links.

<img width="447" height="447" alt="Copper Ethernet Cable" src="https://github.com/user-attachments/assets/2d42b401-3dc5-401d-aa19-d9baeb90c6ff" />

<img width="447" height="447" alt="RJ-45 Ethernet Cable" src="https://github.com/user-attachments/assets/473f69d5-6c68-4b81-b5f0-9eae3a0176f4" />provide the optical interface for long-distance Single-Mode Fiber connectivity.

**Image:**
<img width="554" height="554" alt="téléchargement (5)" src="https://github.com/user-attachments/assets/4c0ce921-784e-4608-9c70-3d7ecdd4c229" />


---

#### 3. Single-Mode Fiber (SMF)

Single-Mode Fiber is used for the long-distance WAN connections. LC connectors are specified for the fiber connections.

**Image:**
<img width="400" height="400" alt="téléchargement (6)" src="https://github.com/user-attachments/assets/042ded3a-0b81-4677-ac01-a37e1904715a" />


---

#### 4. Copper Ethernet Cabling

Copper Ethernet cabling is used for local connections between network devices within each site. It is not used for the long-distance WAN links.

**Image:**
<img width="447" height="447" alt="images (8)" src="https://github.com/user-attachments/assets/2d42b401-3dc5-401d-aa19-d9baeb90c6ff" />
<img width="447" height="447" alt="images (9)" src="https://github.com/user-attachments/assets/473f69d5-6c68-4b81-b5f0-9eae3a0176f4" />

