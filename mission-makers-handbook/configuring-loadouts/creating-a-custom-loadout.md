# Creating a Custom Loadout

So you're interested in creating a custom loadout file for your mission. You've come to (hopefully) the right place! The goal of this page will be to teach you everything you might need to know about a loadout file and how to create a custom loadout for yourself.

## Loadout File Structure

In the framework, there's a **Loadouts** folder. This is where loadout files are kept. Let's crack one open to see how loadout files are structured. Let's open up **aaf\_g3a3\_digi.hpp**. You should see:

<figure><img src="../../.gitbook/assets/Screenshot 2023-12-13 003101.png" alt=""><figcaption><p>aaf_g3a3_digi.hpp</p></figcaption></figure>

As you can see in this file, there's a lot of text. To break it down to a digestible format, each <mark style="color:orange;">orange</mark> string is a definable variable while each <mark style="color:green;">green</mark> string is an item class name retrieved from in-game. And to connect this further, assigning a unit a <mark style="color:orange;">**RIFLE**</mark> will give them a <mark style="color:green;">**"CUP\_arifle\_G3A3\_ris**</mark>**"** or a G3A3 battle rifle as defined on line 26. Underneath that on line 27, you can also identify the define for the corresponding magazines - <mark style="color:orange;">**RIFLE\_MAG**</mark> - and the item class names associated with it - <mark style="color:green;">"CUP\_20Rnd\_762x51\_G3:7"</mark>. The **:7** denotes the quantity of items. Default framework rifle loadouts typically give 7 regular magazines and 3 tracer magazines.

Now you might be asking: "Where can I find these classnames?" It's quite easy! If you're in the editor, simply right click on a unit of your choice -> Edit Loadout -> ACE Arsenal. Once you're inside the arsenal, select what item (uniform, primary weapon, etc.) that you'd like to find the classname for and then find your desired item. For this section, we'll look for an alternate magazine, so if the rifle/primary weapon is not already selected on the left-hand side, do so now. Then, on the right-hand side, select the magazine icon and search for "green". Select any of the magazines listed and you'll notice that when you hover over it, it'll look like this:

<figure><img src="https://lh7-us.googleusercontent.com/Z5KeoftStz0Rqk6OIgLn0nShSRN7HECFYBDa27RgntTzFdB0Cqw3RAYfFTe4TBTsKewzJdFaBZVaMmSsCzxTEweBQbiFBbeqB0w__5r5HBdE88dV4GEZd0JA_F80180_PZhXYrO5j4Nc-RzWYX2B" alt=""><figcaption><p>Magazines galore!</p></figcaption></figure>

If selected, simply copy it (ctrl+c) and paste it (ctrl+v) replacing the existing item class name: <mark style="color:green;">"CUP\_20Rnd\_TE1\_Yellow\_Tracer\_762x51\_G3:3"</mark> with the one you've copied, <mark style="color:green;">"CUP\_20Rnd\_TE1\_Green\_Tracer\_762x51\_G3:3"</mark>, and you're done!

This process applies to all defines - just make sure to match the item to the genre - uniform item class names go under the <mark style="color:orange;">CAMO\_UNIFORM, CAMO\_UNIFORM\_PILOT,</mark> and <mark style="color:orange;">CAMO\_UNIFORM\_VICC</mark> defines whereas the weapon item class names only go under <mark style="color:orange;">RIFLE, GLRIFLE, AR,</mark> etc.

## Item Inheritance

