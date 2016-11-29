This guide explains how to get started with Plover.

## Overview

The main steps are:

1. Install Plover software.
1. Connect a compatible keyboard or stenography (steno) machine.
1. Confirm it's working.
1. Practice and learn stenography using Plover. 

## Install Plover

There are versions of Plover for Windows, OS/X and Mac OS, and Linux. 

* Download and install the [latest release](https://github.com/openstenoproject/plover/releases/latest). 
* See the [installation guide](https://github.com/openstenoproject/plover/wiki/Installation-Guide#installation) for more information.

### Configuring Plover on OS/X and Mac OS

On OS/X and Mac OS, you need to enable [Assistive Device Permissions](https://support.apple.com/en-ca/HT202866) each time you install Plover (`System Preferences > Security & Privacy > Privacy > Accessibility`). Other "keyboard helper" type applications (like Karabiner Elements) may interfere with Plover. 

## Connect a compatible keyboard or stenography machine

###Use a standard keyboard

You can use Plover with a standard keyboard, but there are some important limitations. Stenography often requires you to press five or six keys at once, and sometimes as many as 16. Unfortunately, most keyboards only recognise up to six keys at once. When you need to press more than six keys are once, you have to use a technique called "arpeggiating". See ["How it Works" for more information on arpeggiating](http://qwertysteno.com/Basics/HowItWorks.php) .

Note: To write quickly, you'll need a keyboard with N-key rollover (NKRO), a machine designed for use with Plover, or a professional stenography machine. 

### Use an N-key rollover (NKRO) keyboard

An N-key rollover (NKRO) keyboard is specially designed to allow pressing many keys at once. Most computer gaming ("mechanical") keyboards have NKRO.

See the [[Supported Hardware]] page for a list of supported keyboards.

* The [Zalman ZM-K600S](https://www.amazon.com/Zalman-Unlimited-Multi-Key-keyboard-ZM-K600S/dp/B0196J3IPE) is currently the cheapest option in the USA, at $45-$50.

#### Keytoppers

Most keyboards have the keys in staggered rows, which can make it difficult to press two keys in a column with a single finger. To solve this problem, you can use keytoppers, which are in the shape of the keys on a steno machine, and stick them on top of the relevant keys on the keyboard.  

You can buy laser-cut keytoppers from the [Plover Store](http://plover.deco-craft.com/). You can also make your own keytoppers out of plastic. 

#### NKRO keyboards with an ortholinear layout

Keyboards with an "ortholinear" layout have the keys in straight columns. This is handy for steno, as it makes it easier to press two keys in a column with a single finger. 

* The [Ergodox](https://ergodox-ez.com/) is a fairly high-end NKRO keyboard at $200, with an ortholinear layout. It has two separate halves, so you can angle them to suit you. You can order it with the Gateron White keys, which have a light, 35 gram activation force.
* The [Planck](http://olkb.com/planck/) is a NRKO keyboard with an ortholinear layout. It is 60% smaller than a standard keyboard.

### Use a machine designed for use with Plover

Various steno enthusiasts are making and selling machines designed for use with Plover:

* [StenoMod](http://stenomod.blogspot.com/). 
  * This has light keys and a split design. 
  * See Ted Morin's [review of the StenoMod](http://www.teds.space/2016/10/stenomod-affordable-steno-machine.html).
* [SOFT/HRUF](https://softhruf.love/). 
  * This has the shape of a stenography machine, but is built using computer keys rather than levers. 
  * See Ellis Pratt's [review of the SOFT/HRUF](https://groups.google.com/d/msg/ploversteno/iraOYarRbdg/tlHeagOQGQAJ).
* [StenoBoard](http://stenoboard.com/).

### Use a professional stenography machine
 
Some professional stenography machines are compatible with Plover. You can find used steno machines on eBay at reasonable prices. 

See the [[Supported Hardware]] page for a list of supported professional stenography machines. 

* The most common/popular professional stenography machine used with Plover appears to be the Stentura 400 SRT.

## Confirm it's working ("Hello World")

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a steno machine, you'll need to configure Plover to look for your machine.

### Keyboard

By default, Plover will use your keyboard as its input device. 

1. Run Plover and click the `Enable` radio button. 
 
You may like to go into Plover's `Configure > Display` settings and turn on either the stroke display or the suggestions window.

#### Practice sentences

Try out these [sentences that (mostly) only need two keys at once](https://joshuagrams.github.io/steno-jig/two-key).

#### "Hello World"

To write "hello, world" into a text editor with Plover, using a QWERTY keyboard:

1. Run Plover and click the `Enable` radio button.
1. Open a text editor.
1. Simultaneously press R, N, and O (left index finger on 'R', right thumb on 'N', and right ring finger on 'O'). 
1. Simultaneously press R, F, and V (left index finger between 'R' and 'F', and left thumb on 'V')
1. Simultaneously press J, K, L, and ; (right index finger on 'J', right middle finger on 'K', right ring finger on 'L', and right little (pinky) finger on ';')
1. Simultaneously press D, V, J, O, and [ (left middle finger on 'D', left thumb on 'V', right index finger on 'J', right ring finger on 'O', and right little (pinky) finger on '[')
1. Simultaneously press U, I, O, and P (right index finger on 'U', right middle finger on 'I', right ring finger on 'O', right little (pinky) finger on 'P')

#### Use the correct body posture and finger placement

On a QWERTY keyboard, move your fingers up from the home row so that they rest on the cracks between the keys, and move your thumbs up so they rest on the cracks between `C`/`V` and `N`/`M`. 

Your fingers should be slightly curled, so you press the keys using the tips of your fingers. 

See also:

* [Basic Hand Posture on the Steno Machine](https://www.youtube.com/watch?v=YfHNPW6EnHo)
* [Basic Body Position for Steno Students and Pros](https://www.youtube.com/watch?v=s_zyxgQvNEU)

### Stenography machine

Plover supports several protocols that are in use by various Stenography machines. To configure Plover to the protocol your machine uses:
1. Run Plover and click the `Enable` radio button.
1. Click the 'Configure' button on the Plover Dialog screen. The Plover configuration screen appears. 
1. On the 'Machine' tab, select the protocol your machine uses. 
1. Click 'Save'.

See [Supported protocols](https://github.com/openstenoproject/plover/wiki/Supported-Hardware#supported-protocols) for more information. 

## Practice and learn

* Plover has an excellent introductory textbook and website, called [Learn Plover!](https://sites.google.com/site/ploverdoc/home).

* [Steno Jig](https://joshuagrams.github.io/steno-jig/) is a website where you can practice the Learn Plover exercises. You can also practice the 3,000 most common words.  

See also [[Learning Resources]] and [the old steno practice page](http://stenoknight.com/wiki/Practice).

###Which steno theory should you learn?

There are many steno theories on the best way of using the steno keyboard. 

All English language steno theories are derived from the original Stenotype theory devised by Ward Ireland. They all share the same keyboard design and basic method of representing the sounds. They differ mostly in the details of how they abbreviate words, and how many abbreviations they use. Some theories are focused on raw speed and efficiency, but require a lot of memorisation. Others focus more on consistency and logical rules to reduce the amount of memorisation and "on-the-job" mental gymnastics required.  

We recommend you start with Plover's StenEd-based theory. After 6 months, you'll have a better understanding of stenography, and you could then start experimenting with different theories. Everyone ends up adapting them and forming a personal style anyway. So you don't need to worry about the different steno theories until you hit 100 WPM or so. 