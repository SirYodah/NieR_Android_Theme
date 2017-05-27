I'll be updating this as more versions are released and more bugs are found.

Known Issues for Test Release 1.0

* Performance is probably gonna be shit, there's a ton of animations. The ambient background animations in particular eat up a ton of battery, so I've included the ability to disable them in the next version.

* Don't swipe between screens too fast. Some of the more complex animations in KLWP don't reset properly when you leave a screen and return to it too quickly. Occasionally you'll get left with some items missing until you leave and return to the screen. I think this happens because when an animation's trigger isn't active, the animation isn't just not happening, it plays in reverse until it gets to the starting point of the animation. So when you swipe onto say, the left screen, everything fades and scrolls in because you're on the correct screen. But when you swipe away, they don't just fade away, they also do those same animations in reverse, you just can't see it. So if you swipe back onto it before the reverse animations can finish playing, they don't reset properly and don't trigger to play forwards, even though you're on the correct screen.

* Unread counts may be busted on newer androids, KLWP needs permission granted manually to fix. On Nova Launcher, tap and hold on the KLWP app icon, and then drag it up to App Info when it appears. Permissions can be changed from in there.

* Reports of non-tasker functionality being broken, especially on the unlock animations. Next version includes fixes for this, along with an easy toggle switch to say if you're using tasker or not.

* Probably lots more, still waiting on reports.