Time to take a look at how SLs, FTLs, ARs, and riflemen all get their gear. Scroll down a bit further past all of the defines until you reach line 119 <mark style="color:purple;">class</mark> <mark style="color:orange;">rifleman</mark> { who is our rifleman:

<figure><img src="../../.gitbook/assets/Screenshot 2023-12-13 012137.png" alt=""><figcaption><p>rifleman class</p></figcaption></figure>

In our **uniform\[] =**, you can see that our custom define <mark style="color:orange;">CAMO\_UNIFORM</mark>, is present. If you reference the first image at the top of the page, you'll see that under <mark style="color:orange;">CAMO\_UNIFORM</mark>, there are two uniform item class names defined: <mark style="color:green;">"U\_I\_CombatUniform", "U\_I\_CombatUniform\_shortsleeve"</mark>. For clothing, if you have multiple values present, it will randomly select one - so for right now, both uniforms have a 50/50 chance of being present on each unit. This applies to **vest\[]**, **headgear\[]**, and **backpack\[]** if you have multiple item class names in their respective defines.

Note the backpackItems\[] line, and how the value is <mark style="color:orange;">BASE\_MEDICAL</mark>. You might've noticed that <mark style="color:orange;">BASE\_MEDICAL</mark> is not defined anywhere in **aaf\_g3a3\_digi.hpp**. This is because it is defined in the file **common.hpp**.

This aforementioned common.hpp loadout file has a bunch of common defines/helper macros that allow us to reduce duplication in each of the sub loadout files. Here you can change medical supplies, change leader tools, and change the base soldier level tools.

At this point, we'll be discussing the difference between adding or overriding gear. Scroll down from <mark style="color:orange;">rifleman</mark> to class <mark style="color:orange;">ftl</mark>: <mark style="color:orange;">rifleman</mark> { on line 136. This is our Fireteam Leader.

<figure><img src="../../.gitbook/assets/Screenshot 2023-12-13 013315.png" alt=""><figcaption><p>Fireteam Leader class</p></figcaption></figure>

See <mark style="color:orange;">**ftl**</mark>**:&#x20;**<mark style="color:orange;">**rifleman**</mark> at the top there? The colon means that the FTL is inheriting from the rifleman class.

You'll notice that some items reappear - items like **vest\[]**, **backpack\[]**, or **magazines\[]**. This means that they are being overwritten by new items, such as the FTL's iconic rifle equipped with a grenade-launcher. You'll also notice that some items such as **items\[]** and **linkedItems\[]** have a **+=** after them - that is because these items are being _added_ to their loadout. If we just did items\[] = {LEADER\_TOOLS} for the FTL then he would not be inheriting TOOLS from Soldier\_F. He would be missing his short range radio, map tools, and IR strobe! That is why the LEADER\_TOOLS are appended with +=.

### Unit Class Name - Quick Reference

Each unit class name can have the following attributes:

1. `uniform[] = {"uniform_class_name"};` Randomly selects a uniform from the array to apply to the unit
2. `vest[] = {"vest_class_name"};` Randomly selects a vest from the array to apply to the unit
3. `headgear[] = {"helmet_class_name"};` Randomly selects a helmet/hat from the array to apply to the unit
4. `backpack[] = {"backpack_class_name"};` Randomly selects a backpack from the array to apply to the unit
5. `backpackItems[] = {"item_class_name:number_of_items"};` Add all the items in this array to the backpack, if there's no space left, it will try to add it to the unit's general inventory
6. `weapons[] = {"rifle_class_name"};` Randomly selects a rifle from the array to apply to the unit
7. `magazines[] = {"magazine_class_name:number_of_mags","grenade_class_name:number_of_grenades"};` Adds magazines/grenades to a unit
8. `items[] = {"item_class_name:number_of_items"};` Adds all the items from the array to the unit
9. `linkedItems[] = {"linked_item_class_name"};` Adds all the linked items in the array to the unit (nvgs, gps, compass, etc)
10. `attachments[] = {"weapon_attachment_class_name"};` Tries to add all the attachments to the main weapon/pistol. Not random, if there's two scopes, it will only add the last scope.
11. `launchers[] = {"launcher_class_name"};` Randomly selects a launcher from the array to add to the unit. NOTE: some launchers required the rocket to be in the inventory to be loaded and then launched.
12. `secondaryAttachments[] = {"launcher_attachment_class_name"};` Tries to add all the attachments to the launcher. Not random, if there's two scopes, it will only add the last scope.

### Inheritance Chart

<figure><img src="https://lh7-us.googleusercontent.com/GBre2ewchcHZf-LfnEwMiCQMQyf3P3sntioa8Tgpt_2PRuIWy7ggUhy1QZ1VVbXWJmHf92y9X7DuAPBiW7mhb4knyI0Aj0IuF4wP_cmDlbzmtIzIlWKe0HQDebqEY6u0saGCGsrGVNc4U1vrrJL8" alt=""><figcaption><p><a href="https://imgur.com/an3btQj">Higher Resolution ver.</a></p></figcaption></figure>

Note that there is a fallback class inherited from rifleman. This exists in the case that there is a placed unit from the editor that has no defined class. It will use the rifleman loadout automagically.

Also note that the MSV framework is separate from this graph and is structured differently.

## How to: Custom Loadouts

Okay, so now that we've filled your head with the per-requisite knowledge we will now be walking through how to make a custom loadout step-by-step.

1. In your BWMF folder, inside of the Loadouts folder, find and open the "blankForArsenal.hpp" file.
2. Launch Arma 3 and either go to Tutorials -> ACE Arsenal, or open up the editor, open a BWMF mission or place a fresh unit -> Right click on the unit -> Edit Loadout -> ACE Arsenal.
3.  Barbie your unit until you are satisfied with the result but take care to do the following at least:

    a.   Add whatever uniform you want

    b.   Add whatever vest you want

    c.   Add whatever helmet/hat you want

    d.   Add whatever backpack you want (and that can hold all your gear)

    e.   Add and configure whatever base rifle you want

    f.    Add at least one "normal" magazine

    g.   Add at least one "tracer" magazine
4. Use the POTATO Arsenal Macro to collect all of the classnames (pictured below)
5. Click the "Export" button
6. Paste the macro within the paste boundaries at the top of the "blankForArsenal.hpp" file.
7. Edit the defines beneath the boundaries at your discretion.
8. Ensure that the magazine amount is correct.
9. Give the file a quick once-over to ensure satisfaction.
10. Test the file in a mission to ensure there are no mistakes.
11. You now have a fully functional custom loadout file!

<figure><img src="../../.gitbook/assets/Screenshot 2023-12-13 015356.png" alt=""><figcaption><p>Potato Arsenal Macro</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2023-12-13 020138.png" alt=""><figcaption><p>The paste boundaries</p></figcaption></figure>

## Defining a New Unit Class

\[wip]

## Unit Diversification

This is a new feature as of 2024/04/29!

The POTATO spawn modules (as seen in [https://app.gitbook.com/o/tpAxQFeWzgFzsV9J1iUI/s/iD3lXIkOUvJDc5pYef0a/\~/changes/33/mission-makers-handbook/steps-to-create-a-co-op#spawning-units](../steps-to-create-a-co-op.md#spawning-units)) have been altered to include Rifleman 2 and Rifleman 3 classes into their structure whereas previously only the Rifleman 1 class was present.

What the aforementioned change allows for is the ability to define different weapons between Rifleman 1, Rifleman 2, and Rifleman 3, and to have that difference visible in normal gameplay. For example, if you intend for the players to fight an underfunded guerilla force, now you can define Rifleman 1 as having an AKM, Rifleman 2 to have an FAL, and Rifleman 3 to have an M16A2 - this previously would not be possible due to these classes not being present in the spawning module and only possible via the "Create-a-group" module.

To make use of this feature, an example has been provided below:

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-29 183223.png" alt=""><figcaption><p>Custom Rifle defines</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-29 183123.png" alt=""><figcaption><p>Rifleman 02 and Rifleman 03 classes using the custom rifle defines</p></figcaption></figure>
