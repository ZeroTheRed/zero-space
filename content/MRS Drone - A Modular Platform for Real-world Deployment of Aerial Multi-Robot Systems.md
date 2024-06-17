*Multi-Robot System (MRS)* drone 

**Modularity** - Changes in sensors, frames, and actuator configurations

### Requirements
- Simultaneous *agility*, *robustness*, and *modularity* (*ARM*)
	- Modularity -- *Adaptability* to different applications and payloads
- Sufficient *flight time duration* to execute complex and lengthy tasks
- Ability to *process computationally expensive algorithms* <- High *compute power* 

### Hiccups
- Long design times
- High manufacturing costs
- Difficulty in maintenance
- Real robot experiments experience many collisions 

| Drone Platform                                    | Limitations                    |
| ------------------------------------------------- | ------------------------------ |
| **ASL** (ETH Zurich)<br>**FLA** (GRASP + UZurich) | High weight and low agility    |
| **Crazyflie**                                     | Poor compute power and sensing |
| Platforms from MIT and GRASP                      | Closed source                  |
>[!Info]
>A lot of the UAV platforms and systems being researched at in Universities and R&D firms have never been tested and deployed in the real world

### Features of the MRS Drone
- Modular hardware construction
- Open source software
- Plugin-based architecture
- High compute power
- Strong autonomous capabilities

- **Open-source platforms** for *research institutions and start-ups*
	- Lowering initial development costs
	- Promoting collaboration 

### Frames and Propulsion
**Frame** --> *Size of UAV*, *Max diameter of propellers* -> Payload type, UAV endurance, max thrust, max payload capacity
**Larger propeller at slower spin speed > Slower propeller at faster spin speed** (Greater thrust achieved by accelerating a larger mass of air by a smaller amount). Larger propellers are *more efficient* and deliver *more thrust*

**Tradeoff**
*Smaller UAVs* -> Easier to operate and navigate in crowded areas
*Larger UAVs* -> Longer flight times and greater payload capacities
MRS Drone provides 3 basic frame sets

| Frame materials used                                     | Features                       |
| -------------------------------------------------------- | ------------------------------ |
| Arms - **Plastic**                                       | Cheap                          |
| Arms - **Carbon Fiber**                                  |                                |
| Centre Frame - **glass Reinforced Epoxy Laminate (REL)** |                                |
| Centre Frame - **Carbon Fiber**                          | Great stiffness<br>Lightweight |

**Dronument Project** - High-payload *coaxial octocopter*
- **What are the using it for?** - Autonomous inspection of historical buildings
- **Payload**
	- Regular-size camera with dual-axis gimbal stabilization
	- Hi-res LiDAR
	- Ultrasonic sensors
	- Carbon fiber safety cage for payload protection
- **Propulsion** - Coaxial

**Prototype Drone Hunter**
- Octocopter with Tarot T18 frame
- 18-in propellers and 10 kg payload capacity
- Ouster LiDAR, Reach RTK (Real-Time Kinematic) module
- Folding net to capture and carry drones
- Carbon Fiber and CNC-machined aluminium platform

Attach modular and easily replaceable legs/extensions to drones that can function as shock absorbers and take in kinetic damage to protect the drone

Payload-computer communication interfaces can cause interference to GNSS signals. Appropriate shielding may be required

| Type                | Model                                                    |
| ------------------- | -------------------------------------------------------- |
| **Rangefinder**     | Garmin LiDAR Lite V3<br>MB1340 MaxBotix Ultrasound       |
| **Planar LiDAR**    | RPLiDAR A3<br>                                           |
| **3D LiDAR**        | Ouster OS1 and OS0 series<br>Velodyne VLP16              |
| **Cameras**         | Basler Dart daA1600<br>Bluefox MLC200w (grey or RGB)<br> |
| **RGB-D Cameras**   | Intel RealSense D435i and D455                           |
| **GNSS**            | NEO-M8N<br>RTK Emlid Reach M2                            |
| **Thermal Cameras** | FLIR Lepton<br>FLIR Boson                                |
| **Pixhawk Sensors** | Gyroscopes<br>Barometers<br>Accelerometers               |
| **IMU**             | ICM-42688                                                |
| **UVDAR**           |                                                          |
MRS Drone employs *sensor fusion*

UVDAR is used to offset the degraded performance of computer vision (CV) systems to locate other swarm drones in order to fly and coordinate with each other. This is useful in outdoor environments with variable and unfavourable illumination and is more computationally simple than traditional CV systems

Attaching UV LEDs to drones that are part of a swarm is greatly tested and proven to be effective in identifying drones and ensuring mutual localization driven by UV light detection 

**Current research:** Improving the communication range and bit rate of UVDAR-COM systems and enabling the utilization of known measurement error covariances for increased reliability and sensor-based cooperative behaviour

Adding more ducting to a ducted fan propeller system reduces thrust by 20%
The ducted fan configuration retains the lone propeller's thrust power while reducing current draw by 5%
**Future testing**: Coaxial propeller testing

Modularity means that electronic interfaces must be present in a modular drone to allow the integration of various payloads
PCBs can also double as structural members apart from integrating additional electronics and distributing power 

![[Pasted image 20240530200658.png]]
FT4232H - USB-to-quad serial converter

### MRS UAV System
The software for controlling and deploying multi-rotor UAVs