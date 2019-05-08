# Discord Rich Presence Winamp plugin
Do you use Winamp to play media, and Discord for social purposes? If you have ever wanted to integrate Winamp into Discord, this simple, easy-to-use plugin will allow you to do it.

Features:
- Plugin has a settings menu for ease of use
- Changing settings doesn't require re-starting Winamp or the plugin
- Option to not display currently-playing title

Tested on 
- Winamp version 5.623 (x86)
- Winamp version 5.8 Build 3660 (x86)

This plugin is for Windows 7/8/10+ x86-compatible environments.

Example:

![Winamp is shown running, playing a song, side-by-side with a Discord Rich Presence status indicator showing that song's name and artist](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Example.png "Winamp is shown running, playing a song, side-by-side with a Discord Rich Presence status indicator showing that song's name and artist")

# Frequently Asked Questions (F.A.Q.'s)
**Q: Winamp, really? In {current year}?**

A: Yeah. Some people like it :P

**Q: How does it work?**

A: This is implemented as a Winamp plug-in which calls the Discord RPC API. The rich presence updates are sent to a Discord application which is associated with your Discord account.

**Q: How do I set it up?**

A: Here's step-by-step instructions:

1. Log in to the Discord web app.

Visit [discordapp.com/developers/applications/](http://www.discordapp.com/developers/applications/).

You'll see something like:

![A view of the Applications tab of the Discord Developer Portal, with a button that says Create an application](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup00.png "A view of the Applications tab of the Discord Developer Portal, with a button that says Create an application")

Click "**Create an application**". You can give it a name like "Winamp".

![An image of a dialog box titled Create an application. The user is typing in the text, Winamp. There are buttons labeled Create and Cancel](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup01.png "An image of a dialog box titled Create an application. The user is typing in the text, Winamp. There are buttons labeled Create and Cancel")

Afterward, you'll be taken to a screen to configure the application. You can set an icon, if you want. I got one from [here](https://commons.wikimedia.org/wiki/File:Winamp-logo.png).

![A view of the Applications tab of the Discord Developer Portal; viewing the General Information tab for the Winamp application. The screeenshot shows the Winamp Application's name as Winamp, and a CLIENT ID. An example ID of 112233445566778899 is shown.](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup02.png "A view of the Applications tab of the Discord Developer Portal; viewing the General Information tab for the Winamp application. The screeenshot shows the Winamp Application's name as Winamp, and a CLIENT ID. An example ID of 112233445566778899 is shown.")

The only thing to do here is to take note of the **Client ID**, also called an **Application ID**, since you'll need it later.

2. In Discord settings, go to **Game Activity** and set Winamp as a game if you have not already. An easy way to do that is to run Winamp, and then click the **Add it!** button.

![A view of Discord Settings, at the Game Activity tab. There is a header GAME ACTIVITY, a message of no game detected, and a message of Not seeing your game? Add it! where Add it! is clickable and there is an arrow pointing to it.](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup03.png "A view of Discord Settings, at the Game Activity tab. There is a header GAME ACTIVITY, a message of no game detected, and a message of Not seeing your game? Add it! where Add it! is clickable and there is an arrow pointing to it.")

3. To install the Winamp plugin, unzip the release folder and copy the results to the Plugins folder of your Winamp installation as shown.

Most often, the Plugins folder is located at **C:\Program Files (x86)\Winamp\Plugins**.

![Two Windows file folders are shown; one for the Winamp Plugins install folder and one for the unzipped plugin release. Arrows are showing that the plugin release files are copied into the Winamp Plugins folder.](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup04.PNG "Two Windows file folders are shown; one for the Winamp Plugins install folder and one for the unzipped plugin release. Arrows are showing that the plugin release files are copied into the Winamp Plugins folder.")

When you're done, there should be a file **gen_DiscordRichPresence.dll** in the Plugins folder, plus a folder inside that called DiscordRichPresence.

4. Now open Winamp (or restart it if it was already open), and go to **Preferences**.

![Winamp is shown running, where the user has clicked the menu button, moused-over the Options menu, and is about to click Preferences. Preferences can also be accessed with Ctrl+P.](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup05.png "Winamp is shown running, where the user has clicked the menu button, moused-over the Options menu, and is about to click Preferences. Preferences can also be accessed with Ctrl+P.")

Under the Plug-ins tab, under General Purpose, the "Discord Rich Presence" item should appear. If it does, the plug-in was successfully installed!

![The Winamp Preferences window is shown. There are some Preferences categories, such as Media Library, Skins and Plug-ins. Under the Plug-ins category, the user has clicked the General Purpose sub-category. There's a listing of General Purpose plugins, and Discord Rich Presence, labeled gen_DiscordRichPresence.dll, is at the top, selected. There are buttons labeled Configure selected plug-in and Uninstall selected plug-in. There's an arrow pointing to the Configure selected plug-in button.](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup06.PNG "The Winamp Preferences window is shown. There are some Preferences categories, such as Media Library, Skins and Plug-ins. Under the Plug-ins category, the user has clicked the General Purpose sub-category. There's a listing of General Purpose plugins, and Discord Rich Presence, labeled gen_DiscordRichPresence.dll, is at the top, selected. There are buttons labeled Configure selected plug-in and Uninstall selected plug-in. There's an arrow pointing to the Configure selected plug-in button.")

Click the button **Configure selected plug-in.**

![There is a model dialog box titled Discord Rich Presence. In it, there is a checkbox labeled Display currently-playing title in Discord status. The checkbox is checked. Also, there is a text box labeled Discord Application ID. In the text box, the user has filled in the text 112233445566778899. There are buttons OK and Cancel.](https://raw.githubusercontent.com/clandrew/wdrp/master/Images/Setup07.PNG "There is a model dialog box titled Discord Rich Presence. In it, there is a checkbox labeled Display currently-playing title in Discord status. The checkbox is checked. Also, there is a text box labeled Discord Application ID. In the text box, the user has filled in the text 112233445566778899. There are buttons OK and Cancel.")

On this menu, paste the Discord **Application ID** from before. Also, you can check or un-check the box depending on whether you are comfortable showing the currently-playing media on Discord.

Click OK, and you're done!

**Q: If I want to use the plugin, do I need to build from source?**

A: Nope- you can go to the [Releases](https://github.com/clandrew/wdrp/releases) page and download the binaries in a zip file.

**Q: Do I need to give the application my Discord credentials?**

A: No, the plugin doesn't ask for your credentials.

**Q: How come the status says "Playing a game" instead of "Listening to" like with Spotify?**

A: The Discord RPC library doesn't currently expose a way of changing this UI element. The status for Spotify works because Discord gives Spotify special treatment. If it comes to be that the RPC library adds flexibility of changing this, I'd be interested in adopting it.

**Q: Sometimes, I'm seeing a small delay before my Discord Rich Presence status is updated. What gives?**

A: Discord thresholds the update frequency of the status text on its side. The frequency is every 15 seconds. [See this page for more information](https://discordapp.com/developers/docs/rich-presence/how-to#updating-presence).

**Q: Is there a way to get it to show album art?**

A: Offhand, I don't currently know if it's possible.

**Q: If I want to build the plugin, what type of environment do I use?**

A: The plugin is built using Visual Studio 2017 on a Windows 10 environment. It uses the v141 toolset and SDK version 10.0.17134.0. Other environments might work too.

**Q: I have a question or other comment.**

A: Please contact cmlandrews at gmail dot com. Thank you for your feedback!
