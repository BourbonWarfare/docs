# Configuring Loadouts

## CfgLoadouts

The framework will have a **CfgLoadouts.hpp** file. Open it with your preferred text editor. You will see at the top that you can toggle settings such as changeable optics or wiping vehicle cargo as described below:

* Turn on magnified optics: `allowMagnifiedOptics = 1; // 0 is off`
* Turn on vehicle inventories: `setVehicleLoadouts = -1; // 0 is vanilla, 1 is using the vehicle loadout script`
* Turn off the "fallback" class `useFallback = 0; // 1 is on`

Scrolling down to the bottom, you will find where the loadouts are specified for each team in your mission. By default the selections will be vanilla Arma 3 assets:

<pre class="language-C++"><code class="lang-C++"><strong>// West factions
</strong><strong>#include "Loadouts\west_gear.hpp"                    // Faction specific gear
</strong>class potato_w { // Blufor
    #include "Loadouts\Blufor\us_mx_mtp.hpp"         // Current loadout selected
};
</code></pre>

The framework comes supplied with a handful of loadout files that are ready for use. The **CfgLoadouts** file lists them out. Let’s say you want Blufor to be Germans with G36s. By default Blufor will have **Loadouts\us\_mx\_mtp.hpp**. Simply find this entry (line 83) and change it to **Loadouts\ger\_g36\_fleck.hpp**.&#x20;

**DOUBLE CHECK THE SPELLING, BECAUSE IF YOU REFERENCE A FILE THAT DOESN'T EXIST THEN YOUR MISSION&#x20;**_**WILL**_**&#x20;CRASH ON MISSION LOAD.**&#x20;

Additionally, you’ll see another entry for Blufor such as **#include “Loadouts\west\_gear.hpp”**. Similar includes exist for Opfor and Indy. Do not modify or delete these entries. They are required for every mission, regardless of chosen loadout. If you have your mission open then you will need to reload it in order for Blufor’s loadout change to take effect.

_Note: West is always Blufor and East is always Opfor._
