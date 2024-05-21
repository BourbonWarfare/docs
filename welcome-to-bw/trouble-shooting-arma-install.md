# Trouble Shooting Arma Install

\
**Big Three:**\
1\. Make sure mods are updated.\
2\. Use the `.bat` file.\
3\. Check RPT file (located at %localappdata%/Arma 3/).\
\
**Other things:**\
4\. Verify Game Cache in Steam.\
5\. Check launch options in Steam.

\
**I don't see the server in the list, how do I connect?**

Launch ArmA 3 with the modpack.\
Click the `Connect to BW Server` button in the main menu.

In the multiplayer server brower, click the "DIRECT CONNECT" button.

{% hint style="info" %}
* Address: `104.128.50.152`
* Port: `2303`
{% endhint %}

**Why am I getting kicked?**\
1\. You are missing mods (missing something that the mission requires)\
2\. You have an extra mod mod not from our current modset (local RPT will say "not signed by a key accepted by this server")\
3\. You have modified pbos that don't match the .bisign (won't say anything locally, but server will show message "Wrong signature for file")\
\
**How do I use the bat file?**\
Go to your ArmA 3 directory.\
You should see a file called `Bourbon Warfare Private Client Launcher.bat`.\
you want to copy this, and then on the desktop `Paste > SHORTCUT`.\
This way the bat file can be updated automatically, and your shortcut will keep working\
pasting a copy will work for now, but will fail when the `.bat` file gets updated.\
\
**How do I check my RPT file?**\
Hit `WindowsKey+R` and type in %localappdata%/Arma 3/\
That should take you to something like C:\Users\SomeAsshole\AppData\Local\Arma 3\\\
Sort by Date Modified and open the most recent or pick the most recent name.\
I recommend _Notepad++_, but you should be able to "open with" any text program.\
\
**What should I look for in my RPT?**\
Recent Events will be at the bottom of the log.\
If you just got kicked, reopen the logfile and go to the bottom.
