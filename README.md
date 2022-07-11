# Dark Messiah Coop Setup
These are all changes to lumps and potentially other files that will be needed for co-op compatibility.

### Installation:
- Place everything in this repo inside:
- steamapps\common\Dark Messiah Might and Magic Single Player\mm_tempcontent
- Create the directory mm_tempcontent if it doesn't exist. Now right click Dark Messiah Single Player on Steam and go to:
- Properties... > General > Launch Options and set it to: `-tempcontent`
- Now if all goes well, you should be able to start up Dark Messiah Single Player and see the Create Server button in the main menu.
- If you want to disable all the changes, just simply remove the launch option and it will start up in regular single player.

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
angles "0 0 0"
- spawnpoint_02 at "1405 -1335 40" At the zombie kick off part
angles "0 90 0"

### l01_a

- Added Ballista "Baliste270_2" at "-1129.061 822.25 712"

***Removed***
- func_brush "Grange_playerclip" at "1755 -85 904"
- func_brush "PlayerClip.House" at "1631.75 -599.5 402.5"
- trigger_once "trigger_death" at "-719 324 91"
- player_loadsaved "player_loadsaved.fallydeath" at "1744 376 748"

***Changes***
##### func_button "room07.door.01.lever.button" at "-1424.5 1206 456"
- Removed spawnflag "Use Activates" (512) to prevent player interaction
##### scripted_sequence "sequence_guard_call_before_attack" at "265 -1890 -8.99999"
- Added player teleport and checkpoint 01 activation This is the same entity that sends CinematicEnd()
##### trigger_once at "-1120.5 -134.5 -211"
- Changed to trigger_hurt
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

##### Added trigger_multiple at "808 8434.5 -491" allow more players to fall without fall damage
- Also sets checkpoint to 02

***Removed***
##### trigger_multiple at "-200 3400 -300" causes area portals to close
##### trigger_multiple at "-441 3872 -640" causes area portals to close

***Changes***
##### npc_Leanna "npc_Leanna" at "-151.522 1051.95 -985.998"
- Removed reload on player damage
- Set damage filter to ignore player
##### npc_wizard's and npc_human_guard's
- Removed reload on player damage
- Set damage filter to ignore player
##### trigger_once at "-348 4416 -793.5"
- Added checkpoint outputs to 01
##### trigger_once at "-1040 9641 -153"
- Added checkpoint outputs to 03
##### weapon_arxcrossbowrope "rope_bow"
- Added infinite respawn

***Checkpoints***
- spawnpoint_00 at "504 -918 -1073"
angles "0 91 0" parented to "boat"
- spawnpoint_01 at "-530 4275 -820" at first cinematic for orcs
angles "0 30 0"
- spawnpoint_02 at "780 8350 -685" After drop in to temple
angles "0 90 0"
- spawnpoint_03 at "-1045 8850 -333" After dragon appearance
angles "0 90 0"

### l05_b

***Added***
##### env_global's for transition back from multiple sources
- Sets spawnpoints and set up environments if needed
##### trigger_teleport's at "80 562 423"
- Used for transition positions

***Changes***
##### npc_Leanna "npc_Leanna" at "232 1570 247"
- Removed reload on player damage
- Set damage filter to ignore player
##### func_button "porticullis_couloir.lever.button" at "2966 4077.5 412"
- Set wait -1 and Lock so it can't be closed once opened
##### trigger_once at "4422 3012 -72"
- Changed to trigger_hurt
##### trigger_multiple at "275 4540 423"
##### trigger_multiple at "3960 4016 632"
- Changed outputs to OnEndTouchAll
##### trigger_multiple "PlayerZoneC" at "26 3714 424"
- Changed outputs to OnEndTouchAll
- Added checkpoint outputs to 01
##### math_counter "counter_orcs dead" at "-52 4076 353"
- Added checkpoint outputs to 02
##### math_counter "goblin_death_counter" at "2156 4384 353"
- Added checkpoint outputs to 03
##### trigger_multiple at "80 4960 451"
- Added checkpoint outputs back to 02
##### trigger_once at "5824 2992 542"
- Added checkpoint outputs to 01_from5c
##### func_button "door_goblin_trap.lever.button" at "4898.5 4235 492"
- Prevent use as it could block players
##### ambient_generic "SND_Heal_Life" at "6726 5190 1098"
##### ambient_generic "SND_Heal_Mana" at "6715 2862 1086"
- Removed spawnflag for Play Everywhere (1)
##### trigger_regen's
- Changed OnEndTouch to OnEndTouchAll
##### trigger_changelevel "Changelevel_L05B_L07A"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)

