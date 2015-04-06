### Bot spawns (version 0.2.0)
Adds a number of options and ways to handle bot spawns
[Plugin](plugins/botspawns.smx?raw=true) - [Source](scripting/botspawns.sp)
Adjust bot spawning and rules to increase game control. In early beta, only navmesh spawning and multiple lives supported right now.
#### Dependencies
#### CVAR List
 * sm_botspawns_enabled: Enable enhanced bot spawning features (default: 0)
 * sm_botspawns_spawn_mode: Spawn in hiding spots  (default: 0)
 * sm_botspawns_respawn_mode: Do not respawn  (default: 0)
 * sm_botspawns_counterattack_mode: Use standard spawning for final counterattack waves  (default: 1)
 * sm_botspawns_counterattack_frac: Multiplier to total bots for spawning in counterattack wave (default: 0.5)
 * sm_botspawns_min_spawn_delay: Min delay in seconds for spawning. Set to 0 for instant. (default: 1)
 * sm_botspawns_max_spawn_delay: Max delay in seconds for spawning. Set to 0 for instant. (default: 15)
 * sm_botspawns_spawn_sides: Spawn bots to the sides of the players when facing the next objective? (default: 1)
 * sm_botspawns_spawn_rear: Spawn bots to the rear of pthe players when facing the next objective? (default: 1)
 * sm_botspawns_min_player_distance: Min distance from players to spawn (default: 1200)
 * sm_botspawns_max_player_distance: Max distance from players to spawn (default: 16000)
 * sm_botspawns_min_objective_distance: Min distance from next objective to spawn (default: 1)
 * sm_botspawns_min_counterattack_distance: Min distance from counterattack objective to spawn (default: 3600)
 * sm_botspawns_max_objective_distance: Max distance from next objective to spawn (default: 12000)
 * sm_botspawns_min_frac_in_game: Min multiplier of bot quota to have alive at any time. Set to 1 to emulate standard spawning. (default: 0.75)
 * sm_botspawns_max_frac_in_game: Max multiplier of bot quota to have alive at any time. Set to 1 to emulate standard spawning. (default: 1)
 * sm_botspawns_total_spawn_frac: Total number of bots to spawn as multiple of number of bots in game to simulate larger numbers. 1 is standard, values less than 1 are not supported. (default: 1.75)
 * sm_botspawns_min_fireteam_size: Min number of bots to spawn per fireteam. Default 3 (default: 3)
 * sm_botspawns_max_fireteam_size: Max number of bots to spawn per fireteam. Default 5 (default: 5)
 * sm_botspawns_stop_spawning_at_objective: Stop spawning new bots when near next objective  (default: 1)
 * sm_botspawns_remove_unseen_when_capping: Silently kill off all unseen bots when capping next point  (default: 1)
 * sm_botspawns_spawn_snipers_alone: Spawn snipers alone, can be 50% further from the objective than normal bots if this is enabled? (default: 1)
#### Todo
[X] Instead of spawning all bots in one spot, spawn them at hiding spots in the navmesh
[X] Find path between current and next point, add bots around that axis
[X] Add option for minimum spawn distance to keep bots from spawning on top of players
[X] Create variables for how far off the path to spawn
[X] Create option to either spawn and keep X number of bots in game, or simply spawn on random timer (also an option)
[X] Create functionality to respawn bots to simulate more bots than game can support
