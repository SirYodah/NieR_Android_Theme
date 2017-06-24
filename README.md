# NieR_Android_Theme
Work in progress of a NieR: Automata themed KLWP preset.

Hello! This readme will walk you through how to download and install my NieR Android theme. It'll take a little while to get everything working correctly, so get comfy.

Here's how to get started on all this.

# DOWNLOADS
----------------------------------
First, you'll need Kustom Live Wallpaper installed on your Android. [This one](https://play.google.com/store/apps/details?id=org.kustom.wallpaper&hl=en). You'll also need the pro version key, because you can't import themes without it. [You can find that here](https://play.google.com/store/apps/details?id=org.kustom.wallpaper.pro&hl=en).

You'll also need Nova Launcher or a similar launcher, so that KLWP can play animations. The free version of Nova works just fine. [This is the one](https://play.google.com/store/apps/details?id=com.teslacoilsw.launcher&hl=en). Once you have Nova Launcher, take some time to configure it to your liking. There are two things that you need to make sure of: One, that your phone has three screens. You can tap and hold anywhere on the screen to edit the number of screens with Nova. Second, that there is nothing on any of your screens, other than the top status bar (battery %, time, wifi, etc). This includes page indicators, search bars, or apps. It won't break anything if you keep these things, they'll just be on top of the wallpaper and look out of place.

Now, you've got a decision to make: Do you want your phone to make various sounds from the game as you use it, such as the menu opening, selection, and closing sounds? Of course you do! Unfortunately, the only way to do this without rooting your phone is to buy Tasker, [which is here](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en). This will allow KLWP to make sounds when you interact with the theme, along with allowing for some more stable interactions with the theme. I highly recommend using it, but if you'd rather not spend the cash it shouldn't make your life too much more difficult.

You'll also need the actual theme istelf, along with some optional files if you've decided to use Tasker. Click the download button on this repository and then download as a zip. Extract the files to somewhere where you can easily find and interact with them later.