***Checkpoints***
- spawnpoint_00_from5a at "78 547 332"
angles "0 90 0"
- spawnpoint_01 at "40 3640 382" just before main altar
angles "0 90 0"
- spawnpoint_02 at "200 4105 382" in main altar room
angles "0 120 0"
- spawnpoint_03 at "1450 4380 382" by the first goblin room
angles "0 0 0"

- spawnpoint_00_from5c at "3190 5475 105" entrance from 5c
angles "0 280 0"
- spawnpoint_01_from5c at "6143 2910 710" just before goblin area
angles "0 0 0"

- spawnpoint_00_from7a at "850 4295 4715"
angles "0 90 0"
- spawnpoint_01_from7a at "1155 4995 4715" on elevator from 07
angles "0 0 0" parentname "elevator_C"

##### Might have to change prop_physics at "1160 5000 4664" to a prop_dynamic solid 6 for elevator if it kills players

### l05_c

***Changes***
##### trigger_once at "984 6683.5 436"
- Added checkpoint outputs to 01

***Checkpoints***
- spawnpoint_00 at "80.9556 5291.09 205"
angles "0 90 0"
- spawnpoint_01 at "490 6730 210"
angles "0 0 0"

### l07_a

***Added***
##### trigger_teleport "teleport_start_7b" at "4455 4099 1145"
- Used when transitioning back

***Changes***
##### trigger_changelevel landmark "info_landmark_to_L07"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_multiple's
- Removed outputs closing portal.elevator and portal.halfway
##### trigger_once at "3704 -1320 2436"
##### trigger_once at "7144 384 7204"
##### trigger_once at "2968 984 6960"
##### trigger_once "TRIGG_player_Load_Save" at "2992 1168 786"
- Changed to trigger_hurt
##### trigger_once "r21_trigg_SON_oiseaux" at "3160 1520 2204"
- Added checkpoint outputs to 01
##### trigger_once "r23b_SPAWNdest_place_kill" at "4052 -116 2978"
- Added checkpoint outputs to 02

***Checkpoints***
- spawnpoint_00 at "4380 3888 971"
angles "0 270 0"
- spawnpoint_01 at "3380 1450 2170" by the elevator
angles "0 180 0"
- spawnpoint_02 at "4080 -1205 3050" across the rope bridge
angles "0 90 0"
- spawnpoint_00_from7b at "4273 360 3670"
angles "0 180 0"
- spawnpoint_elevator at "4070 1862 2170"
angles "0 270 0" parentname "elevator_21A"

### l07_b

***Added***
##### func_brush "backtrack" at "4152 232 4355"

***Changes***
##### trigger_once at "2589.38 4684.98 3922.05"
- Changed to trigger_hurt
##### trigger_multiple at "4280 105 4477"
- Removed outputs closing portal.forgehouse, portal.lasthouse, portal.forge and portal.halfway
##### trigger_once at "3400 2090 5661.5"
- Added checkpoint outputs to 01
##### func_button "lever1.button" at "4521.5 1088 5240"
- Prevent multiple use
- Added output to remove backtrack block
- Added checkpoint outputs to 02

