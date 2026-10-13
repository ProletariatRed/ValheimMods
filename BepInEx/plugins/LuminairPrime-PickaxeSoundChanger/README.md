I vibe-coded this BepInEx plugin to replace the annoying pickaxe sound effects with more mellow sounds that are already in the game. The new pickaxe basically sounds like the regular axe. This is good if you feel misophonia for high-pitched metal-on-metal sounds, but I think it's also good for anyone because the default sounds are so loud and obnoxious lol. By default, Valheim plays metal-on-metal sounds even when you hit a TREE with a BONE pickaxe... that's unhinged!!!

This plugin contains ZERO sound files. Instead it re-routes existing game sounds.

I over-designed this plugin: you can replace almost any sound with any other sound, or mute any sound, or change the volume and pitch of any sound. To find a sound name, turn on "Log Sound Names" and copy the sound variable name from the BepInEx console log. The syntax for the Sound Mapping field is: "original_sound = replacement_sound", or "original_sound = mute", or just "original_sound". You can make adjustments to volume and pitch, but Valheim's pitch shifter isn't very good, so don't go much below 1.0 haha.

By default, pressing "K" turns the sound changes off and on for comparison. Valheim doesn't use K normally, so this is a cool way to compare how insane the normal sound effect is. You can disable the hotkey by deleting the K in the settings.

Detailed reasoning: depending on what target you hit with the pickaxe, Valheim will play one or both of 1) sfx_pickaxe_hit (very high-pitched) and 2) sfx_rock_hit (still surprisingly high-pitched). They sound like chiseling a church bell or smashing champagne glasses together. My fix idea is to replace the sfx_pickaxe_hit sound with the REGULAR axe sound (sfx_axe_hit) because the regular axe sound is more mellow. But after that change, I noticed that some pickaxe targets will trigger a DIFFERENT annoying sound effect: sfx_rock_hit.

For sfx_rock_hit I swapped in the sfx_rock_destroyed effect at a very low volume. This provides the feeling of rubble breaking off the target for every hit. When combined with the axe sound effect, the pickaxe almost sounds like it's supposed to be that way!

Note: sounds named sfx_* aren't actually sound files; they are lists (arrays) of sound files that are played randomly for variety. There are usually several actual sound files behind each sfx_* array in the game.
