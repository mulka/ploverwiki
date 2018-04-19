This page lists the machine known to work with Plover.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Dedicated machines designed for use with Plover](#dedicated-machines-designed-for-use-with-plover)
- [Stenotype Machines](#stenotype-machines)
  - [Supported protocols](#supported-protocols)
  - [Known supported stenotypes](#known-supported-stenotypes)
- [Keyboards](#keyboards)
  - [What's NKRO?](#whats-nkro)
  - [How do I know if my keyboard has NKRO](#how-do-i-know-if-my-keyboard-has-nkro)
    - [Test #1: Double Shift](#test-1-double-shift)
    - [Test #2: Keyboard Ghosting Test](#test-2-keyboard-ghosting-test)
  - [What if my keyboard is not capable of NKRO?](#what-if-my-keyboard-is-not-capable-of-nkro)
  - [Known supported keyboards](#known-supported-keyboards)
    - [Which type of key switch should I choose?](#which-type-of-key-switch-should-i-choose)
  - [Adapt a keyboard for steno use](#adapt-a-keyboard-for-steno-use)
    - [Keytoppers](#keytoppers)
    - [Keycaps](#keycaps)
  - [NKRO keyboards with an ortholinear layout](#nkro-keyboards-with-an-ortholinear-layout)
- [Notebooks with NKRO](#notebooks-with-nkro)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Dedicated machines designed for use with Plover

Various steno enthusiasts are making and selling machines designed for use with Plover.

| Product Name                       | Manufacturer       | About                   | Price |
| ---------------------------------- | ------------------ | ----------------------- | ----- |
| [Stenomod](https://stenomod.blogspot.com) | Charley Shattuck | Open source hardware. This has light keys and a split design. See [Ted Morin's review of the Stenomod](http://www.tedmor.in/blog/posts/stenomod-affordable-steno-machine) as well as [Martin Körner's review](https://stenoblog.com/the-stenomod/). The name is supposed to hint at how the machine is "modular" and adaptable. It is very barebones so it is easy to take apart and customize. <br /> ![Stenomod](https://2.bp.blogspot.com/-n7j50BDdjAg/WJECk94jwCI/AAAAAAAAAI4/2E-G1dgflccCltPFN9FEPI4QtMW62ttCQCK4B/s400/20170131_131923.jpg) | $200 |
| [SOFT/HRUF](https://softhruf.love) | Scott Urueta       | Open source hardware. This has the shape of a stenography machine, but is built using computer keys rather than levers. The name is the steno representation for, and is pronounced as, "soft love". <br /> ![SOFT/HRUF](https://i.imgur.com/pvmzoQy.png) | $138 (preorder) |
| [Stenoboard](http://utopen.com)    | Utopen (Emanuele Caruso) | Open source hardware. The first open source steno machine on the market, released in 2014. The Stenoboard's keys actuate like mouse-clicks instead of a keyboard or lever-machine. ![](http://stenoboard.com/images/stenoboard.jpg)| Out of production |

# Stenotype Machines

<img src="http://www.stenograph.com/product/image/large/45009_wave.jpg" width="300"/>

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
| Flash, Blaze, Impression, and Xpression | ProCAT        | ProCAT (serial, *maybe*)             | (For Blaze and other Windows CE-based writers) USB cannot be used with Plover, it is only to transfer files created on the Blaze to your PC or CAT software. USB does not work on Windows 10, only Windows XP (with ActiveSync), and Windows Vista/7/8 with WMDC.exe (Windows Mobile Device Center). Both are abandonware. You need an RJ11 (male) to DB9 (female) to use this writer. |
| Flash Writer                       | ProCAT             | TX Bolt             | Press `Mode` (far right button), click `Setup`, then press the `Emul` button. Display should read `Emulate: Baron` |
| Gemini2                            | Neutrino Group     | Gemini PR (serial)  |                         |
| Gemini RT                          | Neutrino Group     | TX Bolt             | Must start a job on screen or in [Infinity2](http://www.infinitytraditional.com/infinity-2/) |
| Lightspeed                         | Stenovations       | TX Bolt (serial over USB/Bluetooth) | Baud rate 9600 |
| Infinity Ergonomic                 | Neutrino Group     | Gemini PR (serial over USB/Bluetooth)  | Baud rate 115200 |
| Infinity Genesis                   | Neutrino Group     | Gemini PR (serial)  |                         |
| Passport                           | Advantage Software | Passport (USB)      |                         |
| Passport Touch                     | Advantage Software | USB, Bluetooth | While in "Emulation Mode": Stentura over Bluetooth or TX Bolt over USB ﻿ |
| Protege                            | Stenograph         | Stentura (serial)   | Connect Serial-to-USB cable to serial port of Protege. Use USB jack for power only (USB drivers not avail.) [Setup Instructions](https://github.com/openstenoproject/plover/wiki/Stentura-Protege-Setup-and-Usage-Instructions)|
| Revolution Grand                   | Neutrino Group     | Gemini PR (serial)  |                         |
| Stentura 400 SRT                   | Stenograph         | Stentura (serial)   | [Setup Instructions](https://github.com/openstenoproject/plover/wiki/How-to-setup-and-use-Plover-with-a-Stentura-400SRT)  |
| Tréal                              | Word technologies  | Treal (USB)         |                         |
| Wave                               | Stenograph         |                     |                         |

# Keyboards

If you don't have a steno machine, you can use a keyboard that supports N-Key Rollover (NKRO).

<img src="http://www.zalman.com/DataFile/product/B_0001_%EB%A0%88%EC%9D%B4%EC%96%B4%204.jpg" width="300"/>

## What's NKRO?

This is a feature of some keyboards that means that you can press as many keys as you want simultaniously, and they will all register. Typical keyboards stop working correctly when you press somewhere between 4 and 7 keys at once.
For more information, see the [Wikipedia entry about NKRO](http://en.wikipedia.org/wiki/Rollover_(key)#n-key_rollover).

## How do I know if my keyboard has NKRO

In general, most keyboards will not be NKRO. "Gamer" and mechanical keyboards are most likely to have NKRO, while budget as well as laptop keyboards are unlikely to have NKRO.

### Test #1: Double Shift

**Note: this test results in a false positive on some Macbooks**

To test your keyboard for NKRO capability:

1. Open up a text editor.
2. Hold down both shift keys.
3. Type each letter on your keyboard (from A-Z).

> **Note**: You must hold down both shift keys while you type each letter on your keyboard.

If all keys are typed into the text editor, your keyboard probably has NKRO.

### Test #2: Keyboard Ghosting Test
[Keyboard Ghosting Test](https://scratch.mit.edu/projects/20966625/) provides a browser-based application that lets you test your keyboard's capabilities for registering multiple key presses. 

To test your keyboard:

1. Open your web browser and go to [Keyboard Ghosting Test](https://scratch.mit.edu/projects/20966625/).
1. Click the flag to start.
    * Each key you press will light up in the picture of a keyboard. 
1. Press the middle row keys `asdfjkl;`.
    * With a normal keyboard only 6 of the 8 keys will light up (maybe fewer).
    * If your keyboard has N-key rollover, all 8 keys will light up. 
1. Press other multiple-key combinations, such as `yuhj`, and see if they all light up.

## What if my keyboard is not capable of NKRO?

If you don't have a keyboard that's capable of NKRO, but still want to give Plover a try, you can arpeggiate/roll the keyboard chords. More info can be found at the bottom of [this post](http://plover.stenoknight.com/2011/02/plover-211-released.html).

## Known supported keyboards

> **Warning**: Be wary of false advertising; some keyboards are advertised as NKRO or anti-ghosting, but are limited to certain combinations. Check reviews to get confirmation before making a purchase. Some keyboards might only support full-NKRO over a PS/2 connector (the [old-style plug](https://en.wikipedia.org/wiki/PS/2_port#/media/File:Ps-2-ports.jpg).) Full NKRO over USB is possible. Many keyboards do it well, and will work with Plover.

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                | Manufacturer           | Comments        | Price
| --------------------------- | ---------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| Apex m-800                  | SteelSeries            | NKRO over USB   | [$199](https://steelseries.com/gaming-keyboards/apex-m800)
| CM Storm Quickfire TK       | Cooler Master          | NKRO over USB   | [$85](http://www.amazon.com/CM-Storm-QuickFire-TK-Mechanical/dp/B00A378L4C/)
| Francium Pro                  | Deck            | NKRO over USB when in "lightning" mode (Fn + F10). Full NKRO works on Windows and Linux, but is rumored NOT to work on Macs (you'd be stuck with 6KRO).  | [$94](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=690)
| Noppoo Choc                 | Noppoo                 | NKRO over USB (works on Mac without adapters)   | [$95](http://www.amazon.com/Noppoo-84-Technology-Mechanical-Keyboard/dp/B0091Q34EI/ref=sr_1_1?s=pc&ie=UTF8&qid=1458020924&sr=1-1-spons&keywords=noppoo+choc+mini&psc=1)
| Ergo Pro                    | Matias                 | NKRO over USB   | [$200](http://matias.ca/ergopro/pc/)
| Ergodox                     | Ergodox                | NKRO over USB   | [$295](https://www.indiegogo.com/projects/ergodox-ez-an-incredible-mechanical-keyboard)
| G710+                       | Logitech               | NKRO over USB   | [$130](http://gaming.logitech.com/en-us/product/g710plus-mechanical-gaming-keyboard)
| Keyboardio                  | Keyboardio             | NKRO over USB   | [$329](http://shop.keyboard.io)
| Majestouch-2                | Filco                  | NKRO over USB   | [$167](http://amzn.to/oLy2xQ)
| Das Keyboard 4 Ultimate     | Das Keyboard           | NKRO over USB requires key sequence to enable. See fine print on underside of keyboard   | [$169](http://shop.daskeyboard.com/products/das-keyboard-4-ultimate/)
| Ultimate Hacking Keyboard   | Ultimate Gadget Labs   | NKRO over USB   | [$250](https://www.crowdsupply.com/ugl/ultimate-hacking-keyboard)
| Vengeance K65               | Corsair                | NKRO over USB   | [$90](http://www.corsair.com/en/gaming-peripherals/gaming-keyboards/vengeance-k65-compact-mechanical-gaming-keyboard.html)
| I-500 Victop (compact: 87 keys)     | Eastern times tech | NKRO over USB   | [27 GBP](https://www.amazon.co.uk/Water-Resistant-VicTop-Mechanical-Waterproof-Anti-ghosting/dp/B01DBYNVSY/)
| ZM-K600S                    | Zalman                 | NKRO over USB   | [$40](http://www.amazon.com/Zalman-Unlimited-Multi-Key-keyboard-ZM-K600S/dp/B0196J3IPE)
| X51 (Gaming Mechanical Keyboard 87/104) | Metoo                | NKRO over USB   | [$40](https://www.aliexpress.com/item/Metoo-Gaming-Mechanical-Keyboard-87-104-Anti-ghosting-Luminous-Blue-Red-Black-Switch-Backlit-LED-wired/32782819448.html) 
| TOMOKO (87 key Mechanical Keyboard) | TOMOKO               | NKRO over USB   | [$26](https://www.amazon.com/TOMOKO-Water-Resistant-Mechanical-Keyboard-Non-Conflicting/dp/B01DBJTZU2/)

### Which type of key switch should I choose?

Because you hit many keys with steno at once, there are two properties that are useful to have in a mechanical keyboard switch for steno: a **light actuation force** on a **linear** switch.

The light actuation makes it easier on your hands. For a chord like `TKPWHRAOEUGD` (gliding), you are hitting 8 keys with your left hand. That means that whatever switch force you need to depress one key, you have to push 8-times as much. For a 80cN (~80 grams, ~2.9 oz) switch, that's 640cN (~640g, ~22.6 oz). For this reason, your wrists will have a much easier time working with your machine if its actuation force is as light as possible.

The linearity is recommended because it's been found that the tactile feedback that one gets from an individual switch is not as useful when you are receiving 4-10 of those feedbacks at once. The brain just doesn't process all the fingers' feedback in a useful manner. And since the bump usually requires a small addition to the actuation force, we recommend keeping it linear and simple.

Professional steno machines, historically, always bottomed out (meaning the keys are pressed until they can no longer travel; the bottom.) Newer machines use more complicated mechanisms for detecting key travel, often using magnets and the hall effect to determine where the key is, allowing for customizable actuation points. The typical force required for a modern steno machine is between **10cN and 20cN**, with some extremes on either end for personal preference. The travel of a typical lever steno machine is usually between **2mm and 30mm**. The lower end is found in machines like the LightSpeed (nonlever), where the higher end is around the maximum that you can configure a lever machine to stroke.

Most of the mechanical switches have a 2mm actuation point and 4mm travel/bottoming out, but some community members have found that "speed switches" with an earlier actuation point (usually 1.1-1.4mm) are better for steno due to their increased sensitivity.

| Switch | Stat | Note | Machines |
| ------ | ---- | ---- | ------- |
| Gateron Clear / White | 35 cN linear | Best stock option available on the market | Stenomod uses this switch |
| Matias Red | 35 cN linear | Feels heavier than 35 cN switches due to having a "flat" force curve. Matias also has a different stem from Cherry | SOFT/HRUF uses this switch |
| Cherry MX Red | 45 cN linear | | |
| Kailh Silver | 50 cN spring* linear | Has an early actuation (1.1mm vs 2mm) | |
| Cherry MX Brown | 45 cN bumpy | While not ideal compared to other options, this switch is still a better choice than blues, blacks, and other Cherry switches | |

\* The Kailh silvers use a spring that would cause a 50 cN actuation point at 2mm, but since they actuate earlier (1.1mm), the force required is nearer to 35 cN.

There are other methods to decrease actuation force for even these switches. This includes:

- Putting the Gateron Clear's 35 cN spring into the Kailh Silver for its earlier actuation point.
- Trimming the springs of a linear switch by several mm to reduce force.
- Using an aftermarket spring with lower forces, such as a prototype 20 cN spring that isn't yet released to the wider market.
- Removing the leaf-spring (not the primary spring) in the Matias Red switch to make the force curve less flat.

## Adapt a keyboard for steno use

![](https://c1.staticflickr.com/5/4202/34180678224_98d3e26f1f_n.jpg)

Most keyboards have the keys in staggered rows, which can make it difficult to press two keys in a column with a single finger. To adapt a keyboard for steno use, you can use:

* Keytoppers
* Keycaps

You can also use a keyboard with an ortholinear layout.

### Keytoppers

Laser-cut keytoppers are in the shape of the keys on a steno machine. You stick them on top of the relevant keys on the keyboard. You can buy laser-cut keytoppers from the [Plover Store](http://plover.deco-craft.com/). You can also make your own keytoppers out of plastic or even coins.

![Laser-cut keytoppers sitting in a pile](http://i.imgur.com/cjWDy2J.jpg)
 
### Keycaps

If you have a mechanical keyboard, it is likely your keys have a [Cherry MX stem](https://deskthority.net/wiki/Cherry_MX) and will work with custom keycaps. You can replace the existing keycaps on your keyboard with different keycaps, to improve the layout for stenoing.

- [StenoToppers](https://cemrajc.github.io/stenotoppers/) is a 3D printed keycap set designed by Jason Cemra. It aligns the rows, raises the keys, and reduces the keycap tapering, slant and gap. The 3d model (.stl) files are available on Github. If you have access to a 3D printer, you can download .stl files and print them for a negligible cost. Otherwise, you would need to use a 3D printing service.

  <img src="http://imgur.com/FRwXu8x.jpg" width="400">

- The [G20 keycap set](http://pimpmykeyboard.com/g20-blank-keycap-sets/) from Signature Plastics is a great set for steno, and will fit on an ErgoDox or other mechanical keyboard. The keys have a direction, so for optimal comfort, you should angle the top row of steno (`STPH...`) down, so that they are close to the bottom row (`SKWR...`)
- You can 3D-print a [steno-friendly keycap](https://github.com/morinted/stenomod_case).

Keys that have little space between them are good for steno, because then you can hit two neighboring keys with one finger (which is frequently necessary).

## NKRO keyboards with an ortholinear layout

Keyboards with an "ortholinear" layout have the keys in straight columns. This is handy for steno, as it makes it easier to press two keys in a column with a single finger. 

The following machines have been confirmed by users to work with Plover after actually trying it:

| Product Name                       | Manufacturer       | Protocol/Connection | Comments                |
| ---------------------------------- | ------------------ | ------------------- | ----------------------- |
| [ErgoDox](https://deskthority.net/wiki/ErgoDox)           |   ErgodoxEZ, Massdrop, FalbaTech, others |  USB  |     The ErgoDox is a fairly high-end NKRO keyboard at $200, with an ortholinear layout. It has two separate halves, so you can angle them to suit you. You can order it with the Gateron White keys, which have an extremely light, 35 gram activation force.                    |
| [Planck](http://olkb.com/planck/) | OLKB | USB | The Planck is a NKRO keyboard with an ortholinear layout. It is 40% the size of a standard keyboard.|
|[Preonic](http://olkb.com/preonic/)| OLKB | USB | The Preonic is a NKRO keyboard with an ortholinear layout. It is 50% the size of a standard keyboard. |

# Notebooks with NKRO

If you want to always have steno on the go, you might consider finding a notebook with NKRO. Note that not all these machines are equivalent in terms of actuation force or key shape. You might find, for example, that chiclet keys don't feel as good as the Alienware's classic keyboard style. It's always best to try laptop keyboards at a local store, if possible.

| Model    | Screen Size | Manufacturer    | Rollover | Price (USD) | Weight |
| -------- | ----------- | --------------- | ------- | ----- | ------ |
| [Predator Triton 700](https://us-store.acer.com/predator-triton-700-gaming-laptop-pt715-51-732q) | 15" | Acer | n-key | $3000 | 5.3 lbs |
| [Zephyrus GX501](https://www.asus.com/ca-en/Laptops/ROG-ZEPHYRUS-GX501/) | 15"   | Asus        | 30-key   | $2500     | 4.85lbs |
| [GL502](https://www.asus.com/ca-en/ROG-Republic-Of-Gamers/ROG-GL502VT/)    | 15"         | Asus        | 30-key   | $1900 | 4.9 lbs |
| [GL553](https://www.asus.com/ca-en/Laptops/ROG-GL553VD/)    | 15"         | Asus        | 30-key  | $1200     | 5.5 lbs |
| Aorus [X5 v8](https://www.aorus.com/product-detail.php?p=744) and [X7 v8](https://www.aorus.com/product-detail.php?p=745) | 15", 17" | Aorus | 80-key | $2600, $3000 | 5.51 lbs, 7.05 lbs |
| [Alienware R3/R4](http://www.dell.com/en-us/shop/dell-laptops/sc/laptops/alienware-laptops) | 13", 15", 17" | Dell        | n-key | **$1000** to $3000 | 5.8 to 9.8 lbs |
| [Aero 15/15x](https://www.gigabyte.com/us/Laptop/AERO-15--i7-8750H) | 15"      | Gigabyte    | 80-key   | $2000 to $2900 | **4.6 lbs** |
| [P57X](https://www.gigabyte.com/Laptop/P57X-v7)     | 17"         | Gigabyte    | 30-key   | $1800     | 6.6 + 2.2 (power adaptor) lbs |
| HP Omen [15](https://store.hp.com/us/en/pdp/omen-by-hp---15-ce051nr) and [17](https://store.hp.com/us/en/pdp/omen-by-hp---17-an053nr) | 15", 17" | HP | 26-key | $1900 | 5.77 lbs, 8.23 lbs |
| [Legion Y920](https://www3.lenovo.com/us/en/laptops/ideapad/lenovo-legion-y-series-laptops/Legion-Y920/p/88GMY900877) | 17" | Lenovo | 100-key | $2200 | 10.1 lbs |