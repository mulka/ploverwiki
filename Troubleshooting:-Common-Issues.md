Some common problems and solutions are recorded here. If you're having a problem with Plover, see if it is described here along with a solution.

Also, please make sure to check the [Plover bug tracker](https://github.com/openstenoproject/plover/issues) for known reported issues.

--------------------

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [Issues](#issues)
  - [General](#general)
    - [Plover does not recognize my USB keyboard or steno machine](#plover-does-not-recognize-my-usb-keyboard-or-steno-machine)
    - [When using TX Bolt, any chord with `SW-` in it doesn't come out right](#when-using-tx-bolt-any-chord-with-sw--in-it-doesnt-come-out-right)
  - [Dictionary issues](#dictionary-issues)
    - [Dictionary priority](#dictionary-priority)
    - [If you have your own dictionary already](#if-you-have-your-own-dictionary-already)
  - [About the default dictionaries](#about-the-default-dictionaries)
    - [main.json](#mainjson)
    - [commands.json](#commandsjson)
    - [user.json](#userjson)
  - [Windows](#windows)
    - [Unrecognized keystrokes and other strange behavior](#unrecognized-keystrokes-and-other-strange-behavior)
  - [macOS](#macos)
    - [Plover does not run (macOS)](#plover-does-not-run-macos)
    - [Unrecognized keystrokes](#unrecognized-keystrokes)
  - [Linux](#linux)
    - [Unrecognized keystrokes](#unrecognized-keystrokes-1)
    - [Linux dynamic keyboard layout switching is not working](#linux-dynamic-keyboard-layout-switching-is-not-working)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Issues

## General

### Plover does not recognize my USB keyboard or steno machine

> **Note**: Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a steno machine, you'll need to configure Plover to look for your machine. See the [Supported Hardware page](https://github.com/openstenoproject/plover/wiki/Supported-Hardware) for configuration instructions specific to your machine.

If you know your machine has been configured correctly, and Plover doesn't recognize your keyboard or steno machine:

1. Confirm your keyboard or steno machine is plugged into your computer.
1. On the Plover control panel, check if it states the machine is connected or disconnected.
  * If it states the machine is disconnected, press the Reconnect button (this is to the right of "connected" or "disconnected" message).
1. If Plover still doesn't recognize your machine, try closing and relaunching Plover.

### When using TX Bolt, any chord with `SW-` in it doesn't come out right

Solution: in the serial settings, uncheck "Xon/Xoff" under "Flow control". This will solve the issue where using S and W in a chord causes Plover to ignore those keys.

## Dictionary issues

By default, Plover ships with three dictionaries: `main.json`, `commands.json` and `user.json`. This can be a source of confusion to new users.

### Dictionary priority

If two dictionaries contain the same steno strokes, Plover will use the one in the dictionary that has the highest priority.

In Plover 3.x and below, the dictionaries in the dictionary list were prioritized from the bottom up.

In Plover 4 and above, the dictionaries order is configurable, but the default is to have the highest priority dictionary at the top, and it is labeled with a star ⭐.

By default, the `user.json` dictionary is placed at the highest priority. If you want new strokes to go to a different dictionary by default (for example, you have your own dictionary already), make sure that the target dictionary is the highest priority.

### If you have your own dictionary already

If you have your own dictionary already, you'll probably want to remove `main.json` and `custom.json` and add your own dictionary. This includes existing stenographers and users of another theory (Magnum, Phoenix).

We do not recommend you remove the `commands.json` dictionary from the dictionary list. This is because Plover has some concepts that users of other steno software will not be familiar with initially. Feel free to go through `commands.json`, and remap strokes that you want to use in your own theory.

## About the default dictionaries

### main.json

`main.json` is the core default dictionary. It is based on Mirabai Knight's own personal dictionary, which follows a StenEd-style thoery. It contains over 140,000 entries and is adequate for anyone learning stenography. Mirabai uses this dictionary professionally for her realtime work.

### commands.json

`commands.json` contains some keyboard shortcuts and Plover-specific utilities. For example, the stroke to add a new translation: `TKUPT`. It also contains arrow key movements, copy and paste, and more.

Have a look inside to see some sample keyboard commands that Plover can do.

### user.json

`user.json` is a blank dictionary. By default, the `user.json` dictionary is the highest priority - it is the first dictionary Plover will use. When you define new strokes, they will get added to this dictionary. This means you can see which strokes you've defined yourself, instead of trying to locate them inside the default dictionaries.

## Windows

### Unrecognized keystrokes and other strange behavior

* Disable AutoKey if you're getting strange behavior with Plover.

## macOS

### Plover does not run (macOS)

* If you use a keyboard instead of a steno machine, Plover needs [Assistive Device Permissions](https://support.apple.com/en-ca/guide/mac-help/mh43185/mac). From the Catalina version of macOS, you may need to enable both the `Plover` app and the `env` app under Security & Privacy > Privacy > Accessibility.
* Plover will not work if you are using [Karabiner Elements](https://github.com/tekezo/Karabiner-Elements)

### Unrecognized keystrokes

macOS has a feature where holding down a key brings up an accent menu. This can sometimes drop keys when typing quickly, such as `TO/FPLT` producing `t.` instead of `to.` To disable this, follow the instructions in this article: ["How to Disable the Character Accent Menu in OS X Mountain Lion"](https://www.tekrevue.com/tip/how-to-disable-the-character-accent-menu-in-os-x-mountain-lion/).

## Linux

### Unrecognized keystrokes

* Older versions of IBus (prior to 1.5.11) don't handle the very fast simulated key presses of Plover. If this issue affects you, make sure you disable IBus or upgrade it.

### Linux dynamic keyboard layout switching is not working

* Plover does not handle dynamic keyboard layout switching: see [bug #298](https://github.com/openstenoproject/plover/issues/298)

### Delayed/slow output when using gnome-shell and the keyboard machine

* It's a gnome-shell [bug](https://github.com/openstenoproject/plover/issues/1030), unfortunately there's no known workaround.