---
description: 'Author: Raeth'
---

# Crash Course: RHS Armor FCS

So, in the interest of being a nice guy I've decided to write a quick and dirty guide on using the advanced RHS armor systems. This guide is not comprehensive, and is meant more to serve as a quick reference guide. It is split into multiple parts

## Initial Configuration of keybinds

So, if it's your first time ever operating an RHS vehicle you're in for some work, but this should at least get you started quickly.\
1\. Press escape\
2\. Press the button "RHS - Game Options", it should be about midway down your screen, between "Paused - Name" and "MSG ADMINS"\
3\. Once in the menu, I recommend unchecking "FCS Target Lead", because I will not be covering its correct usage in this guide, nor to I recommend using at all, primarily because it doesn't work very well, guessing leads tends to be more reliable.\
4\. Under Vehicles, bind every option with the exception of "Dump Lead" to a key that is currently not in use inside a vehicle, be mindful of radio hotkeys as they are used in vehicles. Your RHS menu should look something like this when you are complete:\
[http://i.imgur.com/8N1h9rl.jpg](http://i.imgur.com/8N1h9rl.jpg)\
4a. I recommend setting multiple keybindings for "Lase Target" as it is the most common button you will be pressing, and you want to have absolutely no confusion over which key it is. For me I can press either Ctrl + T, Alt + T, or Ctrl + Alt + T, meaning that any combination of ctrl/alt + T will lase the target.\
4b. To go along with Part a, I recommend you bind it to some combination of keys, as while it's important you press it quickly in a jam, you don't want to fat finger it when you're up shit creak and lose your range settings.\
5\. To to your normal arma 3 keybinds, and double check that you have no overlapping hotkeys with the keys you just set, this is extremely important to prevent accidents.\
6\. Under "Weapons" near the button make sure you have "Countermeasure" bound. (I use R.)\
7\. Under "Vehicle Movement" Towards the bottom bind "Turn In", make sure it's a key easy to press in a pinch, as your ability to reach that key can mean life or death.\
8\. (Optional) Under "Vehicle Movement" Towards the button, bind Aim up, Aim down, Aim Left, Aim right and Turn out, using the aim up down left and right keys when making large traverses of the turret/command cupola makes things a lot easier, and having a hotkey to turn out prevents "Get out" accidents when using your action menu.\
9\. (Optional) Under "Vehicle Movement" Midway down, if you intent on using WHEELED vehicles a lot, you can bind the hand break, keep in mind it does not function in tracked vehicles at this time.

## Basic Armor Recognition

There are a lot of different classification systems used for identifying armor, here I'm going to list the two most common ones within the context of arma (note: These are far from realistic, I know that)

### Three Class Weight System

"Light" Armor - > This encompases all soft vehicles. ALL unarmed vehicles fall into this category, as well as a limited number of armed vehicles, primarily MRAPS or technicals. If your Rifle or Grenade Launcher can take it out, it's probably light. If it has a canon of any kind, it is NOT a light vehicle, see Medium. Ex: Humvee, Technical, Strider, Ifrit, Hunter, Soviet on a bad day, HEMMETS, Urals, and that weird tracked Russian transport amphibious thing and traditional Strykers.

"Medium" Armor - > This encompases all soft vehicles that have canons or autocannons, as well as vehicles with a decent amount of Armor. The rule of thumb here is, if it's it got any kind of canon, auto or not, plus you can take it out with squad-based AT or Grenade Launchers, its medium. Ex: The BTR, BMP, and BMD series, bradley's, Marshals, Stryker Mobile Gun System (because it has a canon), LAV-25 or your respective equivalent.

"Heavy" Armor - > Anything with "Tank" In its name (Main Battle, Heavy, Medium, Light, Scout, etc) or Self Propelled Guns. Ex: T-72, T-34, Sheridan Light Tank, Paladin Self Propelled Gun, Abrams.

