# Lab 06 - Configuring IP Addresses

## Overview

Configure IP Addresses on Router and PCs 

**Includes:** 3 switches, 3 PCs, 1 router
**Sites:** Site A (15.0.0.0/8), Site B (201.191.20.0/24), Site C (182.98.0.0/16)

## Objectives

* View the router interfaces
* Configure router interfaces
* Configure PC IP addresses
  
## Topology

<img width="719" height="499" alt="image" src="https://github.com/user-attachments/assets/6db3c829-2464-408b-b0ab-fe7cf9fad289" />

## Displaying Unconfigured IP Interface Table of R1

<img width="983" height="209" alt="image" src="https://github.com/user-attachments/assets/75b66928-36a3-48ea-84d9-b40c2928a1a7" />

## Configuring Router  Interfaces with IP Addresses

<img width="1088" height="685" alt="image" src="https://github.com/user-attachments/assets/c2d25128-cccd-42e5-b7a2-f26d56be35a6" />

## Displaying Configured IP Interface Table of R1

<img width="974" height="142" alt="image" src="https://github.com/user-attachments/assets/58d41568-2a3e-41a7-bb12-78ff79ae8cad" />

## Pinging PC2 and PC3 from PC1 Connectivity Test

<img width="712" height="643" alt="image" src="https://github.com/user-attachments/assets/ec075ad4-8c44-44c5-9170-a70eab8ece45" />

## Commands Used

* ```hostname```: Rename generic router to R1  
* ```show ip interface brief```: Display the IP Table 
* ```interface```: Switch to the specified interface for configuration 
* ```ip address```: Manually make an entry of the ip address and subnet mask
* ```description```: Add comments to a specific interface
* ```no shutdown```: Enable an interface
* ```write```: Save the running config
* ```ping```: Connectivity test

## What I Learned

* You can switch to another interface without having to go back to global config mode
* Router interfaces are administratively shutdown by default and must be enabled using no shutdown
* The ```show ip interface brief``` command provides a quick overview of interface IP addresses and their operational status.

