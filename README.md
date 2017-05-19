# NieR_Android_Theme
Work in progress of a NieR: Automata themed KLWP preset.

Hello! If you're here, it's probably because you volunteered to test my NieR theme before I make it public. If that's not why you're here, well feel free to stick around, there's literally nothing I can do about it because I didn't wanna pay to use private repositories.

Anyways, here's how to get started on all this.

# SETUP

First, you'll need Kustom Live Wallpaper installed on your Android. [This one](https://play.google.com/store/apps/details?id=org.kustom.wallpaper&hl=en). You'll also need the pro version key, because you can't import themes without it. [You can find that here](https://play.google.com/store/apps/details?id=org.kustom.wallpaper.pro&hl=en).

Second, you'll need the actual theme itself, click the download button on this repository and then download as a zip. Extract the files somewhere, hook your Android up to your computer via USB, and make sure to press 'Allow' when your device asks you to establish a connection to transfer data. All you need is the .klwp file, so copy that, and move it somewhere onto your phone's storage where you can find it. Don't import it from inside KLWP just yet though, there's some other things to do first.

You'll also need Nova Launcher or a similar launcher, so that KLWP can play animations. The free version of Nova works just fine. [This is the one](https://play.google.com/store/apps/details?id=com.teslacoilsw.launcher&hl=en). Once you have Nova Launcher, take some time to configure it to your liking. There are two things that you need to make sure of: One, that your phone has three screens. You can tap and hold anywhere on the screen to edit the number of screens with Nova. Second, that there is nothing on any of your screens, other than the top status bar (battery %, time, wifi, etc). This includes page indicators, search bars, or apps. It won't break anything if you keep these things, they'll just be on top of the wallpaper and look out of place.

-------------------------------
[Optional, but worth it]

Do you want your phone to make the menu opening sound from the game as you unlock it? Of course you do! Unfortunately, the only way to do this without rooting your phone is to buy Tasker, [which is here](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en). If your phone is rooted, great! You don't need to buy it. I also can't help you at all, because my phone isn't rooted so I have no idea how to change the unlock sound. But if you do buy tasker, follow these next steps to get it working.

First you'll need the sound file itself, which you can find over at [this reddit thread](https://www.reddit.com/r/nier/comments/642dx5/request_extraction/). You'll want the 'opening menu' sound. And probably the other one too, because it's a sweet ringtone.
Then move it onto your phone, and into your ringtones folder so it's easy to find through Tasker.

