**Date:** 12-06-2024 18-42
**Tags:** #wiki/aero/air  
**Uplink:** [[Drone Applications]]

# Uber Eats - VOXL

In 2019, Uber Eats completed their first **successful food delivery using a drone**. They partnered with **ModalAI** to use **VOXL**, their **lightweight computing platform with 4G connectivity**. VOXL helped to keep the drone on a **safe flight path even out of pilot's LoS**

**Cell Connectivity** is a reliable technology for **BVLOS drone flights** (Beyond Visual Line Of Sight)

#### VOXL
* Computing and communications platform that creates **integrated and machine-vision based autonomous navigation maps** for **indoor and outdoor robots**
* Does **not** require **GPS** to run
* Uses **SLAM** for mapping
* Uses **Snapdragon CPUs**
* Supports **4 cameras** using the **MIPI** interface


#### Method of Operation
```mermaid
flowchart LR
	A["Uber Elevate Cloud Services"] --- B["VOXL"]
	B["VOXL"] --- C["Delivery Drone"]
```
**Uber Elevate Cloud Services** - *Airspace management system* for *tracking and guiding drones*
**VOXL** - Command and Control of the drone + Autonomous navigation + Air traffic monitoring using *Automatic Dependent Surveillance-Broadcast (ADS-B)*

### External Links
- https://www.prweb.com/releases/voxl_from_modalai_contributes_to_uber_eats_drone_delivery_testing/prweb16466809.htm
- https://www.therobotreport.com/voxl-modalai-helps-uber-eats-test-drone-delivery-food/
