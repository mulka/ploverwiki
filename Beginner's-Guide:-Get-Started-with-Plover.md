This guide explains how to **get started with Plover**. Plover is free stenography software. All the learning resources listed below are free-of-charge.

## Overview

The main steps are:

1. [Install Plover software.](#install-plover)
1. [Connect a compatible keyboard or stenography (steno) machine.](#connect-a-compatible-keyboard-or-stenography-machine)
1. [Confirm it's working.](#confirm-its-working)
1. [Practice and learn stenography using Plover.](#practice-and-learn)

## Install Plover

Plover works on **Windows, Mac, and Linux**. 

* See the [installation guide](https://github.com/openstenoproject/plover/wiki/Installation-Guide) to install Plover.
* If you get stuck, see the [troubleshooting guide](https://github.com/openstenoproject/plover/wiki/Troubleshooting:-Common-Issues).

## Connect a compatible keyboard or stenography machine

### Use a standard QWERTY keyboard

**You can use Plover with a standard computer keyboard, but there are some important limitations.** Stenography often requires you to press 5 or 6 keys at once, and sometimes as many as 16. Unfortunately, most keyboards only recognize up to 1-6 keys at once. When you need to press more than 6 keys at once, you have to use a technique called "arpeggiating". See ["How it Works" for more information on arpeggiating](http://qwertysteno.com/Basics/HowItWorks.php).

> **Note**: To write quickly, you'll need a keyboard with N-key rollover (NKRO), a machine designed for use with Plover, or a professional stenography machine.

### Use an N-key rollover (NKRO) QWERTY keyboard

An N-key rollover (NKRO) keyboard is specially designed to allow pressing many keys at once. Some gaming or mechanical keyboards have NKRO. 

#### Which NKRO keyboard should I get?

> **Warning**: Be wary of false advertising; some keyboards are advertised as NKRO or anti-ghosting, but are limited to certain combinations. Check reviews to get confirmation before making a purchase. Some keyboards might only support full-NKRO over a PS/2 connector (the [old-style plug](https://en.wikipedia.org/wiki/PS/2_port#/media/File:Ps-2-ports.jpg).) 

Full NKRO over USB is possible. Many keyboards do it well, and will work with Plover. 

* See the [[Supported Hardware]] page for a [list of supported keyboards](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#known-supported-keyboards).
* See also: [Which type of key switch should I choose?](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#which-type-of-key-switch-should-i-choose)

### Adapt a keyboard for steno use

Most keyboards have the keys in staggered rows, which can make it difficult to press two keys in a column with a single finger. To adapt a keyboard for steno, you can use:

* [Keytoppers](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#keytoppers)
* [Keycaps](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#keycaps)

You can also use [a keyboard with an ortholinear layout](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#nkro-keyboards-with-an-ortholinear-layout).

### Use a machine designed for use with Plover

Various steno enthusiasts are making and selling machines designed for use with Plover:

* [Georgi*](https://www.gboards.ca/product/georgi)
* [Splitography*](https://softhruf.love/products/soft-hruf-erl)
* [TinyMod*](https://stenomod.blogspot.com/2018/11/tinymod2.html)

(* = External link)

More information: [Dedicated machines designed for use with Plover](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#dedicated-machines-designed-for-use-with-plover).

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

#### Write "Hello World"

To confirm Plover is working correctly, you may try to write "Hello, world." into a text editor with Plover, using a QWERTY keyboard:

1. Run Plover. 
1. Click the **Enable** radio button.
1. Open a text editor.
1. Simultaneously press `R`, `N`, and `O` (left index finger on `R`, right thumb on `N`, and right ring finger on `O`), and then lift your fingers off the keys. <br>The word `Hell` appears.
1. Simultaneously press `R`, `F`, and `V` (left index finger between 'R' and 'F', and left thumb on 'V'), and then lift your fingers off the keys. <br>The `o` appears. 
1. Simultaneously press `J`, `K`, `L`, and `;` (right index finger on `J`, right middle finger on `K`, right ring finger on `L`, and right little (pinky) finger on `;`), and then lift your fingers off the keys. <br>The comma appears.
1. Simultaneously press `D`, `V`, `J`, `O`, and `[` (left middle finger on `D`, left thumb on `V`, right index finger on `J`, right ring finger on `O`, and right little (pinky) finger on `[`), and then lift your fingers off the keys. <br>`world` appears.
1. Simultaneously press `U`, `I`, `O`, and `P` (right index finger on `U`, right middle finger on `I`, right ring finger on `O`, right little (pinky) finger on `P`), and then lift your fingers off the keys. <br>A period appears.

If you see different output, you might check that you're using the right protocol for your [stenography machine](https://github.com/openstenoproject/plover/wiki/Beginner's-Guide:-Get-Started-with-Plover#stenography-machine).

#### Practice sentences

You can practice sentences that (mostly) only need two keys at once, on the [StenoJig](https://joshuagrams.github.io/steno-jig/two-key) website.

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

It's time to start learning stenography theory for free, practicing writing using stenography, and learning how to make the most of Plover's built-in tools.

* See the [Learning Resources](https://github.com/openstenoproject/plover/wiki/Learning-Stenography) and [the old steno practice page](http://stenoknight.com/wiki/Practice).

### Which steno theory should you learn?

There are many steno theories on the best way of using the steno keyboard.

All English language steno theories are derived from the original Stenotype theory devised by Ward Ireland. They all share the same keyboard design and basic method of representing the sounds. They differ mostly in the details of how they [brief](https://github.com/openstenoproject/plover/wiki/Glossary#brief) words, and how many briefs they use. Some theories are focused on raw speed and efficiency, but require a lot of memorization. Others focus more on consistency and logical rules to reduce the amount of memorization and "on-the-job" mental gymnastics required.

We recommend you start with Plover's StenEd-based theory, and the dictionary that is supplied with the Plover software. After 6 months, you'll have a better understanding of stenography, and you could then start experimenting with different theories. Everyone ends up adapting them and forming a personal style anyway. So you don't need to worry about the different steno theories until you hit 100 WPM or so.

We don't recommend spending money on a theory before you're certain you like stenography.