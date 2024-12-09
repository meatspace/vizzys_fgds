
Hello. This is my attempt to make Hammer more bearable to use with more icons for various entity's. My thinking is any icon is better than a blank one!

-- // MAPBASE CHANGELOG // --
• added detailed info for many entities (taken from Brokk's / Pinsplash's .fgd's)
• added input SetLightingOriginHack (Deprecated, but why not. https://user-images.githubusercontent.com/11617079/109691349-65e9d200-7b98-11eb-8739-ae77a1f5999c.jpg)
• added input KilledNPC to basecompanion
• added output OnNextPoint to func_tracktrain ("Fires every tick as the train moves. Activator is the path_track being traveled to.") might be better in in basetrain? idk without testing
• added input Toggle to func_brush
• added missing spawnflag for npc_manhack "Carried"
• added input HideWeapon to weapon baseclass ("If the weapon is being held by someone, makes it invisible. The weapon will reappear if they switch weapons.")
• added line helpers to the following entities:  phys_keepupright, point_entity_finder, npc_template_maker, ambient_generic, light_spot, light_dynamic, env_sun, info_ladder_dismount	(Thanks SirYodaJedi / Koetekishi Yui)
• changed env_break_shooter to inherit from gibshooterbase (hopefully i didn't...break the shooter 😎)
• added missing weapons to npc_maker now that pretty much every human npc can wield everything
• added input DispatchEffect to baseio ( https://developer.valvesoftware.com/wiki/List_of_Client_Effects ) 
• added input DispatchResponse to TalkNPC (I have no idea how this works, but it was missing)
• added missing keyvalue detailOrientation to prop_detail
• added input Agitate for npc_antlion_grub (it makes them cry for X seconds)
• added missing grenade_helicopter spawnflag: [1] Megabomb (seems to be the default kind dropped from heli's: silent and explode on a timer. unlike the other type that activates on gravity gun pickup)
• added missing ai_sound soundcontext choice: 536870912: "Player vehicle: Sound comes from a vehicle. Hunters will prepare to dodge."
• added missing targetname class for npc_heli_avoidbox 
• added target keyvalue for func_lookdoor (kinda useless without it, not that anyone uses this obscure entity)
• added missing damage filter types to filter_damage_type (with better descriptions for some via Pinsplash .fgd's)
• added missing Enable Gun keyvalue for prop_vehicle_jeep_old (didn't seem to inherit)
• added input ScriptPlayerDeath to scripted_sequence (not on VDC yet) 
• added missing DamageForce override keyvalue for env_explosion (buggy apparently)
• added missing basedoor "Linked Door" field 
• added missing basedoor spawnflag: 65536 : "New +USE Rules - If closing, allow +USE to reopen 
• added inputs Enable, Disable, DisableFloating for func_physbox
• added 22 base hl2 soundscapes to the list. mostly atmospheric, generic ones with few random sounds. (adding all of them would take too long and make me want to kms.)
• added inputs that were missing for logic_mirror_movement (thank VDC)
• added commentary_auto entity icon
• added commentary_auto / point_commentary_node entities and their various values. (point_commentary_node is still missing Mapbase's node types idk how to add them rly)
• added input _OnLogicBranchRemoved to logic_branch_listener (this ain't even on the VDC yet "Sent automatically by a logic_branch when it gets removed for any reason. The !activator will no longer be watched by this entity. Makes the entity fire an output, but only if the listener's final result has changed." according to Pinsplash)
• added helper sphere to point_playermoveconstraint
• added input Color for env_embers
• added input Break for prop_door_rotating (use phys_convert instead)
• added inputs Noise, ColorRedValue, ColorBlueValue, ColorGreenValue to env_laser
• added missing keyvalue BoltWidth to env_laser, defaults to same value as env_beam (2 units)
• added missing spawnflag "Repeatable" to env_shooter / env_rotorshooter (inspired by Pinsplash's .fgd's)
• added input LightWorld to env_projectedtexture (kinda useless unless you've used LightOnlyTarget)
• added Enable, Disable, DisableFloating inputs to func_physbox (inspired by Pinsplash's .fgd's)
• fixed the helper lines for path_corner by copying how path_track does it (idk why they weren't working before)
• removed func_fish_pool's default model as no fish model exists in hl2 files. Grab some fish models from counter-strike: source!
• func_doors now have "touch opens" flag turned OFF by default. This ain't DOOM
• added "Start Active" spawnflag for point_hurt, DISABLED BY DEFAULT (you must enable it before sending a start input I believe )
• added "512x512" cubemap size option. ("1024x1024" and up exist but VDC says they can cause engine error crashes so I didn't add them)
• added input SpeakIdleResponse to npc_citizen
• added input JumpAtTarget to npc_antlion
• added inputs Alpha, Color to env_fade / env_smokestack / env_steam
• added rendermode 8 "Alpha Add" to BaseBrush class. ("Functions similarly to Additive, except the alpha channel controls the opacity of the sprite. For dark sprites, an example material being sprites/strider_blackball.vmt.")
• added input GetFMod to point_posecontroller
• added input SetCharge to item_suitcharger
• added inputs FadeAndRespawn and Socketed inputs to prop_combine_ball
• added missing filter_combineball_type filter type: "Being held by the gravity gun" (renamed physcannon to gravity gun here)
• added input FlyToPathTrack to BaseHelicopter 
• added SetHandModel / SetHandModelSkin inputs for logic_playerproxy. They might be deprecated / obsolete by Mapbase, not sure. Cant hurt to add them.
• added line helper for point_tesla (inspired by Da Spud Lord's TF2 .fgd)
• added missing "Underwater light mutation" light appearance flicker/pattern choice (inspired by Da Spud Lord's TF2 .fgd)
• New base icons: point_message_localized, filter_activator surface, filter_activator_squad, filter_redirect_owner, filter_redirect_inflictor, filter_redirect_weapon
• Updated old icons:  npc_bullseye (was crusty), point_copy_size (fits more), env_spritetrail (its better), logic_achievement (removed underscore), env_closedcaption (forgot the d in closed), info_target_gunshipcrash (added alien gunship), phys_ragdollmagnet (more accurate), info_target_helicoptercrash (it's red now), info_player_view_proxy (glasses have anime glow)
• updated to Mapbase 7.2 versions .fgd's
• fixed even more typos
--// older version stuff //--
• fixed npc_fisherman model path being barney for some reason (valve pls fix)
• added output OnCrashed for info_target_gunshipcrash (not OnCrash, whoops) recommended by Xblah
• env_smokestack, phys_thruster and phys_torque have been changed to a grey directional arrow model (made by ficool2) for better directional placement
• added an icon for env_rotorwash
• added output Onspark to env_spark
• fixed many typos in both .fgd using spellcheck (in descriptions only)
• added input SetMaxDensity to env_fog_controller 
• added inputs for env_spritetrail 
• added input SetMaxPieces to game_weapon_manager 
• added input UseRandomTime to logic_timer
• added input SetTargetEntity to point_anglesensor 
• added input SetFogMaxDensity to sky_camera 
• added input _DisableUpdateTarget and _EnableUpdateTarget to momentary_rot_button (yes the underscores are intentional)
• added inputs SetCycle, SetModel, and SetPlayBackRate to prop_door_rotating, phys_magnet, prop_dynamic, prop_dynamic_override, prop_dynamic_ornament, prop_physics_override, prop_physics, prop_physics_multiplayer, prop_sphere, prop_ragdoll, prop_ragdoll_attached, player/logic_playerproxy


--// INSTALL INSTRUCTIONS //--
Ideally you can just copy the shared_misc folder over the one in /sourcemods/mapbase_shared/shared_misc/bin 
Or manually copy the base.fgd / halflife2.fgd over the ones at:	 /sourcemods/mapbase_shared/shared_misc/bin 
Also, copy the materials/models folders over your own mods or the new icons will show up as checkerboard missing textures.
(remember to do this again if you are upgrading from a previous version)
If something breaks or you don't like it, simply redownload the official Mapbase release and overwrite the .fgd's with the originals.


--// CREDITS //--
Id like to credit the following people:
Ficool2: https://ficool2.github.io/HammerPlusPlus-Website/
To my knowledge all icons in the editor-ficool folder were created by them. I painstakingly copy/pasted each icon from their tf2 ultimate .fgd (downloaded from tf2maps.net) over to the Mapbase .fgd 
I edited and reused a few of their icons as well.

Blixibon: https://github.com/mapbase-source/source-sdk-2013
I edited and reused a few of their Mapbase specific icons such as logic_script and damage_info for example.

TeamSpen210: https://github.com/TeamSpen210/HammerAddons
Some icon entity's like point_entity_finder are by them, and I based the icon point_advanced_finder (a similar Mapbase entity) off of it as well. 

Valve Developer Community: https://developer.valvesoftware.com/
Tf2maps.net: https://tf2maps.net/
A Boojum Snark: https://tf2maps.net/downloads/ultimate-mapping-resource-pack.510/
The Spud Lord: https://tf2maps.net/threads/an-fgd-fit-for-a-lord.41812/
Brokkhouse: https://tf2maps.net/downloads/an-fgd-fit-for-a-lord-brokk-edition.15924/
Pinsplash: https://github.com/Pinsplash/SEFGD
All valuable reference points using their combined .fgd knowledge.

Vizzys: https://developer.valvesoftware.com/wiki/User:Vizzys
Yep that's me, I wrote this. And I made the bad icons. I'm thanking myself. (send help)


--// ADDITIONAL INFO //--
Some entities such as env_splash, env_dustpuff, env_citadel_energy_core and env_flare cannot have custom icons because the scale keyvalue parameter affects the icons and makes them super huge. (a hammer bug or likely oversight by Valve)
Another hammer feature/bug is is if the entity supports a color value it will change the icons color as well making it potentially unreadable. This can really only be fixed by making the icon an outline or 3d model AFAIK.
The closed caption logo used for env_closecaption is public domain.
Entity's I learned are not in Mapbase .fgd's for whatever reasons and you may want to add someday:
prop_detail_sprite, env_detail_controller, weapon_oldmanharpoon, target_changegravity


--// TO-DO LIST //--
Need someone to hex scriptedsequence.mdl and use it for func_useableladder/func_ladderendpoint if such a thing is possible.
info_ladder_dismount could use a hexed version of info_node's model too perhaps.
looking into Shadow Cast Distance (shadowcastdist), vrad_brush_cast_shadows, etc
change physcannon / physgun to gravity gun in more descriptions
add env_spritetrail animated keyvalue (idk if its safe to add without testing)

--// END NOTES //--
Lastly, I've included the photoshop .psd file sources of the icons I've created and/or edited. 
As well as the hammer font source .psd file. It is based on Blixibon's work. I merely cut the characters into individual letters, numbers, and common entity prefixes.
That's everything, go away now.