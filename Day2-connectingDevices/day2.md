# Lab 02 - Cabling and Connecting Network Devices

## Overview

Built a two-site network topology in Cisco Packet Tracer and connected every device using the correct cable type, based on device roles, port types, and link distances. Auto MDI-X was assumed disabled/unsupported, so cable type (straight-through vs. crossover) had to be chosen manually for each link.

**Sites:** Site A (R1/R2) and Site B (R3/R4)
**Includes:** 4 routers, 8 switches, 3 PCs, 1 server

## Objectives

* Connect all devices according to topology labels
* Select the correct cable type for each connection (copper straight-through, copper crossover, fiber)
* Apply correct reasoning for long-distance links (copper vs. fiber, single-mode vs. multi-mode)
* Practice manual cable selection with Auto MDI-X disabled

## Topology

<img width="1367" height="638" alt="Image" src="https://github.com/user-attachments/assets/53bb0e50-07ff-4d09-a07b-b5b73bdf7fbe" />

**Site A:** R1 → R2 → (SW1 → SW3 → PC1) and (SW2 → SW4 → PC2)
**Site B:** R3 → R4 → (SW5 → SW7 → PC3) and (SW6 → SW8 → SRV1)
**Inter-site link:** R1 ↔ R3 (3 km — fiber required, copper can't span this distance)
**Inter-router link:** R3 ↔ R4 (250 m — exceeds 100 m copper limit, fiber required)
**Local links:** R1↔R2 (50 m, copper), all router-switch and switch-PC/server links (copper, short distance)

## Cable Selection Logic

| Connection | Device Types | Distance | Cable Type |
|---|---|---|---|
| R1–R3 | Router–Router | 3 km | Fiber (single-mode, long-haul) |
| R3–R4 | Router–Router | 250 m | Fiber (multi-mode, short-haul) |
| R1–R2 | Router–Router | 50 m | Copper crossover |
| R2–SW1, R2–SW2, R4–SW5, R4–SW6 | Router–Switch | short | Copper straight-through |
| SW1–SW2, SW5–SW6 | Switch–Switch | short | Copper crossover |
| SW1–SW3, SW2–SW4, SW5–SW7, SW6–SW8 | Switch–Switch | short | Copper crossover |
| SW3–PC1, SW4–PC2, SW7–PC3, SW8–SRV1 | Switch–End device | short | Copper straight-through |

**Key reasoning:**
* **Like devices** (router-router, switch-switch) → crossover, since Auto MDI-X is off
* **Unlike devices** (router-switch, switch-PC/server) → straight-through
* **Distance > 100 m** → copper (UTP) is no longer viable; fiber required
* **3 km link** → single-mode fiber is the appropriate choice (long-distance, low signal loss)
* **250 m link** → multi-mode fiber is sufficient and more cost-effective at this range

## What I Learned

* How to determine straight-through vs. crossover cabling based on device type when Auto MDI-X isn't available
* Why copper (UTP) cabling has a 100-meter distance limitation
* The practical difference between single-mode and multi-mode fiber and when to use each
