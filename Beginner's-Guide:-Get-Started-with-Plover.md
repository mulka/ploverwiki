This guide explains how to get started with Plover.

## Overview

The main steps are:

1. Install Plover software.
1. Connect a compatible keyboard or stenography (steno) machine, or use your standard keyboard.
1. Confirm it's working.
1. Practice and learn stenography using Plover. 

## Install Plover

There are versions of Plover for Windows, Mac, and Linux. 

* Download and install the [latest release](https://github.com/openstenoproject/plover/releases/latest). 
* See the [installation guide](https://github.com/openstenoproject/plover/wiki/Installation-Guide#installation) for more information.

### Configuring Plover on macOS

`Note: Plover 3.1.0 only supports macOS 10.10+. Plover 3.0.0 only supports macOS 10.9+. Older versions must use Plover 2.5.8`

On macOS, you need to enable [Assistive Device Permissions](https://support.apple.com/en-ca/HT202866) after you have installed Plover, and following any Plover software updates. 

1. Select `System Preferences > Security & Privacy > Privacy > Accessibility`.
1. Click the lock icon in the lower left corner of the window, and enter an admin account and password when prompted.
1. In the list of apps, select the checkbox next to Plover. 

Note: Other "keyboard helper"-type applications (e.g. Karabiner Elements and text expanders) may interfere with Plover.

## Connect a compatible keyboard or stenography machine

### Use a standard QWERTY keyboard

You can use Plover with a standard keyboard, but there are some important limitations. Stenography often requires you to press five or six keys at once, and sometimes as many as 16. Unfortunately, most keyboards only recognize up to six keys at once. When you need to press more than six keys are once, you have to use a technique called "arpeggiating". See ["How it Works" for more information on arpeggiating](http://qwertysteno.com/Basics/HowItWorks.php) .

`Note: To write quickly, you'll need a keyboard with N-key rollover (NKRO), a machine designed for use with Plover, or a professional stenography machine.`

### Use an N-key rollover (NKRO) QWERTY keyboard

An N-key rollover (NKRO) keyboard is specially designed to allow pressing many keys at once. Some gaming or mechanical keyboards have NKRO. Be wary of false advertising; some keyboards are advertised as NKRO or anti-ghosting, but are limited to certain combinations. Check reviews to get confirmation before making a purchase. Note, also, that some keyboards might only support full-NKRO over a PS/2 connector (the [old-style plug](https://en.wikipedia.org/wiki/PS/2_port#/media/File:Ps-2-ports.jpg).) Full NKRO over USB *is* possible and many keyboards do it well, and will work with Plover.

See the [[Supported Hardware]] page for a list of supported keyboards.

* The [Zalman ZM-K600S](https://www.amazon.com/Zalman-Unlimited-Multi-Key-keyboard-ZM-K600S/dp/B0196J3IPE) is currently the cheapest option in the USA, at $45-$50.

#### Switch type

Stenography works best when the keyboard takes little force to depress keys. The lighter, the better. Ideally, the switch will be linear, it should lack any clicks or bumps. The lighter the force, the better, for steno. In the Cherry MX line, the best switch is Red, at 45 cN actuation. For Gaterons, the best switch for steno is Clear/White (different names, same switch), at only 35 cN actuation.

#### Keytoppers

Most keyboards have the keys in staggered rows, which can make it difficult to press two keys in a column with a single finger. To solve this problem, you can use keytoppers, which are in the shape of the keys on a steno machine, and stick them on top of the relevant keys on the keyboard.  

You can buy laser-cut keytoppers from the [Plover Store](http://plover.deco-craft.com/). You can also make your own keytoppers out of plastic or even coins.

#### NKRO keyboards with an ortholinear layout

Keyboards with an "ortholinear" layout have the keys in straight columns. This is handy for steno, as it makes it easier to press two keys in a column with a single finger. 

* The [ErgoDox](https://deskthority.net/wiki/ErgoDox) is a fairly high-end NKRO keyboard at $200, with an ortholinear layout. It has two separate halves, so you can angle them to suit you. You can order it with the Gateron White keys, which have an extremely light, 35 gram activation force.
* The [Planck](http://olkb.com/planck/) is a NRKO keyboard with an ortholinear layout. It is 40% smaller than a standard keyboard.

### Use a machine designed for use with Plover

Various steno enthusiasts are making and selling machines designed for use with Plover:

* [Stenomod](http://stenomod.blogspot.com/)
  * This has light keys and a split design.
  * It is built and sold by Charley Shattuck out of California.
  * See Ted Morin's [review of the StenoMod](http://www.teds.space/2016/10/stenomod-affordable-steno-machine.html).
  * The name is supposed to hint at how the machine is "modular" and adaptable. It is very barebones so it is easy to take apart and customize.
* [SOFT/HRUF](https://softhruf.love/)
  * This has the shape of a stenography machine, but is built using computer keys rather than levers.
  * It is built and sold by Scott Urueta out of Miami.
  * See Ellis Pratt's [review of the SOFT/HRUF and Stenomod](https://groups.google.com/d/msg/ploversteno/iraOYarRbdg/tlHeagOQGQAJ).
  * The name is the steno representation for, and is pronounced as, "soft love".
* [Stenoboard](http://stenoboard.com/)
  * The first open source steno machine on the market, released in 2014.
  * It is sold and built by Caruso Emanuele out of Italy.
  * The Stenoboard's keys actuate like mouse-clicks instead of a keyboard or lever-machine, which unfortunately makes it unsuitable for extended periods of writing.

### Use a professional stenography machine
 
Some professional stenography machines are compatible with Plover. You can find used steno machines on eBay at reasonable prices. 

See the [[Supported Hardware]] page for a list of supported professional stenography machines.

## Confirm it's working

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a professional stenography  machine or the Stenomod, you'll need to configure Plover to look for your machine.

### Keyboard

By default, Plover will use your keyboard as its input device. 

1. Run Plover.
1. Click the Output: **Enable** radio button. 
 
You may like to go into Plover's `Configure > Display` settings and turn on either the stroke display or the suggestions window.

#### Practice sentences

You can practice sentences that (mostly) only need two keys at once, on the [StenoJig](https://joshuagrams.github.io/steno-jig/two-key) website.

#### Write "Hello World"

To write "Hello, world." into a text editor with Plover, using a QWERTY keyboard:

1. Run Plover. 
1. Click the **Enable** radio button.
1. Open a text editor.
1. Simultaneously press `R`, `N`, and `O` (left index finger on `R`, right thumb on `N`, and right ring finger on `O`), and then lift your fingers off the keys. 
  * `Hel` appears.
1. Simultaneously press `R`, `F`, and `V` (left index finger between 'R' and 'F', and left thumb on 'V'), and then lift your fingers off the keys.
  * `lo` appears. 
1. Simultaneously press `J`, `K`, `L`, and `;` (right index finger on `J`, right middle finger on `K`, right ring finger on `L`, and right little (pinky) finger on `;`), and then lift your fingers off the keys.
  * `,` appears.
1. Simultaneously press `D`, `V`, `J`, `O`, and [ (left middle finger on `D`, left thumb on `V`, right index finger on `J`, right ring finger on `O`, and right little (pinky) finger on `[`), and then lift your fingers off the keys. 
  * `world` appears.
1. Simultaneously press `U`, `I`, `O`, and `P` (right index finger on `U`, right middle finger on `I`, right ring finger on `O`, right little (pinky) finger on `P`), and then lift your fingers off the keys. 
  * `.` appears.

#### Use the correct body posture and finger placement

Your fingers should be curled slightly, so you press the keys using the tips of your fingers. 

<img src="http://stenoknight.com/plover/stenqwerty.png" width="450">

On a QWERTY keyboard, you move your hands half an inch up so that your left thumb is resting on the cracks between the `C` and `V` keys and your right thumb is resting between the `N` and `M` keys. The rest should fall into place. 

| QWERTY layout|Maps to steno layout |  
|:---:|:---:|
|`QWER   TY   UIOP[`|`STPH  **   FPLTD`|
|`ASDF   GH   JKL;`|`SKWR   **   RBGSZ`|
|`CV   NM`|`AO   EU`| 

See also:

* [Basic Hand Posture on the Steno Machine](https://www.youtube.com/watch?v=YfHNPW6EnHo)
* [Basic Body Position for Steno Students and Pros](https://www.youtube.com/watch?v=s_zyxgQvNEU)

### Stenography machine

Plover supports several protocols that are in use by various professional stenography machines. To configure Plover to the protocol your machine uses:

1. Run Plover and click the **Enable** radio button.
1. Click the **Configure** button on the Plover Dialog screen. The Plover configuration screen appears. 
1. On the **Machine** tab, select the protocol your machine uses. 
1. Click **Save**.

See [Supported protocols](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#supported-protocols) for more information. 

## Practice and learn

* Start learning stenography for free with [Learn Plover!](https://sites.google.com/site/ploverdoc/home)

* Practice the Learn Plover (and other stenography) exercises with [Steno Jig](https://joshuagrams.github.io/steno-jig/). 

See also [Learning Resources](https://github.com/openstenoproject/plover/wiki/Learning-Stenography) and [the old steno practice page](http://stenoknight.com/wiki/Practice).

### Which steno theory should you learn?

There are many steno theories on the best way of using the steno keyboard. 

All English language steno theories are derived from the original Stenotype theory devised by Ward Ireland. They all share the same keyboard design and basic method of representing the sounds. They differ mostly in the details of how they abbreviate words, and how many abbreviations they use. Some theories are focused on raw speed and efficiency, but require a lot of memorization. Others focus more on consistency and logical rules to reduce the amount of memorization and "on-the-job" mental gymnastics required.  

We recommend you start with Plover's StenEd-based theory, and the dictionary that is supplied with the Plover software. After 6 months, you'll have a better understanding of stenography, and you could then start experimenting with different theories. Everyone ends up adapting them and forming a personal style anyway. So you don't need to worry about the different steno theories until you hit 100 WPM or so.

It's not recommended to spend money on a theory before you know if you'll even like it.