***Checkpoints***
- spawnpoint_00 at "4280 105 4477"
angles "0 180 0"
- spawnpoint_01 at "3355 1910 5622"
angles "0 90 0"
- spawnpoint_02 at "4430 1060 5189"
angles "0 90 0"

### l08_a1

***Changes***
##### trigger_changelevel landmark "info_landmark_to_L08"
##### trigger_changelevel landmark "lich_climb"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### prop_physics "gem1", "gem2", "gem3", and "gem4"
- Made infinite respawn until socketed, then remove all
##### prop_physics "gem4" at "0 -1284 -852"
- Added checkpoint outputs to 02 once socketed
##### trigger_multiple at "-2524.08 -783 -3195.5"
- Changed to trigger_hurt
##### func_button "funcBut_Aq" at "-1838 -786 -1632"
##### func_button "funcBut_Ac" at "-594 -510 -888"
- Changed to only open
##### trigger_once "Master_Trigger" at "589 -591.5 -638.5"
- Added checkpoint outputs to 01
##### logic_case "gem_logic_cases" at "-170 -560 -499"
- Teleport all players in front of spider statue for sequence
##### trigger_once at "0 -2080 -496.5"
- Removed outputs that close door

***Checkpoints***
- spawnpoint_00 at "1383 258 -192"
angles "0 0 0"
- spawnpoint_01 at "930 -572 -695" at first drop down
angles "0 180 0"
- spawnpoint_02 at "215 -772 -482" at spider statue room
angles "0 135 0"
- spawnpoint_00_from8b at "-1778 625 -1490"
angles "0 180 0"

### l08_a2

***Removed***
##### trigger_once at "-2760 2056 -1756"
- Removes a bunch of things after dropping past it.

***Changes***
##### trigger_changelevel landmark "L08_A1toL08_A2_1"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### func_button "funcBut_Bc" at "-1074 546 -973"
- Added checkpoint outputs to 01
- Locked lever until gem is aquired

***Checkpoints***
- spawnpoint_00 at "-1815 1643 -599"
angles "0 0 0"
- spawnpoint_01 at "-1755 450 -1422" just after big door to lower crypt
angles "0 180 0"

### l08_b

***Added***
##### trigger_teleport at "657 562 -490", "-587 562 -490", and "885 572 -732"
- Teleports all players outside the lich room in to the lich room

***Removed***
##### trigger_multiple at "887 406 -581"
- Closes multiple area portals

***Changes***
##### trigger_changelevel landmark "from_l8_a"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_multiple at "2045 966.5 -612"
- Changed outputs to OnEndTouchAll
##### trigger_once at "2050 -148.5 -491.5"
- Added checkpoint outputs to 01
- Added output to teleport all players outside arena

***Checkpoints***
- spawnpoint_00 at "325.12 -251.091 505"
angles "0 180 0"
- spawnpoint_01 at "" in the lich room
angles "0 0 0"

### l09_a

***Added***
##### trigger_multiple at "-2985 -5608 -4336"
- Sets up start equipment/xana form and disables inventory

***Changes***
##### trigger_once at "-16 -7064.83 -3640"
- Added checkpoint outputs to 01
##### trigger_once at "-471 -2851 -3808"
- Added checkpoint outputs to 02
##### trigger_once at "-2304 520 -2616"
- Added checkpoint outputs to 03
##### trigger_once at "-1872 -1116 -2786.48"
- Added checkpoint outputs to 04

***Checkpoints***
- spawnpoint_00 at "-2985 -5608 -4336"
angles "0 45 0"
- spawnpoint_01 at "-100 -7060 -3800" after archer
angles "0 20 0"
- spawnpoint_02 at "-635 -2875 -3855" before cyclops room
angles "0 0 0"
- spawnpoint_03 at "-2295 1182 -2265" before spider room
angles "0 270 0"
- spawnpoint_04 at "-273 -1335 -2854" above cyclops room
angles "0 15 0"

### l06_a