[This next bit is blatantly stolen from this video](https://youtu.be/6D4XiflXdM0), as I followed this tutorial to do this and couldn't find a better way to do it. Open up Tasker, and create a new task called "Screen Unlocked". Open up this task, and add a Media Play Ringtone action. Edit this action so that the sound file points to your nier menu opening sound. You can also choose what type of sound it is and what stream it plays through, so for example if you set the stream to be ringer, the volume of the sound will use your current ringtone volume instead of something else like notification or media volume. Still inside this task, create a new Variable Set action. Name the variable "%Unlocked" without the quotes, and make it so this action sets it to 1. Now create a third action, this time selecting "Plugin", then "Kustom LWP", followed by "KLWP Send Variable". Edit this action so that it sends the Tasker String "%Unlocked" to the Kustom Variable "screen".

Now exit out of this task, and create a second task called "Screen Locked". The actions in this will be nearly identical to the first task. The only changes are to not add an action to play a sound (Unless you want a sound to play when you lock your phone, which you might), and to set "%Unlocked" to 0 instead of 1.

Next, swipe over to the Profiles screen, and create a new profile, using Event, followed by Display, and then Display Off. Set this profile to trigger the "Screen Locked" task. Now create a second profile, using the same conditions, except with Display Unlocked in place of Display Off. Have this trigger the "Screen Unlocked" task. 

And that's it!

--------------------------------

# IMPORTING AND CUSTOMIZATION


Now onto the good stuff. Boot up KLWP, and use the load preset option to import my preset that you put on your phone earlier. Once you click the save button at the top, KLWP should apply the theme to your phone! It might ask for permission the first time, so make sure to let it do that. If it looks normal, great! Onwards to customization!

I've done some work to make the theme customizeable, so you can change a decent amount of things pretty easily using the Globals tab of KLWP, accessed by swiping to the right while in the root folder. Variables can be changed by either tapping the field, or tapping the select box and then the pencil that appears in the top right. Important things are near the top, with some exceptions that you don't wanna forget towards the bottom. Let's go through them one at a time:

* "unlock" This variable is used to trigger all of those fancy unlock animations. If you DIDN'T follow the optional steps, you'll need to change it off of its default. Tap it, and delete the formula that's currently in the formula editor, and then tap the star underneath it to see if Kustom exported my fav'd formulas with the preset. If it did, select "Unlock without tasker", then tap the check in the upper right corner. If it didn't, enter the following EXACTLY as shown: $if(si(locked),0,1)$

* "LockScrn": Set this image as what you use as your lock screen. It's used to properly fade from your lock screen into the unlock animation.

* "LNumItems": and "RNumItems" These control the number of options on the left and right screen respectively. Supports a maximum of 5 options.

* "NotFound": This is used as placeholder text when an item's information doesn't exist, don't worry about changing it unless you'd just rather it said something else.

* "L-Name", "M-Name", and "R-Name": These are the names of the left, middle, and right screen respectively. You can change these to rename a specific screen, in case you don't want to use if for what I have it set as by default.

* "L-BotTxt", "M-BotTxt", and "R-BotTxt": These control what goes into the information box at the bottom of each screen. You can change them to anything, if you'd like, it won't affect anything else.

* "L-PosX" through "R-PosY": These control the X and Y positions of the items on the left and right screens. You shouldn't need to change these, unless you want to reposition something.

* "R-ToShow": This is used to determine which window to show on the right screen. I wouldn't touch this, as you could break the right screen.

* "u-frame", "u-done", and "u-fcount": These control aspects of the unlock animation. These shouldn't be touched, unless you want the animation itself to play slower or faster, in which case you can safetly change u-frame.

* "L-delay", "M-delay", and "R-delay": I only created these to make testing the top menu unlock animation easier. Fairly unnecessary, and they shouldn't need to be changed.

* "Font": Well it's the font used. Unless you want the theme to not look at all like what it's supposed to, don't change this.

* "Dark", "Medium", "Light", and "Backgrnd": These are the colors used. I wouldn't advise changing them, but be my guest if you want to.

* IMPORTANT SHIT BEGINS HERE

* "Lmenu": This controls what the name of each menu option is on the left screen. Replace the default list with a list of what you want each item to be. The list is comma separated.

* "Rmenu": Same as Lmenu, mostly, but for the right screen. Each option opens up a different app drawer on the bottom half of the screen, so keep that in mind when naming them.

* "RDrawer1" through "RDrawer5": More comma-separated lists, but these will be the names of apps that go in each drawer. Each drawer has 6 slots, but you can safetly enter fewer options, and the slot will be filled with the global "NotFound". Try to remember which app you put where, as you'll need to know which is which when you set touch shortcuts in the next step.

And that's all for globals. Sorry that the important lists are at the bottom, but as you'll notice while editing, lists get sent to the bottom of the global variables whenever they get edited for some reason.

Onwards! The next tab you'll want is Shortcuts, one swipe right of Globals. Here is where you'll set what touching a certain option does. These are pure personal preference, and you can safetly leave all of them blank, they just won't do anything when touched if you do. Again, we'll go through one by one.

* "M Info": This is that thing in the bottom left of the middle screen that gives you the date and location. I normally set this to open my calendar, but you're free to set it to whatever.

* "Weather App": This is triggered by touching any of the weather info inside the status box on the middle screen. Set this to a weather app of your preference. Also, touching the "Last Updated" text line will force an update instead of launching the app.

* "L Item 1" Through "L Item 5": Apps launched by touching the corresponding buttons on the left screen.

* All of the remaining ones are app slots on the right screen. Format is RX-Y, where X is the number of the drawer opened by the corresponding menu button, and Y is the letter code of the slot, so A/B/C/D/E/F.

And that's everything! You could go further if you want, and edit things directly inside of the root folder, but that place is a mess because my work is a mess and everything's a mess and you should just leave it alone if you want to stay sane. I won't stop you from trying though, but I've disabled exporting of changes until this is fully released. Once it's actually done I'll open it up so anyone can do anything to it and export, because I'm sure someone will want to fix some of my work to not be so terribly designed and optimized.