Lastly, head to [this reddit thread](https://www.reddit.com/r/nier/comments/642dx5/request_extraction/), and grab the "Incoming Call" sound file. It isn't necessary to the theme at all, but it's a sweet ringtone and you'll probably want it.

# SETUP
-------------------------------
Now you gotta move all those downloads over to your Android. Hook it up to your PC via USB, and press 'Allow' if your device asks you to establish a connection. Grab the .klwp file and move it somewhere onto your phone where you can find it, doesn't really matter where. If you're going to be using Tasker, open up the Sound Assets folder and move all of them into your phone's Ringtones folder. Except for nier_mail_notify. Move that into your Notifications folder, and set it as your default notification sound if you want. The theme doesn't actually use it at all, it's just a nice thing to have.

Next is also for you Tasker users. Open up the Tasker Files folder that you downloaded, and then copy both the profiles and tasks folders. Copy those over to the Tasker folder on your phone. If the Tasker folder isn't there, try messing around with Tasker for a bit to see if it creates one, or just make it yourself in your phone's root folder. Once that's done, open up Tasker, and turn off 'Beginner Mode' in prefrences. Close out of preferences, and tap the Profiles tab, then select import. Two profiles should appear here if you moved the files over correctly. Import both of them. Then switch to the tasks tab, and tap it, selecting import again. There should be five tasks here, import all of them.

# IMPORTING
--------------------------------------
Now onto the good stuff. Boot up KLWP, and use the load preset option to import my preset that you put on your phone earlier. The theme should appear within KLWP. Before clicking the save button, head on over to the globals tab by swiping the menu to the right. There's a ton of variables here, but right now the only one you care about is the switch named "Tasker?" which should be about three down the list. It's pretty simple really, toggle that switch on if you use Tasker, and toggle it off if you don't use Tasker. Now that you've done that, hit save, wait a minute, and then exit KLWP. The theme should be applied! If the theme doesn't appear or you only see a solid image, try locking and unlocking your phone. Now, onwards to customization!

# CUSTOMIZATION
------------------------------------------------
I've done some work to make the theme customizeable, so you can change a decent amount of things pretty easily using the Globals tab of KLWP, accessed by swiping to the right while in the root folder. Variables can be changed by either tapping the field, or tapping the select box and then the pencil that appears in the top right. Most important things are near the top, with some exceptions that you don't wanna forget towards the bottom. Let's go through them one at a time:

* "LockScrn": Set this image as what you use as your lock screen. It's used to properly fade from your lock screen into the unlock animation. 

* "b-Anims": This switch controls the ambient animations of the lines and circles in the background. Switching it on will turn the animations on, and switching it off will turn them off. This is off by default, because while the animations do look very pretty, they also eat battery life like crazy. If you don't mind sacrificing your phone's battery, you can turn these on.

* "Tasker?": This switches the theme betwen two methods of handling animations when toggled. If you use Tasker, leave it on. If you don't use Tasker, make sure to turn it off.

* "u-Delay": This is an additonal delay that happens before the unlock animation if "Tasker?" is set to off. KLWP's method of detecting unlocks is a bit too quick sometimes, and you'll miss some of the animation unless a delay is added. If you aren't using Tasker, you should experiment with this to find a good-looking delay for you. This delay is in tenths of a second, so the default of four is 0.4 seconds, while changing it to ten would give a whole second delay.

* "LNumItems": and "RNumItems" These control the number of options on the left and right screen respectively. Supports a maximum of 5 options. Set to however many options you want on each screen.

* "Music?": This switch turns the music player on or off. If you'd rather not have the music player visible, that's what this is for.

* "NotFound": This is used as placeholder text when an item's information doesn't exist, don't worry about changing it unless you'd just rather it said something else.

* "L-Name", "M-Name", and "R-Name": These are the names of the left, middle, and right screen respectively. You can change these to rename a specific screen, in case you don't want to use if for what I have it set as by default.

* "L-BotTxt", "M-BotTxt", and "R-BotTxt": These control what goes into the information box at the bottom of each screen. You can change them to anything, if you'd like, it won't affect anything else.

* "L-PosX" through "R-PosY": These control the X and Y positions of the items on the left and right screens. You shouldn't need to change these, unless you want to reposition something.

* "R-ToShow": This is used to determine which window to show on the right screen. I wouldn't touch this, as you could break the right screen.

* "unlock": The formula that determines when the phone is unlocked if "Tasker?" is on. Does nothing if "Tasker?" is off. Changing this will break the unlock animation if you have "Tasker?" set to on, however I guess you could set it to be 1 if you'd rather never see the unlock animations.

* "u-frame", "u-done", and "u-fcount": These control aspects of the unlock animation. These shouldn't be touched, unless you want the animation itself to play slower or faster, in which case you can safetly change u-frame.

* "L-delay", "M-delay", and "R-delay": I only created these to make testing the top menu unlock animation easier. Fairly unnecessary, and they shouldn't need to be changed.

* "Font": Well it's the font used. Unless you want the theme to not look at all like what it's supposed to, don't change this.

* "Dark", "Medium", "Light", and "Backgrnd": These are the colors used. The theme fully supports changing these colors, all items and images will update to reflect the new color. This can be useful if your phone's screen is calibrated incorrectly, causing the theme's colors to look wrong. I'll go more in-depth on this later in readme.

* IMPORTANT SHIT BEGINS HERE

* "Lmenu": This controls what the name of each menu option is on the left screen. Replace the default list with a list of what you want each item to be. The list is comma separated.

* "Rmenu": Same as Lmenu, mostly, but for the right screen. Each option opens up a different app drawer on the bottom half of the screen, so keep that in mind when naming them.

* "RDrawer1" through "RDrawer5": More comma-separated lists, but these will be the names of apps that go in each drawer. Each drawer has 6 slots, but you can safetly enter fewer options, and the slot will be filled with the global "NotFound". Try to remember which app you put where, as you'll need to know which is which when you set touch shortcuts in the next step.

And that's all for globals. Sorry that the important lists are at the bottom, but as you'll notice while editing, lists get sent to the bottom of the global variables whenever they get edited for some reason.

Onwards! The next tab you'll want is Shortcuts, one swipe right of Globals. Here is where you'll set what touching a certain option does. These are pure personal preference, and you can safetly leave all of them blank, they just won't do anything when touched if you do. You'll notice that some of the shortcuts have a chain link icon and are set to "Task Shorcut". These are what play the sounds when interacting with the theme, for some reason some of them show up here. Just ignore them, they *shouldn't* do anything if you don't have tasker. Hopefully.

Again, we'll go through one by one.

* "M Info": This is that thing in the bottom left of the middle screen that gives you the date and location. I normally set this to open my calendar, but you're free to set it to whatever.

* "Weather App": This is triggered by touching any of the weather info inside the status box on the middle screen. Set this to a weather app of your preference. Also, touching the "Last Updated" text line will force an update instead of launching the app.

* "L Item 1" Through "L Item 5": Apps launched by touching the corresponding buttons on the left screen.

* All of the remaining ones are app slots on the right screen. Format is RX-Y, where X is the number of the drawer opened by the corresponding menu button, and Y is the letter code of the slot, so A/B/C/D/E/F.


Lastly, you may notice that the theme's colors look off compared to what you've seen from my screenshots. This is because many phone's screens are calibrated incorrectly by default. Also, some manufacturers go a step further and completely disable the ability to calibrate the screen without rooting (Thanks Samsung! *Not.*) If your colors look off, do some research and find out if your Android model is capable of screen calibration. If not, then you can try to fiddle with the colors from inside KLWP until it looks right, as I've made it so that literally everything in the theme can have its color changed. This is a bit tedious, but it's better than having the theme look really saturated and green all the time.

--------------------------------------------------------------------------------

And that's everything! You could go further if you want, and edit things directly inside of the root folder, but that place is a mess because my work is a mess and everything's a mess and you should just leave it alone if you want to stay sane. I won't stop you from trying though, because I'm sure someone will want to fix some of my work to not be so terribly designed and optimized. You can even export your changes and host if yourself if you want, I won't stop you. Just remember to credit me and not claim it as your own work, or else I'll be very mad, and I'll send you messages, letting you know how mad I am.

Before you head out, make sure to check out the Known Issues file, as the theme isn't perfect and you should know what you're getting yourself into. I don't plan on releasing any updates to this at the moment, but if you find something absolutely broken that slipped through my tests that I don't have documented, then please let me know!