Now, this system is not perfect. There are some overlaps and grey areas, for instance, where does an AAV fall? It has a decent amount of armor but it does not fulfil the requirement of having a canon for medium armor. If you're not sure what a specific vehicle is and you want to call it out using this system, error on the side of caution and call it one level above whatever you think it might be. The other primary problem with this system is it can be a bit ambiguous as to where things go, for instance A Sheridan "Light" Tank is "Heavy" armor because, at the end of the day, it's a fucking tank.

### Four Class Type System

"Soft" - > This encompassses any soft target, ranging from cars to most MRAPS. All Unarmed vehicles go here. Ex: Humvee, Ifrit, Hunter, Urals.

"APC" - > Armored Personnel Carriers, this is any vehicle that has wheels, a gun on the roof and can carry people behind armor, regardless of type. Ex: BTR series, Stryker both MGS and standard, even some big MRAPs fall under this.

"IFV" - > Infantry Fighting Vehicles, this is generally anything that carriers people behind armor and has tracks, but is NOT a full blown tank. Ex: BMD and BMP series, as well as the Bradley.

"Tank" - > Just like heavy armor, this is ANY type of tank, light medium or heavy. Ex: T-72, Abrams, T-64, T-34, T-80.

This system isn't really perfect either, while it's much more defined in each category, it has the problem of not accounting for everything you might see, it could also be ambiguous as to what exactly you're talking about when you say and "IFV", as that could range from a scout BMP to a BMD-4 with it's smooth bore plus Autocannon ATGM goodness. Because of this, only use this system if you don't have a good look at whatever you're seeing, for instance if you see tracks and an elongated rear section, call it an IFV just to be safe. If you see a turret and tracks, call it a tank. Once you gather more information about the target, its a good idea to be more specific and update your commander/Markers on the map.

### Summarizing Recognition

If you can't identify the specific type of vehicle but know what kind of armament and armor profiles it has, it's generally a better idea to use the first system. If you can't identify the vehicle and don't know much about its armament or armor profiles, use the second system. In a perfect world neither of these systems will be used, because eventually you should begin to memorize the shapes of various vehicles and be able to call of specific types, for Instance, BTR - 80A versus a BTR - 70, or even just identifying the differences between a BMD or BMP.

## Now for the Actual Fire Control Systems

This is where things get hard, because there are a lot of different forms of these systems, I'll be dividing them up into categories and summarizing them here, if you want to know which specific vehicles use which specific systems, check the armor quick reference handbook.

### American Light System

This is just the default Arma 3 system, used primarily by mounted crew served weapons. There is no rangefinder. To operate:

1. Aim at your target and get a general idea of range either by map, nearby elements, or guesswork.
2. Use the default Arma 3 zeroing keys (Page up and down, depending on your bindings) to change your range, which is displayed in the top right hand corner in meters.
3. Fire a small burst, then correct your shot. If your shots deviate significantly, adjust your range settings. Important Note: This system is not widely implemented in RHS vehicles (or most vehicles, for that matter) in Arma 3 and has significant bugs, for instance when aiming down sites on GMG's, using the adjust keys may not function. When in doubt, zero to 300 and try your best.

### American Medium System (Default ACE)

This is probably the easiest system by far in our modpack, it's not actually an RHS system but because some RHS vehicles use it (and people often confuse it with an RHS system) I'll be covering it here anyway. It's as simple as doing the following:

