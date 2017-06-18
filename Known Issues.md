I'll be updating this as more versions are released and more bugs are found.

Known Issues for Test Release 3.0
-------------------------------------
* The music player will not show any information when the song is paused. This is actually intended, as my goal was to have song info remain visible while paused, and go away when the music app is closed or if playback is stopped. Unfortunately, some apps (looking at you, Spotify) don't properly report their state to KLWP, saying that they're paused when the app is actually closed and other things like that. The workaround for this is to just make the song information disappear whenever a song isn't playing.

* Animations still get stuck if you swipe between screens too quickly. This appears to be rooted in how KLWP handles animations, so I don't believe there's anything I can do to fix it. Just don't swipe around too quickly, and you'll be good. Even if something gets stuck, fixing it is as simple as swiping away, waiting a second, then swiping back.

* The included "tick" sound doesn't play when you swipe between screens. Tasker doesn't have the ability to tell which screen number you're on, and also can't read variables from KLWP. This means that a sound on swiping back and forth is impossible, unfortunately. I could make it so that the top buttons react to touch and bring you to their respective screens, but this would require a refactor of the entire theme that I'm just not willing to undertake right now.

* Unread counts may be busted on newer androids, KLWP needs permission granted manually to fix. On Nova Launcher, tap and hold on the KLWP app icon, and then drag it up to App Info when it appears. Permissions can be changed from in there.

* Non-Tasker functionality isn't perfect. KLWP's method of detecting your screen unlocking doesn't appear to be as reliable as Tasker's, so sometimes animations may break or desync on unlock. Re-locking and unlocking your phone again should fix the immediate problem, but there isn't anything I can do to fix the source of the issue.

* Some of the global switches within KLWP may switch themselves on or off while editing the theme. This appears to be a UI bug caused by my theme having an ungodly amount of shit in it, but is mostly harmless. Just make sure that when you save and apply the theme, that you do so from the globals tab and make sure that your switches are set correctly when you do.

* For events to appear in the Home screen info, they have to be created as full-day events in your calendar app. This is mostly because I have no fucking clue how calendar functions work in KLWP and couldn't find a way to get it to display the first event of any kind on a day.

* The theme does not have landscape support, and likely never will. It'd be too much work to go back and refactor every single item in the theme to react to orientation changes at this point, and I don't have enough space left in the theme to add more screens. A side of effect of all this is that the theme will bug out when you use a landscape app. Everything **should** reset correctly on changing back to portrait, but I've had reports of things breaking instead. If this happens, re-applying the theme should fix it.

* There may be some misc. other problems with certain parts of the theme getting stuck or disappearing at seemingly random times. If this happens, I've always been able to fix it by opening KLWP, toggling the "Tasker?" global a few times, then saving and exiting. Otherwise, I'm not sure what actually causes these problems, please report if you find any, especially if they're reproduceable.

Known Issues for Test Release 2.0
-------------------------------------
* Animations still get stuck if you swipe between screens too quickly. This appears to be rooted in how KLWP handles animations, so I don't believe there's anything I can do to fix it. Just don't swipe around too quickly, and you'll be good. Even if something gets stuck, fixing it is as simple as swiping away, waiting a second, then swiping back.

* The included "tick" sound doesn't play when you swipe between screens. Tasker doesn't have the ability to tell which screen number you're on, and also can't read variables from KLWP. This means that a sound on swiping back and forth is impossible, unfortunately. I could make it so that the top buttons react to touch and bring you to their respective screens, but this would require a refactor of the entire theme that I'm just not willing to undertake right now.

* Unread counts may be busted on newer androids, KLWP needs permission granted manually to fix. On Nova Launcher, tap and hold on the KLWP app icon, and then drag it up to App Info when it appears. Permissions can be changed from in there.

* Non-Tasker functionality isn't perfect. KLWP's method of detecting your screen unlocking doesn't appear to be as reliable as Tasker's, so sometimes animations may break or desync on unlock. Re-locking and unlocking your phone again should fix the immediate problem, but there isn't anything I can do to fix the source of the issue.

* Some of the global switches within KLWP may switch themselves on or off while editing the theme. This appears to be a UI bug caused by my theme having an ungodly amount of shit in it, but is mostly harmless. Just make sure that when you save and apply the theme, that you do so from the globals tab and make sure that your switches are set correctly when you do.

* For events to appear in the Home screen info, they have to be created as full-day events in your calendar app. This is mostly because I have no fucking clue how calendar functions work in KLWP and couldn't find a way to get it to display the first event of any kind on a day.

* There may be some misc. other problems with certain parts of the theme getting stuck or disappearing at seemingly random times. If this happens, I've always been able to fix it by opening KLWP, toggling the "Tasker?" global a few times, then saving and exiting. Otherwise, I'm not sure what actually causes these problems, please report if you find any, especially if they're reproduceable.


Known Issues for Test Release 1.0
------------------------------------------
* Performance is probably gonna be shit, there's a ton of animations. The ambient background animations in particular eat up a ton of battery, so I've included the ability to disable them in the next version.

* Don't swipe between screens too fast. Some of the more complex animations in KLWP don't reset properly when you leave a screen and return to it too quickly. Occasionally you'll get left with some items missing until you leave and return to the screen. I think this happens because when an animation's trigger isn't active, the animation isn't just not happening, it plays in reverse until it gets to the starting point of the animation. So when you swipe onto say, the left screen, everything fades and scrolls in because you're on the correct screen. But when you swipe away, they don't just fade away, they also do those same animations in reverse, you just can't see it. So if you swipe back onto it before the reverse animations can finish playing, they don't reset properly and don't trigger to play forwards, even though you're on the correct screen.

* Unread counts may be busted on newer androids, KLWP needs permission granted manually to fix. On Nova Launcher, tap and hold on the KLWP app icon, and then drag it up to App Info when it appears. Permissions can be changed from in there.

* Reports of non-tasker functionality being broken, especially on the unlock animations. Next version includes fixes for this, along with an easy toggle switch to say if you're using tasker or not.

* Probably lots more, still waiting on reports.
