---
description: 'Author: AACO'
---

# ACRE 2

Hey gang, this post is going to go into some details about ACRE and an explanation of keybinds.

## Intro

A quick explanation of ACRE and why they keys are set up as they are: So ACRE does not cap the number of radios you can utilize as an individual, so if someone really wanted they could be rolling 20 deep with 343s. To accommodate this ACRE is based off of "active" radios, not short range / long range like TFAR. ACRE determines radio order by how they are order in your inventory. It goes from top to bottom on your uniform, then vest, then backpack. The keybinds for "Alternate PTT 1-3" will activate the first three radios in this order. Now on a practicality level for BW, you should never have more than three radios (evil mission makers / framework issues aside) so just using these "Alternate PTT" buttons will work fine for what we do.

## Other odd behaviors and their explanations:

* I was trying to talk to someone on the radio, but they could never hear me.
  * One possibility is that ACRE radios are set to a mono-channeled mode, that means when you are transmitting, you can not receive radio messages on the radio you are transmitting from. There's a bug in ACRE the exacerbates the problem, even if you let go of your push to talk button and the person who was transmitting at the same time as you, keeps talking, you will not receive the message.
  * The other major possibility is that (especially with 343s) you are either out of range of the person you're trying to talk to, or there is terrain interference causing issues sending to units. A small hill can cause serious 343 radio issues if the groups are over 150-200m away.
  * Your ACRE is broken, you _should_ be able to reinitialize your radios in the signal tabs of your briefing. If that does not fix your problem, you probably have issues with the A3 ACRE plugin connecting to the TS3 ACRE plugin, at that point debugging the issue should take priority.
* My cycle radio/babel keys don't give any kind of popup.
  * Those keys will only have a popup (showing active radio/language) if you have more than one radio/known language.

## On to keybinds

### Default keybinds / what they do

* Tab: Change talk volume (hold tab, use scroll wheel to adjust)
* Caps Lock: Push to talk on active radio (the first radio in your inventory is the default active radio on mission load)
* Shift + Caps Lock: Push to talk on the first radio in your inventory (will also set the first radio as the active radio)
* Ctrl + Caps Lock: Push to talk on the second radio in your inventory (will also set the second radio as the active radio)
* Alt + Caps Lock: Push to talk on the third radio in your inventory (will also set the third radio as the active radio)
* Ctrl + Alt + Caps Lock: Open up active radio to switch channels or change radio volume (you can also do this by double clicking on any radio in your inventory)
* Alt + Shift + Caps Lock: Activate next radio (will not key the radio) Goes front to back (First radio -> Second radio -> Third radio -> .... -> Loop back to first radio)
* Ctrl + Alt + Right Arrow: Sets the active radio to your right ear
* Ctrl + Alt + Left Arrow: Sets the active radio to your left ear
* Ctrl + Alt + Up Arrow: Sets the active radio to both of your ears
* Ctrl + Alt + Down Arrow: Lowers your headset, essentially muting all your radios
* Left Windows Key: Cycle babel language

### My keybinds / rationale

* Tab: Change talk volume works fine for me)
* Caps Lock: Push to talk on the first radio in your inventory (removed active radio key, due to never needing it with the way our radios are set up)
* Shift + Caps Lock: Push to talk on the second radio in your inventory (Just shifted the bind up)
* Alt + Caps Lock: Push to talk on the third radio in your inventory (kept the same, trying to use Ctrl + Caps Lock kept messing with my stance)
* Ctrl + Alt + Caps Lock: Open up active radio to switch channels or change radio volume (works fine for me)
* Alt + Shift + Caps Lock: Activate next radio (works fine for me)
* Right Arrow: Sets the active radio to your right ear (A lot easier than the Ctrl+Alt combo)
* Left Arrow: Sets the active radio to your left ear (A lot easier than the Ctrl+Alt combo)
* Up Arrow: Sets the active radio to both of your ears (A lot easier than the Ctrl+Alt combo)
* Down Arrow: Lowers your headset, essentially muting all your radios (A lot easier than the Ctrl+Alt combo)
* App Key: Cycle babel language (removed the conflict with ACE interact)
