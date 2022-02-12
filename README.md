# Dark Messiah Coop Setup
These are all changes to lumps and potentially other files that will be needed for co-op compatibility.



# ChangeLog:
### l00

***Changes***
##### trigger_once at "1408 204 -256"
- Removed output that closes the door behind you.
##### point_teleport "point_teleport.kick_undead" at "1404 -1300 24"
- Changed to info_player_teleport
##### trigger_multiple "tuto_kick_undead.npc_undead.trigger2" at "1408 -919 -36"
- Changed to trigger_teleport
- Removed "teleport.fade_" Fade outputs
##### weapon_arxsword "weapon_sword" at "1424 -2223 182"
- Changed to template which will respawn indefinitely
##### trigger_once at "876 -2427 436"
- Add checkpoint outputs to 01
##### trigger_once at "1408 -1460 127"
- Add checkpoint outputs to 02

***Checkpoints***
- spawnpoint_00 at "1165 339.496 1565" At the start
angles "0 33.5 0"
- spawnpoint_01 at "876 -2427 436" After the first rope.
angles "0 90 0"
- spawnpoint_02 at "1405 -1335 40" At the zombie kick off part
angles "0 90 0"

### l01_a

- Added Ballista "Baliste270_2" at "-1129.061 822.25 712"

***Removed***
- func_brush "Grange_playerclip" at "1755 -85 904"
- func_brush "PlayerClip.House" at "1631.75 -599.5 402.5"
- player_loadsaved "player_loadsaved.fallydeath" at "1744 376 748"

***Changes***
##### func_button "room07.door.01.lever.button" at "-1424.5 1206 456"
- Removed spawnflag "Use Activates" (512) to prevent player interaction
##### scripted_sequence "sequence_guard_call_before_attack" at "265 -1890 -8.99999"
- Added player teleport and checkpoint 01 activation This is the same entity that sends CinematicEnd()
##### trigger_once at "1801 135 908.5"
- Removed rope destruction outputs
##### trigger_once at "1804 -645.45 867.5"
- Add checkpoint outputs to 02
##### trigger_once at "1981.5 543 1042"
- Add checkpoint outputs to 03
##### trigger_once at "-138 1476 897.5"
- Add checkpoint outputs to 04

***Checkpoints***
- spawnpoint_00 at "1388.6 -644.985 -11.2139" At the horse
- spawnpoint_01 at "360 -1900 28" Inside gate area
angles "0 130 0"
- spawnpoint_02 at "1800 -75 865" Just before rope jump
angles "0 90 0"
- spawnpoint_03 at "1685 330 780" Just after rope jump
angles "0 90 0"
- spawnpoint_04 at "-825 1455 750" At ballistas
angles "0 270 0"


### l02_a

***Removed***
- player_loadsaved "Gestion_dead_reload" at "2284 -3791 -40"

***Changes***
- weapon_arxcrossbow at "2397.77 -3646.71 -107"
- weapon_mm_staff_wood at "2411.77 -3674 -113"
- weapon_arxsword at "2365.44 -3890.39 -330"
- weapon_mm_shield_guard at "2394 -3803 -341"
- weapon_arxdaggers at "2380 -3711 -343"
- Added infinite respawn
##### trigger_look "trigger_look_leanna" at "3135 -1217.5 -447"
- Removed cinematic lock to allow players to move around
##### npc_Leanna "Leanna" at "3136 -1216 -490"
- Removed reload on player damage
- Set damage filter to ignore player
##### trigger_once "sareth_door_close" at "3615.5 -1375 -338"
- Removed door close outputs
##### logic_relay "Gestion_relationship" at "2284 -3790 -58"
- Added output to keep required guards friendly
- Added output to delete logic_autosave to prevent saving after guards are hostile
##### trigger_once at "2726 -1394.5 -306.5"
- Add checkpoint outputs to 01

***Checkpoints***
- spawnpoint_00 at "2181 -3972 -139"
angles "0 45 0"
- spawnpoint_01 at "2600 -1445 -452"

### l02_b1

***Changes***
##### npc_Leanna "Leanna" at "3136 -1216 -490"
- Removed reload on player damage
- Set damage filter to ignore player
##### npc_necro_guard "tim" at "-3420 -12804 32.9032"
- Add checkpoint outputs to 01 OnDeath
##### trigger_once at "-3492 -10892 159"
- Add checkpoint outputs to 02

***Checkpoints***
- spawnpoint_00 at "-4815 -10825 305"
angles "0 270 0"
- spawnpoint_01 at "-3040 -13035 45"
angles "0 35 0"
- spawnpoint_02 at "-3575 -10875 105"
angles "0 270 0"

### l02_b2

##### Added trigger_once at "-3474 -12171 109"
- Set up to unlock the kitchen doors

***Changes***
##### trigger_changelevel landmark "b1toB2bis"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### kitchen_door_big1 and kitchen_door_big2
- Added functionality to open door by a trigger on the other side of it.
##### func_door_rotating "kitchen_out_door" at "-3265 -11737 152"
- Add checkpoint outputs to 01

***Checkpoints***
- spawnpoint_00 at "-3575 -11195 -125"
angles "0 270 0"
- spawnpoint_01 at "-3142 -11695 -50"
angles "0 270 0"

### l03_a

***Removed***
- trigger_once at "-1017 3205 173.5" causes rope to break

***Changes***
##### trigger_once at "672 1937.5 -76"
- Added checkpoint outputs to 01
##### trigger_multiple at "-252 3872 9"
- Added checkpoint outputs to 02
##### trigger_once at "-1014.5 2775 219"
- Added checkpoint outputs to 03

***Checkpoints***
- spawnpoint_00 at "2016 1184.01 -24"
angles "0 180 0"
- spawnpoint_01 at "680 1955 -80"
angles "0 260 0"
- spawnpoint_02 at "-252 -3872 -10"
angles "0 190 0"
- spawnpoint_03 at "-1040 2765 165"
angles "0 270 0"