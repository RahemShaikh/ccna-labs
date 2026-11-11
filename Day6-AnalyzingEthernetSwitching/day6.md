# Lab 06 - Ethernet LAN Switching

## Overview

Populating ARP and MAC Address tables with the ping command

**Includes:** 2 switches, 4 PCs

## Objectives

* Ping PCs with empty ARP/MAC tables
* Use ping to generate traffic
* Examine ARP/MAC tables
* Clear MAC table entries
  
## Topology

<img width="722" height="395" alt="image" src="https://github.com/user-attachments/assets/a60c9ad8-9ff3-4998-980f-b17a5f64d02c" />

## Simuation Mode ping command PC1 -> PC3

<img width="1432" height="1044" alt="image" src="https://github.com/user-attachments/assets/9c765d42-af25-423a-89f6-532122f5fc30" />

## Populated MAC Address Table of Switch 1

<img width="827" height="379" alt="image" src="https://github.com/user-attachments/assets/e8289b30-72a1-4b77-8c04-9c5f6fff8e43" />

## Clearing MAC Address Table of Switch 1

<img width="549" height="233" alt="image" src="https://github.com/user-attachments/assets/6ea5c17d-a54a-4200-bbda-4a757593aa54" />

## Commands Used

* ```ping```: Send ICMP packets to targeted IP Address      
* ```show mac address-table```: Shows the MAC Address table on a switch
* ```clear mac address-table dynamic```: Clear all dynamically filled entries in the MAC Address Table

## What I Learned

* ARP maps IP to MAC Address
* When PC1 pings PC3 for the first time, ICMP packets are buffered for ARP packets
* Switches learn the MAC address from the source MAC Address
