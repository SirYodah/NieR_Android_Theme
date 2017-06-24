I'll be updating this as more versions are released and more bugs are found.

Known Issues for Release 1.0
-------------------------------------
* The music player will not show any information when the song is paused. This is actually intended, as my goal was to have song info remain visible while paused, and go away when the music app is closed or if playback is stopped. Unfortunately, some apps (looking at you, Spotify) don't properly report their state to KLWP, saying that they're paused when the app is actually closed and other things like that. The workaround for this is to just make the song information disappear whenever a song isn't playing.

* Animations get stuck if you swipe between screens too quickly. This appears to be rooted in how KLWP handles animations, so I don't believe there's anything I can do to fix it. Just don't swipe around too quickly, and you'll be good. Even if something gets stuck, fixing it is as simple as swiping away, waiting a second, then swiping back.

* The included "tick" sound doesn't play when you swipe between screens. Tasker doesn't have the ability to tell which screen number you're on, and also can't read variables from KLWP. This means that a sound on swiping back and forth is impossible, unfortunately. I could make it so that the top buttons react to touch and bring you to their respective screens, but this would require a refactor of the entire theme that I'm just not willing to undertake right now.

* Unread counts may be busted on newer androids, KLWP needs permission granted manually to fix. On Nova Launcher, tap and hold on the KLWP app icon, and then drag it up to App Info when it appears. Permissions can be changed from in there.

* Non-Tasker functionality isn't perfect. KLWP's method of detecting your screen unlocking doesn't appear to be as reliable as Tasker's, so sometimes animations may break or desync on unlock. Re-locking and unlocking your phone again should fix the immediate problem, but there isn't anything I can do to fix the source of the issue.

* Some of the global switches within KLWP may switch themselves on or off while editing the theme. This appears to be a UI bug caused by my theme having an ungodly amount of shit in it, but is mostly harmless. Just make sure that when you save and apply the theme, that you do so from the globals tab and make sure that your switches are set correctly when you do.

* For events to appear in the Home screen info, they have to be created as full-day events in your calendar app. This is mostly because I have no fucking clue how calendar functions work in KLWP and couldn't find a way to get it to display the first event of any kind on a day.

* The theme does not have landscape support, and likely never will. It'd be too much work to go back and refactor every single item in the theme to react to orientation changes at this point, and I don't have enough space left in the theme to add more screens. A side of effect of all this is that the theme will bug out when you use a landscape app. Everything **should** reset correctly on changing back to portrait, but I've had reports of things breaking instead. If this happens, re-applying the theme should fix it.

* Performance is bad. I can't tell if my work is just incredibly unoptimized, or if KLWP just isn't really meant to have as many items in a theme as I do. The theme will probably work poorly on older or less powerful models, and seems to use a decent chunk of battery life too. For reference, I built this on a Samsung Galaxy J7, and the theme mostly works perfectly for me, but animations will still occasionally lag or hang before playing.

* There's a somewhat lengthy delay between pressing a button and Tasker playing the corresponding sound. I don't think there's much I can do to fix this, as the interactions between KLWP and Takser seem to just not be fast enough.

* There may be some misc. other problems with certain parts of the theme getting stuck or disappearing at seemingly random times. If this happens, I've always been able to fix it by opening KLWP, toggling the "Tasker?" global a few times, then saving and exiting. Otherwise, I'm not sure what actually causes these problems, please report if you find any, especially if they're reproduceable.

