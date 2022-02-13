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

### l03_b

##### Added point_teleport "teleport_players" at "3460 1088 -1345"


***Removed***
- trigger_multiple at "3460 1028 -1300" causes villagers to not be attacked

***Changes***
##### trigger_changelevel landmark "l03_atob"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### func_occluder "occluder.warehouse"
- Changed name to occluder.warehousenoclose so it doesn't close when players reach different areas than others
##### logic_relay "scene.xana_warning.relay"
- Added teleport all players (teleport_players) to trigger position for cinematic
##### trigger_once at "3472 1080 -1573"
- Added global reset for villager attack just in case
- Removed fade
- Removed changelvl.toL4_brush block
##### trigger_multiple at "-1176 972 -837.5"
- Added checkpoint outputs to 01
##### trigger_once at "-904 952 -816"
- Added checkpoint outputs to 02
##### trigger_once at "3160 728 -1378"
- Added checkpoint outputs to 03

***Checkpoints***
- spawnpoint_00 at "196 209 -342"
angles "0 101 0"
- spawnpoint_01 at "-1183 895 -895" in first trap door tunnel
angles "0 270 0"
- spawnpoint_02 at "-915 920 -828" after entering second trap door tunnel
angles "0 70 0"
- spawnpoint_03 at "3130 740 -1450" outside menalag's area
angles "0 10 0"

### l04_b

##### Added point_teleport "teleport_players_end" at "-1350 -2260 -1136"

***Changes***
##### npc_Leanna "npc_Leanna" at "748 -4559 -1482.61"
- Removed reload on player damage
- Set damage filter to ignore player
##### npc_wizard "R49A_wizard_Kojak" at "696 -4509 -1482.31"
- Removed reload on player damage
- Set damage filter to ignore player
##### trigger_once "fermeture_caisse" at "868 -3956.5 -1314"
- Removed door closing outputs
- Added checkpoint outputs to 01
##### trigger_multiple "disable_rush01" at "853 -4646 -1354.5"
- Changed OnEndTouch to OnEndTouchAll
##### npc_necro_guard "R12_necroGuardPatrol_02" at "-1326 -4241 -1589"
- Added checkpoint outputs to 02 OnDeath
##### func_door_rotating "R22A_door" at "-1667 -4061 -1542"
- Added checkpoint outputs to 03
##### trigger_once "R31_trigger_general" at "-1616 -2308 -1279"
- Added checkpoint outputs to 04
##### trigger_once at "-1630 -3527.5 -1254"
- Added checkpoint outputs to 05
##### Fixup to ballistas base and nose props
- Baliste0_1_prop Baliste0_2_prop Baliste0_3_prop
##### logic_choreographed_scene "leanna_good_luck" at "868 -4111 -1284"
- Removed effect for crate
##### point_teleport "point_teleport_0*"
- Changed to !activator teleports for ballistas
##### trigger_multiple at "-1536 -3008 -1904"
- Changed OnEndTouch to OnEndTouchAll
##### trigger_multiple "r49_trig_ballistes_vs_player" at "-592 -3248 -1256"
- Changed OnEndTouch to OnEndTouchAll
##### func_door_rotating "porte_close_03" at "-2035 -2465.69 -1270.62"
- Added output to stop npc ballistas OnOpen
##### func_door_rotating "R31_35_door" at "-1344.9 -2462.76 -1270.87"
- Added output to stop npc ballistas OnOpen
##### func_door_rotating "porte_close_01" at "-1793 -2466.69 -1270.87"
- Added output to stop npc ballistas OnOpen
##### math_counter "end" at "-1314 -2224 -1089"
- Added teleport all players

***Checkpoints***
- spawnpoint_00 at "2196 -4656 -1503"
angles "0 180 0"
- spawnpoint_01 at "1025 -4182 -1416" after leanna opens door
angles "0 150 0"
- spawnpoint_02 at "-1333 -4155 -1404" at entrance of ship
angles "0 250 0"
- spawnpoint_03 at "-1690 -4200 -1550" inside room with food
angles "0 90 0"
- spawnpoint_04 at "-1725 -2285 -1550" at bottom of ladder leading to ballistas
angles "0 0 0"
- spawnpoint_05 at "-1942 -3473 -1264" entrance to top of ship
angles "0 0 0"

### l05_a

***Changes***
##### npc_Leanna "npc_Leanna" at "-151.522 1051.95 -985.998"
- Removed reload on player damage
- Set damage filter to ignore player
##### npc_wizard's
- Removed reload on player damage
- Set damage filter to ignore player

***Checkpoints***
- spawnpoint_00 at "504 -918 -1073"
angles "0 91 0" parented to "boat"