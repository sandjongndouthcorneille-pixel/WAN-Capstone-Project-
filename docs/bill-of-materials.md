# Bill of Materials (BoM)

## Project
Meridian Bank WAN Design

## Description
This document contains the list of required network equipment and resources for the Meridian Bank WAN design project.

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