1. Point canon at (hopefully) hostile target
2. Hit tab (Note: Not covered in keybind guide, if TAB does not work for you, check your ACE 3 keybinds, "Ace3 Vehicles" under "Lase Target / Measure Distance), somewhere on your screen a number will appear/change to the current range of the target.
3. Pull the trigger. NOTE: Ballistics of all weapons are shared, so re-measuring after ammo or weapon change is not required.

### American Heavy System

This is the most basic fully-RHS based system, and it is currently only used in the Abrams series. Using it is very simple:\
1\. Select Type of Ammo and make sure the gun is loaded.\
2\. Aim at target, and use your RHS "Lase Target" Keybind. This will begin the lasing process.\
3\. At the bottom of your screen, a range should appear in green lettering, be mindful it may appear behind your shacktac HUD. This is the range calculated by the rangefinder, and it has automatically transferred this range into the ballistic computer. Manual range entry is NOT required.\
4\. To the left and slightly above the range number, a green square will appear. This means that the rangefinder is capable of operating again.\
Note: Due to an engine limitation, the green square will not appear if the rangefinder currently is not set to a range, this occurs just after you enter the vehicle, an indication that the green dot will not appear is the green numbers displaying random numbers or jumping around when the canon is moved. Simply find a range to correct this.\
5\. Fire your first shot at the target, be mindful not to switch ammo types between lasing and firing.\
6\. Depending on terrain, elevation, and a number of other factors, your first shot will likely not hit its target. **Do not re-lase the target if you miss, just correct off the impact.**\
7\. Repeat (without re-lasing unless the range has been significantly changed) until the target is dead.\
\
Things to be mindful of in this system:\
1\. Firing outside of maximum range of your selected weapon will produce strange results, this is most notable when firing coax weapons at long distances (Usually >1km)\
2\. As far as I can tell, the system assumes that you're firing from sea level to another target at sea level, so the greater the elevation differences between you and the target, the more likely the first shot will miss.\
3\. The rangefinder has a minimum range of about 300m, within this range the rangefinder will automatically select 0000, this is because differences within this range are negligible.\
4\. Arma can be really fucking weird sometimes and this system can be unreliable, at the end of the day, this system is not a replacement for good aim and shot correction. If the rangefinder is giving you crazy ranges or missing by a lot, range something within minimums to reset the range to 0000 and fire manually.

### Russian Light System

Use Optical Sights, no zeroing or rangefinders (I might expand this later to describe how to use said sights, but at the time of posting I actually don't know how)

### Russian Heavy/Medium Basic (Functioning) System

This system works extremely similarly to the American Heavy System, using it is fairly simple:\
1\. Aim at your target and select ammo type using your action menu\
2\. Press your lase target hotkey, a four character number should appear in the upper center portion of the screen.\
This is the range calculated by the rangefinder, and it has automatically transferred this range into the ballistic computer. Manual range entry is NOT required.\
3\. Fire your first shot. Depending on terrain, elevation, and a number of other factors, your first shot will likely not hit its target. **Do not re-lase the target if you miss, just correct off the impact.**\
4\. Correct off your first shot and eliminate the target.\
\
Things to be mindful of in this system:\
1\. Different weapons have different ballistic characteristics, make sure you re-lase after changing weapons to ensure the correct ballistics are used in the calculations.\
2\. Firing outside of maximum range of your selected weapon will produce strange results, this is most notable when firing coax weapons at long distances (Usually >1km)\
3\. As far as I can tell, the system assumes that you're firing from sea level to another target at sea level, so the greater the elevation differences between you and the target, the more likely the first shot will miss.\
4\. The rangefinder has a minimum range of about 300m, within this range the rangefinder will automatically select 0000, this is because differences within this range are negligible.\
5\. Arma can be really fucking weird sometimes and this system can be unreliable, at the end of the day, this system is not a replacement for good aim and shot correction. If the rangefinder is giving you crazy ranges or missing by a lot, range something within minimums to reset the range to 0000 and fire manually.\
6\. If you're firing an ATGM range is generally irrelevant, as it tracks your mouse.

### Russian Medium Advanced (WIP) System

This system is used on a limited number of RHS vehicles and it can be difficult to identify, if you have a TV screen looking optic, with a range that changes depending on what you are currently looking at, you are using this system. This system is not corrected implemented and does not function past a basic rangefinder. If you find yourself in a vehicle of using this system, its all eyeballs for you.

### Russian Heavy/Medium Advanced (Functioning) System

This system works extremely similarly to the American Heavy System and Russian Medium Basic, with the exception that it looks like you're looking at a TV instead of down a scope.\
1\. Aim at your target and select ammo type using your action menu\
2\. If you see ссу вкл and nothing else on the screen, zoom in one level.\
3\. Press your lase target hotkey, a four character number should appear in the lower right hand quadrant of the screen.\
This is the range calculated by the rangefinder, and it has automatically transferred this range into the ballistic computer. Manual range entry is NOT required.\
4\. Fire your first shot. Depending on terrain, elevation, and a number of other factors, your first shot will likely not hit its target. **Do not re-lase the target if you miss, just correct off the impact.**\
5\. Correct off your first shot and eliminate the target.\
\
Things to be mindful of in this system:\
1\. Different weapons have different ballistic characteristics, make sure you re-lase after changing weapons to ensure the correct ballistics are used in the calculations.\
2\. Firing outside of maximum range of your selected weapon will produce strange results, this is most notable when firing coax weapons at long distances (Usually >1km)\
3\. As far as I can tell, the system assumes that you're firing from sea level to another target at sea level, so the greater the elevation differences between you and the target, the more likely the first shot will miss.\
4\. The rangefinder has a minimum range of about 300m, within this range the rangefinder will automatically select 0000, this is because differences within this range are negligible.\
5\. Arma can be really fucking weird sometimes and this system can be unreliable, at the end of the day, this system is not a replacement for good aim and shot correction. If the rangefinder is giving you crazy ranges or missing by a lot, range something within minimums to reset the range to 0000 and fire manually.\
6\. If you're firing an ATGM range is generally irrelevant, as it tracks your mouse.

### Russian Heavy Basic (Version 1) System

This is the system used by many Russian Main Battle Tanks. Today, this version is used primarily in export versions of the tanks, as most vehicles have been upgraded to the advanced system within Russia. **Using it can be quite challenging, so I recommend you experiment with it in the editor prior to slotting a vehicle that uses this system.**\
1\. Select the "Fire Control System" weapon using your switch weapon keys.\
2\. Click the fire key to activate the laser.\
3\. Select the weapon and ammo type you wish to use using your weapon switch keys.\
4\. Press the Lase Target key while aiming at the target, your sight will shift dramatically during this process. This is intended.\
5\. Bring the gun up the the large aiming reticle is at the center of mass for your target.\
6\. Fire your first shot. Depending on terrain, elevation, and a number of other factors, your first shot will likely not hit its target. **Do not re-lase the target if you miss, just correct off the impact.**\
7\. Correct off the shot.\
8\. When lazing your next target, occasionally weirdness happens and the gun sight will no longer adjust to new ranges, if this happens, simply return to the fire control system weapon, toggle the laser off, and then toggle it back on again. Return to your weapon of choice and repeat from steps 4.\
\
Things to be mindful of in this system:\
1\. Different weapons have different ballistic characteristics, make sure you re-lase after changing weapons to ensure the correct ballistics are used in the calculations.\
2\. Firing outside of maximum range of your selected weapon will produce strange results, this is most notable when firing coax weapons at long distances (Usually >1km)\
3\. As far as I can tell, the system assumes that you're firing from sea level to another target at sea level, so the greater the elevation differences between you and the target, the more likely the first shot will miss.\
4\. The rangefinder has a minimum range of about 300m, within this range the rangefinder will automatically select 0000, this is because differences within this range are negligible.\
5\. Arma can be really fucking weird sometimes and this system can be unreliable, at the end of the day, this system is not a replacement for good aim and shot correction. If the rangefinder is giving you crazy ranges or missing by a lot, range something within minimums to reset the range to 0000 and fire manually.\
6\. If you're firing an ATGM range is generally irrelevant, as it tracks your mouse.\
\
Because this is by far the most complicated system to use, a made a simple video of the system in work, keep in mind that during the process of this video I switch ammo types from AP to HE, without using the action menu, which causes a large adjustment of my aiming reticle.\


{% embed url="https://youtu.be/OQlu-82KCPk" %}

### Russian Heavy Basic (Version 2) System

This is the system used by many Russian Main Battle Tanks. Today, this version is used primarily in export versions of the tanks, as most vehicles have been upgraded to the advanced system within Russia. This version of the FCS also includes a next-round selector for the autoloader. **Using it can be quite challenging, so I recommend you experiment with it in the editor prior to slotting a vehicle that uses this system.**\
\
The different types of ammo for the next-round autoloading system are as follows:\
0 - High Explosive Fragmentation Fin Stabilized\
б - Armor Piercing Fin Stabilized Discarding Sabot\
к - High Explosive Anti-Tank Fin Stabilized\
у - Anti-tank Guided Missile\
\
**It is absolutely imperative that you are aware of how to operate the autoloading system for optimal use of this tank! If you do not understand how this system functions, tell someone so it can be corrected before the mission!**\
\
To operate the Autoloader:\
1\. Load your first round normally using the action menu\
2\. Select the type of round you would like to be fired after the round in the chamber by pressing the Next round switch and using the guide above to select the correct type of ammo\
3\. After you fire the round in the chamber, this type of round will be loaded\
4\. If you would like to load a different type of ammo without firing, you must use your action menu to clear the round in the chamber.\
\
For the actual fire control system:\
1\. Aim at your target and select ammo type using your action menu, and ensure your next round is set correctly.\
2\. Press your lase target hotkey, a four character number should appear in the bottom center portion of the screen.\
2a. The light on the left tells you whether the weapon is ready to fire or not.\
This is the range calculated by the rangefinder, and it has automatically transferred this range into the ballistic computer. Manual range entry is NOT required.\
3\. Fire your first shot. Depending on terrain, elevation, and a number of other factors, your first shot will likely not hit its target. **Do not re-lase the target if you miss, just correct off the impact.**\
4\. Correct off your first shot and eliminate the target.\
\
Things to be mindful of in this system:\
1\. Different weapons have different ballistic characteristics, make sure you re-lase after changing weapons to ensure the correct ballistics are used in the calculations.\
2\. Firing outside of maximum range of your selected weapon will produce strange results, this is most notable when firing coax weapons at long distances (Usually >1km)\
3\. As far as I can tell, the system assumes that you're firing from sea level to another target at sea level, so the greater the elevation differences between you and the target, the more likely the first shot will miss.\
4\. The rangefinder has a minimum range of about 300m, within this range the rangefinder will automatically select 0000, this is because differences within this range are negligible.\
5\. Arma can be really fucking weird sometimes and this system can be unreliable, at the end of the day, this system is not a replacement for good aim and shot correction. If the rangefinder is giving you crazy ranges or missing by a lot, range something within minimums to reset the range to 0000 and fire manually.\
6\. If you're firing an ATGM range is generally irrelevant, as it tracks your mouse.

### Russian Heavy Basic (Version 3) System

This system is identical to Version 2 with the exception that the UI is slightly different. For the purposes of this guide, operating the weapon should be the same. This is the system used by many Russian Main Battle Tanks. Today, this version is used primarily in export versions of the tanks, as most vehicles have been upgraded to the advanced system within Russia. This version of the FCS also includes a next-round selector for the autoloader. **Using it can be quite challenging, so I recommend you experiment with it in the editor prior to slotting a vehicle that uses this system.**\
\
The different types of ammo for the next-round autoloading system are as follows:\
0 - High Explosive Fragmentation Fin Stabilized - 30F26\
б - Armor Piercing Fin Stabilized Discarding Sabot - 3BM46\
к - High Explosive Anti-Tank Fin Stabilized - 3BK31\
у - Anti-tank Guided Missile - 9M119\
\
**It is absolutely imperative that you are aware of how to operate the autoloading system for optimal use of this tank! If you do not understand how this system functions, tell someone so it can be corrected before the mission!**\
\
To operate the Autoloader:\
1\. Load your first round normally using the action menu\
2\. Select the type of round you would like to be fired after the round in the chamber by pressing the Next round switch and using the guide above to select the correct type of ammo\
3\. After you fire the round in the chamber, this type of round will be loaded\
4\. If you would like to load a different type of ammo without firing, you must use your action menu to clear the round in the chamber.\
\
For the actual fire control system:\
1\. Aim at your target and select ammo type using your action menu, and ensure your next round is set correctly.\
2\. Press your lase target hotkey, a four character number should appear in the bottom center portion of the screen.\
2a. The light on the left tells you whether the weapon is ready to fire or not.\
This is the range calculated by the rangefinder, and it has automatically transferred this range into the ballistic computer. Manual range entry is NOT required.\
3\. Fire your first shot. Depending on terrain, elevation, and a number of other factors, your first shot will likely not hit its target. **Do not re-lase the target if you miss, just correct off the impact.**\
4\. Correct off your first shot and eliminate the target.\
\
Things to be mindful of in this system:\
1\. Different weapons have different ballistic characteristics, make sure you re-lase after changing weapons to ensure the correct ballistics are used in the calculations.\
2\. Firing outside of maximum range of your selected weapon will produce strange results, this is most notable when firing coax weapons at long distances (Usually >1km)\
3\. As far as I can tell, the system assumes that you're firing from sea level to another target at sea level, so the greater the elevation differences between you and the target, the more likely the first shot will miss.\
4\. The rangefinder has a minimum range of about 300m, within this range the rangefinder will automatically select 0000, this is because differences within this range are negligible.\
5\. Arma can be really fucking weird sometimes and this system can be unreliable, at the end of the day, this system is not a replacement for good aim and shot correction. If the rangefinder is giving you crazy ranges or missing by a lot, range something within minimums to reset the range to 0000 and fire manually.\
6\. If you're firing an ATGM range is generally irrelevant, as it tracks your mouse.

### Russian AINET System

The AINET smart fuse system is a system for the Frag rounds that essentially creates air bursting effect. On vehicles with this feature, you will notice an additional UI elements, depending on specifically which variant of the AINET system the vehicle uses. Using this system can be touchy, it was recently introduced and has many bugs, but to operate it:

1. Lase your target with a type of ammo other than HE-FRAG loaded
2. Load HE Frag
3. Fire at your target

The round will take a significant ballistic bath and should hopefully explode above the target, depending on terrain this may not be very effective. This system appears to be extremely buggy and even I can't always get it to work correctly. That being said, when used correctly it is extremely effective.

### Russian SHTORA-1 EOCMDAS System

This system is only implemented in the most advanced Russian Main battle tanks, and has not be implemented in all tanks that should have it yet as of the time of posting. The SHITORA-1 is an Electro-Optical Countermeasure Defensive Aids Suite. The system detects and protects against beam guided anti-tank weapons systems such as the TOW ATGM.

The system consists of two dazzlers on each side of the gun, four rough laser sensors on the sides of the turret and two precision laser sensors mounted on the front of the turret. When a laser beam is detected, the system will play a sound and then turn the turret to face the beam, after which a volley of smoke grenades will be fired in conjunction with the activation of the dazzlers. Future versions of Russian tanks and some tanks in the T-90 series do not have the dazzlers as they are ineffective against modern ATGMS.

In game, this system is operated by the commander, by using his action menu to select the "Shtora: Turn on" button, this automatically places it in auto mode. Manual mode is not covered in this guide.

For various reasons, this system is not very effective in our modpack. For instance, it does not defeat Javelins like it should.
