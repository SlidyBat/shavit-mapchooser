# shavit-mapchooser
A SourceMod mapchooser plugin designed for use with shavits timer

## Available ConVars

 - smc_maplist_type (Default = 0, Min = 0, Max = 2) - Where the plugin should get the map list from. 0 = zoned maps from database, 1 = from maplist file (maplist.txt), 2 = from maps folder
 
 - smc_mapvote_blockmap_interval (Default = 1, Min = 0) - How many maps should be played before a map can be nominated again
 - smc_mapvote_enable_novote (Default = 1, Min = 0, Max = 1) - Whether players are able to choose 'No Vote' in map vote
 - smc_mapvote_extend_limit (Default = 3, Min = 0) - How many times players can choose to extend a single map (0 = block extending)
 - smc_mapvote_extend_time (Default = 10, Min = 1) - How many minutes should the map be extended by if the map is extended through a mapvote
 - smc_mapvote_show_tier (Default = 1, Min = 0, Max = 1) - Whether the map tier should be displayed in the map vote (currently only available through with smc_maplist_type 0)
 - smc_mapvote_duration (Default = 1, Min = 0.1) - Duration of time in minutes that map vote menu should be displayed for
 - smc_mapvote_start_time (Default = 5, Min = 1) - Time in minutes before map end that map vote starts
 
 - smc_rtv_allow_spectators (Default = 1, Min = 0, Max = 1) - Whether spectators should be allowed to RTV
 - smc_rtv_minimum (Default = -1, Min = -1) - Minimum number of points a player must have before being able to RTV, or -1 to allow everyone
 - smc_rtv_delay (Default = 5, Min = 0) - Time in minutes after map start before players should be allowed to RTV
 - smc_rtv_required_percentage (Default = 50, Min = 1, Max = 100) - Percentage of players who have RTVed before a map vote is initiated
 
## Available Commands

### Admin Commands

 - sm_extend (ADMFLAG_CHANGEMAP) - Admin command for force extending map
 - sm_forcemapvote (ADMFLAG_RCON) - Admin command for forcing the end of map vote
 - sm_reloadmaplist (ADMFLAG_CHANGEMAP) - Admin command for forcing maplist to be reloaded

### Player Commands

 - sm_nominate - Lets players nominate maps to be on the end of map vote
 - sm_unnominate - Removes nominations
 - sm_rtv - Lets players Rock The Vote
 - sm_unrtv - Lets players un-Rock The Vote