***Removed***
##### player_loadsaved

***Changes***
##### trigger_multiple "TRIGG_player_Load_Save" at "3008 -4128 -184"
- Changed to trigger_hurt
##### trigger_multiple "TRIGG_conditionsGOB_chat1ON" at "1149 -5171.5 364"
- Added checkpoint outputs to 01

***Checkpoints***
- spawnpoint_00 at "1071 -1689 214"
angles "0 0 0"
- spawnpoint_01 at "1375 -4380 540"
angles "0 250 0"

### l06_b

***Added***
##### trigger_multiple at "-2049.5 -3911.92 521.9"
- Used to return the worm back to the starting height when starting back across the bridge.
- Also sets spawnpoint to 01

***Removed***
##### player_loadsaved
##### trigger_multiple "TRIGG_disappearFIN" at "-1784 -1584 664"
- Prevents further players from progressing by brush and worm functions.
##### func_brush "player_no_exit" at "-1883 -1584 664"

***Changes***
##### trigger_changelevel landmark "landmark_06_A_06_B"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "-2528 -3128 -88"
- Changed to trigger_hurt
##### trigger_once "Ver_trig_pilier_01" at "-2049.5 -3911.92 521.9"
- Removed pilar drop outputs
##### path_track "worm_attack_littlearch02" at "-2648 -3736 -640"
- Moved to "-2648 -3500 -640"
##### path_track "VerTrack_Balliste3" at "-2824 -3856 -613"
- Moved to "-2900 -3556 -613"
##### path_track "VerTrack_N_ARCH" at "-2592 -3880 -1164.86"
##### path_track "VerTrack_BatSWbas02" at "-2584 -3880 -1165"
- Moved to "-2592 -3450 -1164.86"
- Changed angles to "0 200 0"
##### path_track "VerTrack_poisonBatSWbas" at "-2744 -3912 -1165"
- Moved to "-2700 -3600 -1165"
- Changed angles to "0 200 0"
##### prop_physics at "-3340.82 -3843.9 36.9646" and "-3295.31 -3843.9 36.9646"
- Made indestructible so further players can still make it across
##### trigger_multiple "VerBatSWbasTRIGG" at "-3540.84 -3813.3 70.07"
- Added checkpoint outputs to 02
##### trigger_once "Ver_pont_TRIGG_player" at "-3968 -2048 208"
- Added checkpoint outputs to 03
##### logic_relay "Ver_blocs_SWrelay" at "-3751.85 -3817.65 569"
- Removed all outputs that block the doorway after walking through.

***Checkpoints***
- spawnpoint_00 at "448 -4176 817"
angles "0 90 0"
- spawnpoint_01 at "-865 -3685 630" just before bridge
angles "0 200 0"
- spawnpoint_02 at "-3610 -3665 135" after bridge
angles "0 270 0"
- spawnpoint_03 at "-5220 -2575 360" in alcove with chest
angles "0 300 0"

### l06_c

***Added***
##### trigger_teleport's "teleport_to_raft"
- Moves all players from the start and up to the gate on to the raft.
based on trig -341 -1394.5 -796.64

***Changes***
##### trigger_changelevel landmark "landmark_06_B_06_C"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### logic_relay "Puits_relayPUSHetc" at "-506.649 -2495.63 -1030"
- Added checkpoint outputs to 01.
- Added output to teleport players outside of the room via teleport_to_raft

***Checkpoints***
- spawnpoint_00 at "-1244 -1585 -624"
angles "0 90 0"
- spawnpoint_01 at "-295 -2406 -1030" on raft
angles "0 270 0" parentname "PUITS_ascenceur_pour_l_echaffaud"

### l06_d

***Added***
##### 2x: func_button, post, chain, wheel
- Used for returning the carts after they reach the other side.

