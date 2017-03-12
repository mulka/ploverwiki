This page lists the machine known to work with Plover.

It lists:

* [Stenotype machines](#stenotype-machines)
* [Keyboards with NKRO](#keyboards)
* [Dedicated machines designed for use with Plover](#dedicated-machines-designed-for-use-with-plover)

# Stenotype Machines

## Supported protocols

Plover supports several protocols that are in use by various machines:

* **Stentura serial**: most machines by Stenograph and many others.
* **Gemini PR serial**: typically any recent machine made by the Neutrino Group, such as the Piper, Revolution, or Infinity series.
* **ProCAT**: protocol used by all ProCAT machines.
* **TX Bolt**: an older protocol supported by some machines as a primary or secondary protocol.
* **Treal**: used only by the Treal from Word Technologies.
* **Passport**: used only by the Passport Writer from Advantage Software.

This means that, in theory, many machines work with Plover.

## Known supported stenotypes

The following machines have been confirmed by users to work with Plover
after actually trying it:

| Product Name                       | Manufacturer       | Protocol/Connection | Comments                |
| ---------------------------------- | ------------------ | ------------------- | ----------------------- |
| Elan Cybra Student                 | Stenograph         | TX Bolt (serial)    |                         |
| Flash, Blaze, Impression, and Xpression | ProCAT        | ProCAT              |                         |
| Flash Writer                       | ProCAT             | TX Bolt             | Press `Mode` (far right button), click `Setup`, then press the `Emul` button. Display should read `Emulate: Baron` |
| Gemini2                            | Neutrino Group     | Gemini PR (serial)  |                         |
| Gemini RT                          | Neutrino Group     | TX Bolt             | Must start a job on screen or in [Infinity2](http://www.infinitytraditional.com/infinity-2/) |
| Lightspeed                         | Stenovations       | TX Bolt (serial over USB/Bluetooth) | Baud rate 9600 |
| Infinity Ergonomic                 | Neutrino Group     | Gemini PR (serial over USB/Bluetooth)  | Baud rate 115200 |
| Infinity Genesis                   | Neutrino Group     | Gemini PR (serial)  |                         |
| Passport                           | Advantage Software | Passport (USB)      |                         |
| Passport Touch                     | Advantage Software | USB, Bluetooth | While in "Emulation Mode": Stentura over Bluetooth or TX Bolt over USB ﻿ |
| Protege                            | Stenograph         |                     |                         |
| Revolution Grand                   | Neutrino Group     | Gemini PR (serial)  |                         |
| Stentura 400 SRT                   | Stenograph         | Stentura (serial)   | [[Setup Instructions|How-to-setup-and-use-Plover-with-a-Stentura-400SRT]]  |
| Tréal                              | Word technologies  | Treal (USB)         |                         |
| Wave                               | Stenograph         |                     |                         |

# Keyboards

If you don't have a steno machine, you can use a keyboard that supports N-Key Rollover (NKRO).

## What's NKRO?

This is a feature that certain keyboards have that let the keyboards
register each key regardless of other keys being pressed. Read the
[Wikipedia entry about NKRO](http://en.wikipedia.org/wiki/Rollover_(key)#n-key_rollover).

## How do I know if my keyboard has NKRO?

### Simple test
To test your keyboard for NKRO capability:

1. Open up a text editor.
2. Hold down both shift keys.
3. Type each letter on your keyboard. 

> **Note**: You must hold down both shift keys while you type each letter on your keyboard.

If all keys are typed into the text editor, your keyboard probably has NKRO.

### Microsoft's keyboard ghosting demonstration website test
[Microsoft's keyboard ghosting demonstration website](http://www.microsoft.com/appliedsciences/content/projects/KeyboardGhostingDemo.aspx) provides a browser-based application that lets you test your keyboard's capabilities for registering multiple key presses. 

To test your keyboard:

1. Open your web browser and go to [Microsoft's keyboard ghosting demonstration website](http://www.microsoft.com/appliedsciences/content/projects/KeyboardGhostingDemo.aspx).
1. Click "**Click To Use**". Each key you press will light up green in the picture of a keyboard. 
1. Press the middle row keys `asdfjkl;`.
  * With a normal keyboard only 6 of the 8 keys will light up green (maybe fewer).
  * If your keyboard has N-key rollover, all 8 keys will light up green. 
1. Press other multiple-key combinations, such as `yuhj`, and see if they all light up green.

## What if my keyboard is not capable of NKRO?

If you don't have a keyboard that's capable of NKRO, but still want to give Plover a try, you can arpeggiate/roll the keyboard chords. More info can be found at the bottom of [this post](http://plover.stenoknight.com/2011/02/plover-211-released.html).

## Known supported keyboards

> **Warning**: Be wary of false advertising; some keyboards are advertised as NKRO or anti-ghosting, but are limited to certain combinations. Check reviews to get confirmation before making a purchase. Some keyboards might only support full-NKRO over a PS/2 connector (the [old-style plug](https://en.wikipedia.org/wiki/PS/2_port#/media/File:Ps-2-ports.jpg).) Full NKRO over USB is possible. Many keyboards do it well, and will work with Plover.

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                | Manufacturer           | Comments        | Price
| --------------------------- | ---------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| Apex m-800                  | SteelSeries            | NKRO over USB   | [$199](https://steelseries.com/gaming-keyboards/apex-m800)
| CM Storm Quickfire TK       | Cooler Master          | NKRO over USB   | [$85](http://www.amazon.com/CM-Storm-QuickFire-TK-Mechanical/dp/B00A378L4C/)
| Noppoo Choc                 | Noppoo                 | NKRO over USB   | [$95](http://www.amazon.com/Noppoo-84-Technology-Mechanical-Keyboard/dp/B0091Q34EI/ref=sr_1_1?s=pc&ie=UTF8&qid=1458020924&sr=1-1-spons&keywords=noppoo+choc+mini&psc=1)
| Ergo Pro                    | Matias                 | NKRO over USB   | [$200](http://matias.ca/ergopro/pc/)
| Ergodox                     | Ergodox                | NKRO over USB   | [$295](https://www.indiegogo.com/projects/ergodox-ez-an-incredible-mechanical-keyboard)
| G710+                       | Logitech               | NKRO over USB   | [$130](http://gaming.logitech.com/en-us/product/g710plus-mechanical-gaming-keyboard)
| Keyboardio                  | Keyboardio             | NKRO over USB   | [$329](http://shop.keyboard.io)
| Majestouch-2                | Filco                  | NKRO over USB   | [$167](http://amzn.to/oLy2xQ)
| Das Keyboard 4 Ultimate     | Das Keyboard           | NKRO over USB   | [$169](http://shop.daskeyboard.com/products/das-keyboard-4-ultimate/)
| Ultimate Hacking Keyboard   | Ultimate Gadget Labs   | NKRO over USB   | [$250](https://www.crowdsupply.com/ugl/ultimate-hacking-keyboard)
| Vengeance K65               | Corsair                | NKRO over USB   | [$90](http://www.corsair.com/en/gaming-peripherals/gaming-keyboards/vengeance-k65-compact-mechanical-gaming-keyboard.html)
| ZM-K600S                    | Zalman                 | NKRO over USB   | [$40](http://www.amazon.com/Zalman-Unlimited-Multi-Key-keyboard-ZM-K600S/dp/B0196J3IPE)

### Which type of key switch should I choose?

Stenography works best when the keyboard takes little force to depress keys. The lighter, the better. Ideally, the switch will be linear, it should lack any clicks or bumps. The lighter the force, the better, for steno. In the Cherry MX line, the best switch is Red, at 45 cN actuation. For Gaterons, the best switch for steno is Clear/White (different names, same switch), at only 35 cN actuation.

## Adapt a keyboard for steno use

Most keyboards have the keys in staggered rows, which can make it difficult to press two keys in a column with a single finger. To adapt a keyboard for steno use, you can use:

* Keytoppers
* Keycaps
* A keyboard with an ortholinear layout

### Keytoppers

Laser-cut keytoppers are in the shape of the keys on a steno machine, and stick them on top of the relevant keys on the keyboard. You can buy laser-cut keytoppers from the [Plover Store](http://plover.deco-craft.com/). You can also make your own keytoppers out of plastic or even coins.
 
### Keycaps

If you have a mechanical keyboard, it is likely your keys have a [Cherry MX stem](https://deskthority.net/wiki/Cherry_MX) and will work with custom keycaps. You can replace the existing keycaps on your keyboard with different keycaps, to improve the layout for stenoing.

- [StenoToppers](https://cemrajc.github.io/stenotoppers/) is a 3D printed keycap set designed by Jason Cemra. It aligns the rows, raises the keys, and reduces the keycap tapering, slant and gap. A pre-release version of the the 3d model (.stl) files is available on Github. If you have access to a 3D printer, you can download .stl files and print them for a negligible cost. Otherwise, you would need to use a 3D printing service.
- The [G20 keycap set](http://pimpmykeyboard.com/g20-blank-keycap-sets/) from Signature Plastics is a great set for steno, and will fit on an ErgoDox or other mechanical keyboard. The keys have a direction, so for optimal comfort, you should angle the top row of steno (`STPH...`) down, so that they are close to the bottom row (`SKWR...`)
- You can 3D-print a [steno-friendly keycap](https://github.com/morinted/stenomod_case).

Keys that have little space between them are good for steno, because then you can hit two neighboring keys with one finger (which is frequently necessary).

### NKRO keyboards with an ortholinear layout

Keyboards with an "ortholinear" layout have the keys in straight columns. This is handy for steno, as it makes it easier to press two keys in a column with a single finger. 

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                       | Manufacturer       | Protocol/Connection | Comments                |
| ---------------------------------- | ------------------ | ------------------- | ----------------------- |
| [ErgoDox](https://deskthority.net/wiki/ErgoDox)           |   ErgodoxEZ, Massdrop, FalbaTech, others |  USB  |     The ErgoDox is a fairly high-end NKRO keyboard at $200, with an ortholinear layout. It has two separate halves, so you can angle them to suit you. You can order it with the Gateron White keys, which have an extremely light, 35 gram activation force.                    |
| [Planck](http://olkb.com/planck/) | OLKB | USB | The Planck is a NKRO keyboard with an ortholinear layout. It is 40% the size of a standard keyboard.|
|[Preonic](http://olkb.com/preonic/)| OLKB | USB | The Preonic is a NKRO keyboard with an ortholinear layout. It is 50% the size of a standard keyboard. |

# Dedicated machines designed for use with Plover

Various steno enthusiasts are making and selling machines designed for use with Plover.

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                       | Manufacturer       | Protocol/Connection | Comments                |
| ---------------------------------- | ------------------ | ------------------- | ----------------------- |
| [SOFT/HRUF](https://softhruf.love) | Scott Urueta       | TX Bolt (serial)    | Open source hardware. This has the shape of a stenography machine, but is built using computer keys rather than levers. The name is the steno representation for, and is pronounced as, "soft love".  |
| [Stenoboard](http://utopen.com)    | Utopen (Emanuele Caruso) | NKRO/TX Bolt/Gemini PR | Open source hardware. The first open source steno machine on the market, released in 2014. The Stenoboard's keys actuate like mouse-clicks instead of a keyboard or lever-machine. |
| [Stenomod](https://stenomod.blogspot.com) | Charley Shattuck | TX Bolt        | Open source hardware. This has light keys and a split design. See Ted Morin's [review of the StenoMod](http://www.teds.space/2016/10/stenomod-affordable-steno-machine.html). The name is supposed to hint at how the machine is "modular" and adaptable. It is very barebones so it is easy to take apart and customize. |

