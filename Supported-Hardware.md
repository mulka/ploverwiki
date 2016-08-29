# Stenotype Machines

## Supported protocols

Plover supports several protocols that are in use by various machines:

* **Stentura serial**: most machines by Stenograph and many others.
* **Gemini PR serial**: typically any recent machine made by the Neutrino Group, such as the Piper, Revolution, or Infinity series.
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
| [SOFT/HRUF](https://softhruf.love) | Scott Urueta       | TX Bolt (serial)    | Open source hardware    |
| [Stenoboard](http://utopen.com)    | Utopen             | NKRO/TX Bolt/Gemini PR | Open source hardware    |
| Stentura 400 SRT                   | Stenograph         | Stentura (serial)   |                         |
| Tréal                              | Word technologies  | Treal (USB)         |                         |
| Wave                               | Stenograph         |                     |                         |

# Keyboards

Plover is best used with a keyboard supporting N-Key Rollover (NKRO).

## What's NKRO?

This is a feature that certain keyboards have that let the keyboards
register each key regardless of other keys being pressed. Read the
[Wikipedia entry about NKRO](http://en.wikipedia.org/wiki/Rollover_(key)#n-key_rollover).

## How do I know if my keyboard has NKRO?

A simple test is to open up a text editor and--while holding down both
shift keys--type each letter on your keyboard. If all keys are typed
into the text editor, your keyboard probably has NKRO.

[This site](http://www.microsoft.com/appliedsciences/content/projects/KeyboardGhostingDemo.aspx)
provides a web application that lets you test your keyboard's
capabilities for registering multiple key presses. To test, click where
it says "click to use", then each key you press lights up green in the
picture of a keyboard. Press the middle row keys asdfjkl; and with a
normal keyboard only 6 of the 8 keys will light up green, maybe fewer,
but if your keyboard has n-key rollover, all 8 will light up green. Then
press other multiple-key combinations such as yuhj and see if they all
light up green.

## What if my keyboard is not capable of NKRO?

If you don't have a keyboard that's capable of NKRO, but still want to
give Plover a try, you can arpeggiate/roll the keyboard chords. More
info can be found at the bottom of [this post](http://plover.stenoknight.com/2011/02/plover-211-released.html).

## Known supported keyboards

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

