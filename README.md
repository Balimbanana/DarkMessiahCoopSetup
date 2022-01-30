# Dark Messiah Coop Setup
These are all changes to lumps and potentially other files that will be needed for co-op compatibility.



# ChangeLog:
### l00

**Changes**
- trigger_once at "1408 204 -256"
	Removed output that closes the door behind you.
- point_teleport "point_teleport.kick_undead" at "1404 -1300 24"
	Changed to info_player_teleport
- trigger_multiple "tuto_kick_undead.npc_undead.trigger2" at "1408 -919 -36"
	Changed to trigger_teleport
	Removed "teleport.fade_" Fade outputs
- weapon_arxsword "weapon_sword" at "1424 -2223 182"
	Changed to template which will respawn indefinitely
- trigger_once at "876 -2427 436"
	Add checkpoint outputs to 01
- trigger_once at "1408 -1460 127"
	Add checkpoint outputs to 02

**Checkpoints**
- spawnpoint_00 at "1165 339.496 1565" At the start
angles "0 33.5 0"
- spawnpoint_01 at "876 -2427 436" After the first rope.
angles "0 90 0"
- spawnpoint_02 at "1405 -1335 40" At the zombie kick off part
angles "0 90 0"

### l01_a

- Added Ballista "Baliste270_2" at "-1129.061 822.25 712"

**Removed**
- func_brush "Grange_playerclip" at "1755 -85 904"
- func_brush "PlayerClip.House" at "1631.75 -599.5 402.5"
- player_loadsaved "player_loadsaved.fallydeath" at "1744 376 748"

**Changes**
- func_button "room07.door.01.lever.button" at "-1424.5 1206 456"
	Removed spawnflag "Use Activates" (512) to prevent player interaction
- scripted_sequence "sequence_guard_call_before_attack" at "265 -1890 -8.99999"
	Added player teleport and checkpoint 01 activation This is the same entity that sends CinematicEnd()
- trigger_once at "1801 135 908.5"
	Removed rope destruction outputs
- trigger_once at "1804 -645.45 867.5"
	Add checkpoint outputs to 02
- trigger_once at "1981.5 543 1042"
	Add checkpoint outputs to 03
- trigger_once at "-138 1476 897.5"
	Add checkpoint outputs to 04

**Checkpoints**
- spawnpoint_00 at "1388.6 -644.985 -11.2139" At the horse
- spawnpoint_01 at "360 -1900 28" Inside barracks
angles "0 130 0"
- spawnpoint_02 at "1800 -75 865" Just before rope jump
angles "0 90 0"
- spawnpoint_03 at "1685 330 780" Just after rope jump
angles "0 90 0"
- spawnpoint_04 at "-825 1455 750" At ballistas
angles "0 270 0"
