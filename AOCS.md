**Date:** 12-06-2024 00-51
**Tags:** #wiki/aero/sat 
**Uplink:** [[MOC - Satellites]]

# AOCS

**AOCS** - Attitude and Orbit Control Systems

> [!info]
> **Attitude** - Orientation of the satellite 

The **attitude** and **orbit** are controlled by a **system of actuators, sensors, and software**.  The AOCS has **3-axis stabilized Earth-pointing attitude control**[^1] and **orbit control** for which the needed **thrust impulses** are provided by the **propulsion system**
#### System Components of GRACE-FO 
1. **Fluxgate magnetometer** - Provides *coarse attitude* based on satellite's *position* and a model of Earth's magnetic field
2. **GPS receiver** - For *determining the position* of the two satellites. It measures the *change in position of the satellites* w.r.t the position of GPS satellites. Each satellite has *3 antennas*[^1]
	1. For collecting *navigation data*
	2. For collecting *atmospheric occultation data*
	3. For *backup navigation*
3. **Star tracker assembly** - *Transformation* of science data to *inertial references*. It precisely calculates the orientation of each satellite by *measuring its relative position w.r.t stars*. It has *3 redundant star tracker heads*. [^1] - The STA provides <span style="color:lime">absolute orientation</span> based on star positions
5. **High-performance gyro package** - *Attitude rates* during spacecraft *emergency modes*. The gyro provides <span style="color:lime">rate of rotation</span> of the satellite
6. **Coarse Earth and Sun sensor** - *Coarse attitude* determination. This provides a <span style="color:lime">faster and rougher attitude updates than the STA</span> for *initial attitude acquisition* and *redundancy*
7. IMU
8. Magnetic torquers
9. **Cold gas propulsion system** - Provides *thrust impulses for orbit control*

### AOCS Architecture

![[Pasted image 20240515170437.png]]
<span style="color:royalblue">Source: ESA</span> [^2]

1. **Attitude Measurement Assembly**
	1. <span style="color:aquamarine">Digital Earth Sensor</span> (STD) - Roll and Pitch
	2. <span style="color:aquamarine">Digital Sun Sensor</span> (SSD) - Yaw
	3. <span style="color:aquamarine">4 independent 2-axis gyros</span> (GYROS) - For *rate of rotation*
2. **Wheels and Magnetotorquer Assembly**
	1. <span style="color:aquamarine">Three 40 Nm reaction wheels</span> (RW) - For *torque control*
	2. <span style="color:aquamarine">2 magnetotorquers </span>(MAC) - For *torque generation*
	3. <span style="color:aquamarine">Monitoring and Command Unit</span> (EAIM) 
3. **Propulsion and Solar Array Drive Mechanism (SADM) Assembly**
	1. <span style="color:aquamarine">4 pressurized tanks in blow-down mode</span> - Each contains 300 kg of Hydrazine
	2. <span style="color:aquamarine">2 branches of eight 23.5 N thrusters</span> located on SVM
4. **Safe Mode Assembly**
	1. <span style="color:aquamarine">Safe mode dedicated electronics unit</span> (T4S)
	2. <span style="color:aquamarine">Sun Acquisition Sensors</span> (SAS)
	3. <span style="color:aquamarine">Safe mode software</span>
5. **OBDH (On-Board Data Handling) Bus**[^4]

>[!info]
>**Blow-down mode** - In propulsion systems using Hydrazine (for example), the pressurant gas is pumped into the same bladder tank that contains the propellant. The pressurant "blows down" or forces the propellant into a perforated axial stand-pipe that's present in the tank, thus causing propulsion. It's simple and reliable[^3]

 
[^1]: https://gracefo.jpl.nasa.gov/attitude-and-orbit-control-system/
[^2]: https://www.esa.int/Applications/Observing_the_Earth/Meteorological_missions/MetOp/Attitude_and_orbit_control
[^3]: https://www.space-propulsion.com/spacecraft-propulsion/hydrazine-tanks/hydrazine-tank-overview.html
[^4]: https://www.esa.int/Enabling_Support/Space_Engineering_Technology/Microelectronics/OBDH