***Changes***
##### trigger_changelevel landmark "landmark_L06_C-L06_D"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_multiple at "1906 -4511 1846" and "4427 -4429 848"
- Changed outputs to OnEndTouchAll
##### trigger_once at "3440 -4128 -148" and "4424 -1792 -424"
- Changed to trigger_hurt
##### trigger_multiple "close.portalmuraille" at "2617.5 -4629.5 988"
- Removed outputs that close area portals
##### trigger_once at "4016.5 -4159 899"
- Added checkpoint outputs to 01.

***Checkpoints***
- spawnpoint_00 at "1345 -6055 2645"
angles "0 0 0"
- spawnpoint_01 at "4553 -4475 870" after second cart
angles "0 90 0"


### l09_d

***Removed***
##### trigger_multiple at "2935.5 -338.5 1758.5"
- Closes area portals outside.
##### logic_branch "player_in_xana" at "-595.988 -1379.64 229.758"
- Prevents boat scene from happening if any player enters Xana form.

***Changes***
##### trigger_changelevel landmark "landmark_L06_A_L09_D"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "2055 -363 1992"
- Added checkpoint outputs to 01.
##### npc_wizard and npc_human_guard
- Made invincible to player attacks.
##### logic_choreographed_scene "scene.xana_beach01" at "1920 -1391.16 832"
- Removed output for message about demon form.

***Checkpoints***
- spawnpoint_00 at "5653 -654 1350"
angles "0 90 0"
- spawnpoint_01 at "1895 -322 1900"
angles "0 230 0"

### l10_a

***Added***
##### func_brush at "1535 -6420 676"
- Used to make exiting water at the start slightly smoother.
##### trigger_teleport "teleport_start_10c" at "1372 -5795 710"
- Used to teleport stragglers from the original start to the 10c start on transition.

***Changes***
##### trigger_once at "16 -3600 912.5"
- Removed output to close portal (teleport_shutdown).
- Added output to complete enter portal objective.
- Added name "trigger_firstentry" which will be removed on transition back from l10_c
##### trigger_once at "1120 -5536 928"
- Added name "trigger_firstentry" which will be removed on transition back from l10_c
##### trigger_once at "16 -444 144"
- Changed to trigger_hurt.
##### trigger_changelevel landmark "l10_AtoL10_C_1"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)

***Checkpoints***
- spawnpoint_00 at "1372 -5795 710"
angles "0 280 0"
- spawnpoint_00_from10c at "280 2045 -25"
angles "0 180 0"
- spawnpoint_01_from10c at "-85 -2755 -280" at bottom of elevator
angles "0 180 0"

### l10_b

***Added***
##### trigger_multiple "key_blackorb_trigger" at "2677 6686 -568"
- Gives orb to players that enter the room.

***Removed***
##### trigger_multiple at "3496 4920 266"
- Disables stairs brush

***Changes***
##### trigger_changelevel landmark "MAP_AB_01"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "3496 4920 -344"
- Added checkpoint outputs to 01.
##### func_rot_button "bibliodoor" at "3487.5 4344.5 -480"
- Added checkpoint outputs to 02.

***Checkpoints***
- spawnpoint_00 at "1680 3720 520"
angles "0 0 0"
- spawnpoint_01 at "3500 4545 5" half way down stairs
angles "0 90 0"
- spawnpoint_02 at "3500 4440 -490" bottom of stairs
angles "0 270 0"

### l10_c

***Added***
##### env_global for transition back to l10_a
- Sets spawnpoints and set up environments.

***Removed***
- player_loadsaved "game_over"

***Changes***
##### trigger_changelevel landmark "MAP_AB_02"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "1040 3040 -400" and "1024 3056 456"
- Changed to trigger_hurt
##### trigger_once at "556 5248 1240"
- Added checkpoint outputs to 01.
##### func_button "Room33.door.01.lever.button" at "-816 2990.5 1172"
- Added checkpoint outputs to 02.
##### trigger_multiple "leanna_cocoon.trigger" at "1892 1912 -3144"
- Moved player_in_elevator.trigger enable to this trigger.
##### trigger_once at "452 3072 44"
- Added checkpoint outputs to 03.
##### func_button "Room37.door.38.lever.button" at "1078.5 4754 -572"
- Added checkpoint outputs to 04.

