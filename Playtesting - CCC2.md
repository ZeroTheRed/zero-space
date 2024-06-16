Difficulty: HMP
Source Port: Nugget Doom

## General Notes
![[Pasted image 20230915144425.png]]
- Update map name and "total time" font to CCC2 one
- Show the intended map name instead of default name

## MAP01 - YE INTRO MAPPE
- Looks like a placeholder

## MAP02 - Castledoomia 2: Knight's Quest
- 2 backpacks in close-by locations (redundant) - The first secret had a backpack and then there's another non-secret backpack close by. What is the secret for then?
- Starting area is quite underwhelming - Lot of obstacles that obstruct wiggle room
- Way too many trees + mancubi fireballs from afar + imp projectile shower = strenuous movement for cover (the area right after the starting 4 buildings)
- Weird texture bug (software renderer shenanigans)
![[Pasted image 20230915150409.png]]
- Add a fence here (looks very odd)
![[Pasted image 20230915150604.png]]
- No-escape kill pit right before yellow key room (the player won't really jump in there unknowingly so it's a non-issue + it's towards the first third of the map so it's fine I guess but your call whether to have an escape route here or not)
- A third backpack (opposite to the revenant and plasma gun alcove). Do you really need 3 backpacks in a single level, all in the first half of the map?
	- Fourth backpack beyond the cave that takes you to the place where the soulsphere and 3 HK secret is located
- Soulsphere secret before the blue key is bizarre to obtain
- 4 cyberdemons in a small area? HMP? A bit too harsh, no?

## MAP03 - Castle Klattakus MKII
- ![[Pasted image 20230915153153.png]]
Widen the pillar cages a bit -- If the software renderer is used, the player can prematurely see what's hidden in the trap and it ruins the surprise a bit
- 2 chainsaws in one map 
- Megaarrmor secret too cryptic (you have to hump the DOORTRAK of the chainsaw secret opposite to it to get this one). No clear indication that this is the secret trigger

## MAP05 
Texture misalignment
![[Pasted image 20230916143025.png]]
* Line 123 is facing the other side and is blocked from the player's reach (cannot flip switch and hence, the secret is inaccessible)
* Switch in Sector 213 is too far and dark for the player to notices

## MAP06 - The Depths
* Starting is too harsh for HMP (Revenants + HKs + Mancubus)
* Linedef 168 has no texture - HOM. Linedef 716
* Linedef 172 is a bit buggy (you can't trigger it on the left half because of the player's hitbox)
* The player might most likely be at low health by the time they reach the AV cage +the slime floor is damaging. Bit too much for HMP?
* ![[Pasted image 20230916151516.png]]
* Weird stuff happening on sector tags 31 (Got it -- Sector 75 is accidentally tagged with the same number as the door adjacent to it)
* Linedefs surrounding the soulsphere along trigger the rise of sector 159 with the imp swarm but the player can easily dodge that and end up getting accosted by a HOM pit of imps
* Same area -- A cell pack sitting in plain sight is a secret but the megaarmor (obtained by straferunning off the platform) isn't. Makes sense to be the other way around
* Sector 16 - One-way door (what if the player wants to revisit previous sections of the map?)
* ![[Pasted image 20230916152646.png]]
* Texture misalignment right there

## MAP07
Texture misalignment
![[Pasted image 20230916220049.png]]

![[Pasted image 20230916220139.png]]
Silent teleport line can be carefully stepped to prevent a room-over-room effect, leading to HOMs

![[Pasted image 20230916220340.png]]
Same problem here as well (no-key door entry place, with the tight stairwell)

![[Pasted image 20230916221910.png]]
Increase height of building if possible

![[Pasted image 20230916223855.png]]
Tex misalignment

![[Pasted image 20230916224245.png]]
Tree lowers and "falls off" along with floor

## MAP08 - Castle Superbeast
![[Pasted image 20230920144534.png]]

## MAP10 - Tower of Doom
Starting area - Portal fuck

Lift issue (Sector 335)

Can't get out of the pain elemental room
