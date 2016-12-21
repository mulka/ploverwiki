Some common problems and solutions are recorded here. If you're having a problem with Plover then please see if it is described here along with a solution. Make sure to check the [bug tracker](https://github.com/openstenoproject/plover/issues) for known reported issues.

# Dictionaries

By default, Plover ships with three dictionaries: `main.json`, `commands.json` and `user.json`. This can be a source of confusion to new users. 

## main.json

`main.json` is the core default dictionary. It is based on Mirabai Knight's own personal dictionary, which follows a StenEd-style thoery. It contains over 140,000 entries and is adequate for anyone learning stenography. Mirabai uses this dictionary professionally for her realtime work.

## commands.json
`commands.json` contains some keyboard shortcuts and Plover-specific utilities. For example, the stroke to add a new translation: `TKUPT`. It also contains arrow key movements, copy and paste, and more. 

Have a look inside to see which keyboard commands Plover can do.

## user.json

`user.json` is a blank dictionary. It has the highest priority - it is the first dictionary Plover will use. When you define new strokes, they will get added to this dictionary. This means you can see which strokes you've defined yourself, instead of trying to locate them inside the default dictionaries.

## Dictionary priority
The dictionaries in the dictionary list are prioritised from the bottom up. By default, the `user.json` dictionary is placed at the bottom of the dictionary list and has the highest priority. If you wanted new strokes to go to different dictionary (for example, you have your own dictionary already), make sure this dictionary is at the bottom of the list.

## If you have your own dictionary already

If you have your own dictionary already, you'll probably want to remove `main` and `custom` and add your own dictionary. This includes existing stenographers and users of another theory (Magnum, Phoenix). 

We do not recommend you remove the `commands.json` dictionary from the dictionary list. This is because Plover has some concepts that users of other steno software will not be familiar with initially. 

Make sure your theory dictionary is at the bottom of the list if you want new strokes to go to it.

# Windows

* Make sure to disable AutoKey if you're getting strange behavior with Plover

# macOS

* If you use a keyboard instead of a steno machine, Plover needs [Assistive Device Permissions](https://support.apple.com/en-ca/HT202866).
* macOS has a feature where holding down a key brings up an accent menu. This can sometimes drop keys when typing quickly, such as `TO/FPLT` producing `t.` instead of `to.` To disable this, follow [this help article](https://www.tekrevue.com/tip/how-to-disable-the-character-accent-menu-in-os-x-mountain-lion/).
* Plover will not work if you are using [Karabiner Elements](https://github.com/tekezo/Karabiner-Elements)

# Linux

* Older versions of IBus (prior to 1.5.11) don't handle the very fast simulated key presses of Plover. If this issue affects you, make sure you disable IBus or upgrade it.

* Plover does not handle dynamic keyboard layout switching: see [bug #298](https://github.com/openstenoproject/plover/issues/298)