***Checkpoints***
- spawnpoint_00 at "12 2310 513"
angles "0 0 0"
- spawnpoint_01 at "-413 4750 805" near top of first stair case
angles "0 90 0"
- spawnpoint_02 at "-260 3065 1160" at top of first elevator
angles "0 180 0"
- spawnpoint_03 at "490 3070 -60" in room where choice to save Leanna is made
angles "0 0 0"
- spawnpoint_04 at "1150 4835 -3085" on elevator down to spider lair
angles "0 90 0"

### l11_a

##### Not addressed yet:
- Xana form hate/like relations with allies.

***Added***
##### trigger_teleport at "-2226 -3338 -486"
- Teleports players from the landmark position to the start position.

***Removed***
##### trigger_multiple "closepartie1_a" at "-880 -3200 -96"
- Closes area portals.
##### trigger_multiple at "268 -2060 388"
- Closes area portals.

***Changes***
##### trigger_multiple at "-2024 -2944 -18"
- Changed area portal conditions.
##### trigger_once at "1440 -940 -736" and trigger_multiple at "-416 -2296 -521.5"
- Changed to trigger_hurt.
##### trigger_multiple at "-1600 -2704 -72"
- Changed to only enable/spawn fire once on entry.
##### trigger_once at "-437 -3529 -204"
- Added checkpoint outputs to 01.
- Moved to "-437 -3495 -204"
##### trigger_multiple at "-1364 -2770 132"
- Changed to trigger_once.
- Removed area portal close.
- Added checkpoint outputs to 02.
##### trigger_multiple "openpartie1_a" at "-1752.5 -2957.5 -96" and "472 -1895 151" and "CS2.ZoneB" at "216 -1916 144"
- Changed outputs to EndTouchAll.
##### trigger_multiple at "-376 -1521.5 102.9" and "-312 -1521.5 102.9"
- Removed area portal close.
##### npc_villager_male "keyman.room02" at "307 -1913 106.036"
- Removed game over outputs (apart from death).
- Made invulnerable.
##### npc_human_guard "HumanGuard.room02.04" at "184 -1944 104"
- Removed game over outputs.
- Made invulnerable.
##### mm_player_inputs at "552 -1296 103.936"
- Removed Xana form game over.
##### logic_relay "Percy.2VillagerCloseDoor" at "224 -1904 112"
- Added checkpoint outputs to 03.
- Added teleport players outside the room for the scene.
- Added close area portals from previous areas.
##### logic_relay "Percy.5VillagerCloseDoor2" at "224 -1968 112"
- Keep door open.
##### logic_relay "Duncan_Scene.start" at "-452.307 -3500.34 -247"
- Removed CinematicBegin.
##### logic_choreographed_scene "HumanGuard.CS1.02.scene" at "-532 -3480 -246.427"
- Removed CinematicEnd.

***Checkpoints***
- spawnpoint_00 at "-2272 -3140 -880"
angles "0 75 0"
- spawnpoint_01 at "-370 -3565 -218"
angles "0 140 0"
- spawnpoint_02 at "-1435 -2780 180"
angles "0 0 0"
- spawnpoint_03 at "287 -1933 140"
angles "0 150 0"

### l11_b1

***Added***
##### trigger_once at "9863 -6751 133"
- Sets checkpoint to 01.

***Removed***
##### func_brush "anti_retour" at "9526.61 -6584.86 273.5"
- Blocks bridge.
##### logic_branch "Game_Over.IsPlayerInXana" at "8875 -6544 515"
- Reloads game if player in Xana form.
##### logic_relay "logic_relay_demon" at "8875 -6559 515"
- Reloads game if player in Xana form.
##### trigger_once at "10566.5 -6744 120"
- Removes Percy.

