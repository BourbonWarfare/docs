---
description: 'Credits: AACO, Nikkomara, Zerith'
---

# Getting Started

Hello! This is a guide for members who are looking to create missions for the community to play on session nights. The Bourbon Warfare Mission Framework (BWMF) is structured to be easy enough for any member to start making missions. Simply follow the steps in this guide and your missions will be ready for testing.

Before reading further, please note that this guide is written without a focus on the 3D editor. If you are unfamiliar with the 3D editor then it’s recommended to play around in it to get a feel for how to do things. This guide will refer to components in the 3D editor but not necessarily explain where to find everything.

It’s recommended to have a text editor such as [Notepad++](https://notepad-plus-plus.org/download/) or [Atom](https://atom.io/) to aid you during the mission workflow. If you decide to use Atom, consider picking up [the Atom plugin for SQF syntax highlighting.](https://atom.io/packages/language-arma-atom) It helps but is not required.

### Mission-making Overview:

1.  Framework Setup

    a. Name your mission
2.  Make your mission ([TvT](steps-to-create-a-tvt.md) or [Co-op](steps-to-create-a-co-op.md)?)

    a. Pick a map

    b. Loadouts

    c. Trimming player slots to desired specifications

    d. Briefings/Objectives

    e. Balance considerations (terrain, ratio, gear, assets, etc.)
3. Test your mission by yourself via the [mission-maker checklist](https://forums.bourbonwarfare.com/viewtopic.php?f=8\&t=562) and the [Mission Tester Checklist](https://forums.bourbonwarfare.com/viewtopic.php?f=8\&t=2608)
4. Upload your mission to the [#mission-upload](https://discord.com/channels/204621032428929025/934246522911096943) channel on the BW Discord.
5. Post your mission in the [Finished Missions](http://forums.bourbonwarfare.com/viewforum.php?f=30) forums and ask at least 2 others to test and sign-off on your mission. It is _your_ responsibility to find testers. Do not expect others to test for you.

### Framework Setup

All of our missions are created using our own mission framework, which is called the Bourbon Warfare Mission Framework, or **bwmf** as it will be referred to from now on. This framework contains everything we need to make our missions, such as loadouts, briefings, and more. You will want to download the framework from here: [https://github.com/BourbonWarfare/bwmf](https://github.com/BourbonWarfare/bwmf).

You will download a folder named **bwmf-master**. It is strongly recommended to check for a new version with regularity, as it gets updated on a semi-frequent basis.

Setting up a mission with the framework is relatively easy. The steps are outlined here:

1. Copy the **bwmf-master** folder.
2. Go into the **mpmissions** folder (Located at My Documents\Arma 3\mpmissions) and paste the copied **bwmf** folder.
3. Rename **bwmf-master** to your desired mission name using our naming convention explained below. The map suffix tells Arma what map your mission is on so it is the most important. (ie - **nikko\_tvt50\_shutdown\_v2.Zargabad**)
4. Launch your game and go to **Multiplayer -> New** (Should be local server) **->** **Select Zargabad** (or whichever map you selected) **-> Select your mission -> Click 3D editor** This ensures you are testing your mission in a server environment. It's easier to find certain issues here versus the singleplayer editor.
5. Once in the editor you should see multiple pre-placed units and platoons. You will work down from these to make your mission, but at this point you have setup the framework and are ready to make a mission!

### Naming Your Mission the BW Way

**nikko\_tvt50\_shutdown\_v2.Zargabad**

The first part of the name, **nikko\_**, is used to denote the author. **Try to condense your name to about 4-5 letters if it’s really long.**

**tvt50\_** explains two things. One, it tells us that this mission is a TvT mission(team vs team, adversarial, pvp) and the number **50** means that the author **recommends** 50 players to be present for an optimal mission experience.

**shutdown\_** is the mission name, self explanatory.

**v2** denotes which version of the mission is being played. You want to stay in v1 for as long as you can on your local machine and try to catch as many bugs as possible. Once you are satisfied and have checked your mission thoroughly THEN upload it to the server. If your testers find issues then go to v2, etc.

**.Zargabad** denotes what map this takes place on, which in this case, is Zargabad.

_An important thing to note is that we use mpmissions because the missions we make are meant to be played in Multiplayer. While you can use the single player mission editor and simply export the mission to make multiplayer compatible, it’s a good habit to use mpmissions in case you would like to use extensive scripting in your future missions. It will also make it more clear if you broke something with gear because the game will crash as it will emulate being a local server._
