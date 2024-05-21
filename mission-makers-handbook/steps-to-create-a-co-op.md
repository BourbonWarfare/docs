# Steps to Create a Co-op

Most of the relevant info to "building" the mission has already been gone over in the previous sections, so this page will simply contain all Co-op relevant information.

## Zeus' Intent

The purpose of a Zeus is like a conductor - to guide and shape the encounters of a mission in a way that feels organic and spontaneous. Playing to "win" is not the objective of the Zeus - creating interesting and dynamic fun for the most amount of people is the goal. Give challenges to your players, and keep in mind the little immersive sensibilities like not spawning units in line of sight of players. This is where you want to specify how you want the pacing of your co-op to go, as well as what assets to use, and other specific information you want the Zeus/co-zeus to know.

## Spawning Units

When you are zeusing a co-op, use the Potato modules to spawn AI. These modules can be found in Systems > Modules > POTATO HC: East (West, Independents). These spawned units will have the gear script run from the loadout file that you define for that faction. During the mission making process, you can also place down vehicles some place far away from the main AO and add a side appropriate potato HC AI next to them. That way, when the mission loads in, you’ll have a premade ‘motor pool’ of sorts that will show up in each side’s spawner module.

If you have a specific camouflage that you'd like the vehicles to use, make sure to go into the vehicle/vehicles attributes while in the editor/mission making, scroll down to "POTATO" and select the "Copy Custom Garage Appearance" option. This will ensure POTATO spawns the vehicles with the correct vehicle "skin".

Note: _HC stands for headless client_

What is the headless client, you may ask? Well instead of AI logic being calculated on the server, it is instead done on the headless client. This saves some server resources. In general, it’s best to use HC AI.

You can use POTATO HC:Custom > Spawn-a-vic or Spawn and Garrison Units to create/crew any vehicle or spawn and garrison units. These modules are pretty self explanatory: just plop one down on the map, and follow the on-screen menu.

There are two other modules in POTATO > Utilities that are worth mentioning. The first is “Move all AI to HC”. What this does is self explanatory. If you are Zeus and notice the mission maker has a bunch of placed (non-HC) AI, then simply use this module to migrate all AI to the headless client.

The other module is Global Set AI Skill. This module lets you tune AI accuracy, aim speed, spotting distance, and more. This is a good module to change ad-hoc during a mission given the present scenario. A good general rule is to start the co-op with the AI having lower accuracy, higher aim shake, and higher aim time in order to keep players from being 1-shot too frequently. Another option would be to turn off cover and suppression to make AI more aggressive but less accurate, but all this is up to you as Zeus.

There are various other modules that I recommend checking out, such as POTATO factory. From Potato Factory you can set what side you want it to spawn, and in what vehicles.

Beneath this is Editor specific, non-zeus ways to spawn initial contact.

### Using POTATO: HC prebuilt units

When to use this: If you want to place a generic group/vehicle in a general place, to be maneuvered later by zeus.

How to use this: In the 3DEN editor, go to the modules tab and look for the categories labeled like "POTATO HC: East". When you open this category there should be a decent sized list of units/groups you can set down. When you place the module down, there should be a generic "logic" icon placed on the map. When you load this mission, the module will spawn the selected group/unit at that position.

### Using POTATO: HC garrisoning

When to use this: If you need units it occupy buildings in a town, this module is for you

How to use this: In the 3DEN editor, go to the modules tab and look for the category labeled "POTATO HC: Custom". When you open this category look for the "Spawn and Garrison units" module. Place this in the center of the town you want to garrison. When you place the module down, there should be a generic "logic" icon placed on the map. Double click this module, and you should be able to edit the attributes of the module. You can set: the factions of the units to spawn, the radius from the placed module to search for homes, the chance that each home will be occupied (You probably want to set this from 15-30, but it really depends on the size of the town), the minimum units to place in each house, and the maximum units to place in each house. Once the mission loads, the garrison script will run, populating one house every .25 seconds.

Notes: The maximum number of units to spawn per placed module is defaulted to 100, this can be changed mission side though. You can also change the factions the zeus can place, as well as change the units the script will spawn. Add/configure this in your mission's description.ext file to customize this module:

```C++
class CfgGarrison {
    maxUnits = 70; // change max units spawned per module to 70

    class blu_f {
        units[] = {"B_soldier_F"}; // change it so the NATO faction will only spawn riflemen
    };
    
    class opf_g_f { // add new faction (only works for zeus)
        units[] = {"O_G_Soldier_F","O_G_Soldier_F","O_G_Soldier_SL_F"}; // note: these units are randomly selected, so there's a 1/3 chance to get an SL, 2/3 chance for a rifleman
    };
};
```

### Using POTATO: HC send group to HC

When to use this: If you can't find the groups/vehicles you need to place, or you want precise control over where the unit's are placed or give them waypoints or set unit stances in the editor.

How to use this: In the 3DEN editor, place your groups as usual, do what you want to them. When you have them set up, double click on the groups you want to move to the HC, go to the "POTATO: HC" attribute group, and check the "Move Group to HC" box. When the mission loads, it will move each checked group to the HC.

Note: this method uses [setGroupOwner](https://community.bistudio.com/wiki/setGroupOwner) which does use a decent bit of bandwidth, so if possible use the above HC options.

## Respawns

Deciding whether or not to utilize a respawn in a co-op is ultimately up to the Zeus, but here are the steps involved:

1. Place Module > POTATO: Respawn > Respawn Point (put this at the location where you want people to respawn)
2. Place Module > POTATO: Respawn > Open Respawn. In the below picture, first select faction (CSAT is Opfor, and NATO is Blufor). Next, Group is the element that you want to respawn (IFV, SL, fireteam, etc.). Config is the callsign that will be associated to the respawn group (be sure to pick something not in use). Clicking Add will add the specified element to the list of respawns. Clicking Open Respawn will now allow players to slot what you’ve chosen. Clicking Trigger Respawn will respawn the players.

<figure><img src="https://lh7-us.googleusercontent.com/d7YhsPScHQPn-GH940nfZbWZA-_f1YtLh9A307XQGuGk1sYfu8eLrDJtM_MeBt4MTg8kI24tu0aFT86ILrPwWZ9k8n11UNfKA1APCw3-vyEAY3oYt0M-nA3rRLWWVFat0B7n7kusPxLPA1bcc0YF" alt=""><figcaption></figcaption></figure>

## Considerations and Caveats

This guide does not intend to tell you how to Zeus. Rather, the goal is to point out useful tools/modules that can help you facilitate your Zeus plan. I openly encourage asking any Zeuser any questions about assets/strategy/etc. because there are a lot of whack things in Arma that will just simply come from experience. I recommend asking #mission-making or and they will be more than happy to set some time aside to work with you on something. Just give people a heads up.

\
Our co-ops take place over kilometers, whereas TvTs are more focused. Objectives are very cut-and-dry in TvTs. Co-ops might be different. Co-ops have way more moving parts, considering factors such as player assets, AI assets, terrain involved, mission objectives, and time allotted. Sometimes players will do something that you (the mission maker) did not account for, such as ditching transport vehicles. These are all situations that you (the Zeus) will have to deal with ad-hoc. These are situational cases where there are a lot of factors in play and no scenario is ever the same. This is the part that will come with experience; how to dynamically adjust is what truly makes for interesting missions!\
\
Again, direct any questions to #mission-making. Members there will answer your questions to the best of their knowledge.