***Changes***
##### trigger_once at "9020 -6487.5 440"
- Removed clip re-enable.
- Changed StopActionLoop to Percy's sequence.
##### scripted_sequence "sequence_open_door3" at "8928.53 -6526 385"
- Added output to change name to Percy's sequence to enable door to stay open at start.
##### scripted_sequence "sequence_percy_jump" at "9307 -6464 190"
- Removed output to drop bridge.
##### trigger_once at "10051 -5040 -305.5" and "13834.5 -5201 -76"
- Changed to trigger_hurt.
##### npc_villager_male "keyman.room02" at "8924 -6529 388"
- Removed game over outputs (apart from death).
- Made invulnerable.
##### scripted_sequence "percy_exit_run" at "8984 -6554 386"
- Changed next script to run through door.
##### trigger_once at "11687.1 -5501.5 668.18"
- Added teleport for all players at start of cinematic.
##### trigger_multiple "trig_portalstart02_open" at "11676 -6552 360"
- Removed area portal closes.
- Added checkpoint outputs to 02.
##### trigger_multiple at "11676 -6521 360", "12436 -6788 496", "10064 -6744 384", "10096 -6744 384", "10480 -5397.04 448", "11213.9 -5230 240", "11126 -5226.5 280", "11960 -6706 360", "11536 -3952 172"
- Removed area portal closes.
##### trigger_multiple at "11340.3 -4544.57 240"
- Removed brush disable from leaving area.
##### trigger_multiple at "11536 -4040 172"
- Added checkpoint outputs to 03.

***Checkpoints***
- spawnpoint_00 at "8846 -6528 385"
angles "0 300 0"
- spawnpoint_01 at "9880 -6735 135" after first jump
angles "0 0 0"
- spawnpoint_02 at "11480 -6605 295" at top of first rope
angles "0 40 0"
- spawnpoint_temple at "11515 -5292 715"
- spawnpoint_03 at "10890 -5145 85" after third courtyard
angles "0 90 0"

### l11_b2

***Changes***
##### trigger_changelevel landmark "info_landmark_L11_B1_B2"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "7856 -2376 661"
- Added checkpoint outputs to 01.
##### trigger_multiple "PlayerTriggerZoneB" at "7440 -2469.5 673.15", "7411 -2553 673.15", "7312 -1736 673.15", "7520 -1752 673.15", "7568 -690 553", "9010 -2076 776", "7356 -526 514"
- Changed OnEndTouch to OnEndTouchAll
##### npc_villager_male "Percy" at "7454 -2750 629.146"
- Removed gameover outputs from Xana or player hit.
- Made invulnerable.
##### trigger_once at "9072 -3552 -96"
- Changed to trigger_hurt with fall damage.
##### trigger_once at "7360 -292 674"
- Removed door closing outputs.
##### momentary_rot_button "room05.grid.lever" at "7554.5 -926 705.77"
- Locked from player interaction.
##### func_door_rotating at "7532.5 -1575 716", "7760 -1030 716", "9631 -3043.5 328"
- Added lock on open then unlock for next use (resolves spam close door).
##### trigger_multiple "Percy.SequenceF.trigger" at "7356 -481 674"
- Removed gate close on end touch.

***Checkpoints***
- spawnpoint_00 at "9733 -3297 260"
angles "0 270 0"
- spawnpoint_01 at "7770 -2470 675" at meeting with Percy
angles "0 180 0"

### l11_c

***Added***
##### Ballistas

***Changes***
##### trigger_once at "340 -184 -598"
- Changed to trigger_hurt with fall damage.
##### trigger_multiple at "2740 376 108"
- Changed OnEndTouch to OnEndTouchAll.
##### Balistas adjusted

