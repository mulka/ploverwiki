Some common problems and solutions are recorded here. If you're having a problem with Plover then please see if it is described here along with a solution. Make sure to check the [bug tracker](https://github.com/openstenoproject/plover/issues) for known reported issues.

# General

* By default, Plover ships with three dictionaries. This can be a source of confusion to new users:

    - `main.json` is the core default dictionary. It is based off of Mirabai's own personal dictionary, which follows a StenEd-style. It contains over 140,000 entries and is adequate for anyone learning stenography. Mirabai uses this dictionary professionally for her realtime work.
    - `commands.json` contains some keyboard shortcuts and Plover-specific utilities, like the stroke to add a new translation: `TKUPT`. It also contains arrow key movements, copy and paste, and more. Take a look inside to see what Plover can do.
    - `user.json` is a blank dictionary. It's placed at the bottom of the dictionary list, meaning it is highest priority. When you define new strokes, they will get added to this dictionary, meaning that you can easily see which strokes you've defined yourself, instead of losing them inside the default dictionaries.
    - **If you have your own dictionary already**, you'll probably want to remove `main` and `custom` and add your own dictionary. This includes existing stenographers and users of another theory (Magnum, Phoenix). I'd recommend at least leaving `commands` there as Plover has some concepts that users of other steno software will not be familiar with initially. Make sure your theory dictionary is at the bottom of the list if you want new strokes to go to it.

# Windows

* Make sure to disable AutoKey if you're getting strange behavior with Plover

# macOS

* If you use a keyboard instead of a steno machine, Plover needs [Assistive Device Permissions](https://support.apple.com/en-ca/HT202866).
* macOS has a feature where holding down a key brings up an accent menu. This can sometimes drop keys when typing quickly, such as `TO/FPLT` producing `t.` instead of `to.`. To disable this, follow [this help article](https://www.tekrevue.com/tip/how-to-disable-the-character-accent-menu-in-os-x-mountain-lion/).

# Linux

* Older versions of IBus (prior to 1.5.11) don't handle the very fast simulated key presses of Plover. If this issue affects you, make sure you disable IBus or upgrade it.

* Plover does not handle dynamic keyboard layout switching: see [bug #298](https://github.com/openstenoproject/plover/issues/298)
