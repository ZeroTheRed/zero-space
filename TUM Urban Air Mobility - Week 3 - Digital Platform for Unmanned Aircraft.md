**Date:** 12-06-2024 14-44
**Tags:** #wiki/aero/air 
**Uplink:** [[TUM Urban Air Mobility - Week 3]]

# TUM Urban Air Mobility - Week 3 - Digital Platform for Unmanned Aircraft
[dipul](www.dipul.de) - Unmanned Aviation digital platform 

| What information does it provide?                                                                                             | For whom?                                 | What tools are provided?                 |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- | --------------------------------------- |
| Category of drone operations<br>Safety recommendations<br>How to register as an operator<br>Legal basis<br>Geographical zones | Federal and National aviation authorities Map tools for geographical zones (+WMS) s  |
- Identify locations A and B on www.dipul.de (use the address field)
- Measure the distance between A and B using the external tool www.geoportal.de/map.html
	- **1.9 km** 
- How many different coloured geo-zones are there between A and B? **6 zones** or **41 zones**
- Calculate the distance between A and B (orthodrome $R_m$ = 6371 km) - This is the middle Earth radius

>[!Definition]
>An **orthodrome** or a great circle is the intersection formed by a sphere and a plane. The arc of an orthodrome is the shortest distance travelled on a sphere between two points

**Answer**
Both locations A and B are in Flatowallee 28 and Harbigstraße 34 respectively, both of them being falling under restricted geographical zones. The distance measured between A and B in geoportal.de is roughly 1.9 km. There happen to be 41 geographical zones between both the locations when drawing a circle 
The calculated distance is 9 km

### My procedure
- The identification of locations is already done for me, the coordinates are given to me anyways - Flatowallee 28 (52° 30′ 43″ N 13° 14′ 27″ E) and Harbigstraße 34 (52° 30′ 01″ N 13° 15′ 38″ E)
- I went to geoportal.de/map.html and measured the distance. I had to go to Tools and select the "Measure distance" tool, which helps me draw a line between the two points whose distance I want to measure. It was a bit wonky as I couldn't easily place two points on the map so I had to switch points while the line was being drawn but I got the distance between A and B as 1.9 km
- I went back to dipul and drew a circle between A and B and I counted the total number of geographic zones that showed up. Earlier, I got 41 zones but upon repeating the process, I'm getting 32 zones? Odd, am I making a mistake somewhere?
![[Dipul Geographic Zones in Circle.png]]
* To calculate the great circle distance/arc length/orthodromic distance, I had to refer to Wikipedia for the formula and here it is
$$\Delta\sigma = \arccos(\sin\phi_1\sin\phi_2 +\cos\phi_1\cos\phi_2\cos\Delta\lambda) $$
$$d = R_m\Delta\sigma$$
$(\lambda_1, \phi_1)$, $(\lambda_2, \phi_2)$ -- Latitude Longitude coordinate pairs of A(1) and B(2) in degrees 
$\Delta\lambda$ -- Absolute difference of latitudes (degrees)
$\Delta\phi$ -- Absolute difference of longitudes (degrees)
$\Delta\sigma$ -- Central angle (degrees)
$R_m$ -- Mean Earth radius (km)
$d$ -- Arc length/great circle distance/orthodromic distance (km)

Using the formulae, I arrived at $d$ = **9 km**
I find it strange that the arc length isn't matching with the distance I measured before (1.9 km). Is there a conceptual misunderstanding?

### The answer
So, on geoportal.de, one of the points was already marked. How was that possible? I suppose there's either some tool I missed or they had imported the data from Dipul's map tool over directly. Either way, the correct answer is **1.861 km**. Quite close to mine!

I was extremely wrong with the geographical zone count. The actual number of zones between A and B is just **2** 
![[Dipul Geographic Zones - Actual Count.png]]
Christoph found just 2. This doesn't match with what I found on the web map tool. Anyways, here, he identifies that there are only two differently coloured categories between A and B. I will have to retry this myself 
So the difference is that he didn't account for temporary operating restrictions (red-tinted shades on my map tool) while I took them into consideration. Also, he didn't count the exact number of zones. Instead, he counted the number of different colours. Essentially, he was asking for the **number of types of geo-zones between A and B** and not the actual count itself. Hence the discrepancy

As for the orthodrome distance calculation, I applied the correct formula but the reason my answer didn't match the measured distance is silly -- I switched the latitudes and longitudes in my calculation! Notations are confusing :(

### External Links
- https://en.wikipedia.org/wiki/Great-circle_distance#Formulae

| Previous                                                                          |     | Next                                                     |
| --------------------------------------------------------------------------------- | --- | -------------------------------------------------------- |
| [[TUM Urban Air Mobility - Week 3 - National Drone Policies and Legal Framework]] |     | [[TUM Urban Air Mobility - Week 3 - Legal Requirements]] |