***Checkpoints***
- spawnpoint_00 at "1785 -721 -775"
angles "0 75 0"
- spawnpoint_01 at "1305 -445 -345"
angles "0 180 0"


### l12_a

***Changes***
##### trigger_changelevel landmark "info_landmark_to_L12"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_multiple at "-374 263 -2659" and "-809.5 2444 -2242.5"
- Changed to trigger_hurt.
##### trigger_once "piege_04_trigger_02" at "-1305 512 -963"
- Added checkpoint outputs to 01.
##### func_button "levier_spawnWizard.prop_AA" at "245 1470 -577"
- Added checkpoint outputs to 02.
##### trigger_once at "-1520 1176.5 -1600"
- Added checkpoint outputs to 03.
##### trigger_once at "-1251 2524 -1195"
- Added checkpoint outputs to 04.

***Checkpoints***
- spawnpoint_00 at "596 -1716 -463"
angles "0 180 0"
- spawnpoint_01 at "-1475 250 -1035" after first necromancer
angles "0 90 0"
- spawnpoint_02 at "5 1660 -570" at staircase after lich
angles "0 290 0"
- spawnpoint_03 at "-905 960 -1600" at bottom of stairs before casket optional open
angles "0 170 0"
- spawnpoint_04 at "-1275 2315 -1180" after cyclops in higher area
angles "0 200 0"

### l12_b

***Changes***
##### trigger_changelevel landmark "L12_A_LANDMARK"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "-780 4579.03 -895.27"
- Added checkpoint outputs to 01.
##### logic_relay "piege_02_start" at "-1061.58 3934.87 -1111"
- Removed first door close, made second door only close once.
##### func_button "funcBut_BB" at "-313 3666 -1616"
- Removed door close.
##### trigger_once at "150 4086 -1496"
- Added checkpoint outputs to 02.
- Removed output that closes door.
##### trigger_multiple at "-496 6740 -1836"
- Removed output that closes door.
##### logic_relay "big_end_door_open" at "-467.6 4871.19 -1999"
- Added checkpoint outputs to 03.
##### trigger_once at "-496 5064 -1948"
- Added teleport to 03 position.

***Checkpoints***
- spawnpoint_00 at "-1730.78 3210.01 -1655"
angles "0 90 0"
- spawnpoint_01 at "-680 4375 -1045" after first couple traps
angles "0 180 0"
- spawnpoint_02 at "5 4060 -1625" at lich room
angles "0 90 0"
- spawnpoint_03 at "-495 5080 -1970" after liches
angles "0 90 0"

### l12_c

***Added***
##### trigger_once at "2783.5 4216 -3526.5"
- Sets spawnpoint to 02.

***Removed***
##### trigger_once at "777 3604 -2862"
- Creates brush at start of map.

***Changes***
##### trigger_changelevel landmark "Landmark_L12_B-C"
- Set spawnflags 6 (2 disable touch) (4 to previous chapter)
##### trigger_once at "8486.31 5107.84 -3948", "2479 2532 -3836", "2587 5976 -3836", "7490.75 4275.65 -3134.5"
- Changed to trigger_hurt.
##### trigger_once at "625 4216 -2901.5"
- Added checkpoint outputs to 01.
##### trigger_multiple at "4262.5 4220 -3822.5"
- Removed area portal close.
##### logic_relay "go_stasis_destroy" at "3234 4222 -3723"
- Added checkpoint outputs to 03.
##### npc_leanna "leanna" at "683.723 4005.24 -3047.92"
- Made invulnerable to player (if she exists by this point).

***Checkpoints***
- spawnpoint_00 at "-1143.45 5167.35 -3055"
angles "0 270 0"
- spawnpoint_01 at "345 4220 -3020" meetup with leanna (if applicable)
angles "0 0 0"
- spawnpoint_02 at "1360 4775 -3675" entrance of arena
angles "0 290 0"
- spawnpoint_03 at "2900 4215 -3865" in front of altar
angles "0 0 0"