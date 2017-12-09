## What you need

1. Stentura Stenograph machine
    
    This was done with a **Stentura 400SRT**, but it should work with others versions (e.g. 200SRT), as long as it is the electric version.
1. A serial cable.

    There are a couple options here:
    + **Option 1: Stenograph realtime cable kit**

        The one that usually comes with the Stentura comes in three parts. A grey connector, a black connector, and a cable. **There's nothing special about this cable**, even though they try to pretend there is. So if you don't already have it, don't spend the amounts of money they are charging to get one. **Use Option 2 instead.**
    + **Option 2: Any RS232 (Also called DB9) male to female cross over-cable**

        This is also known as Null Modem. This is a serial cable that will work with the machine.

        Here are a few options from Amazon:
        - [StarTech SCNM9FM2MBK](https://www.amazon.com/StarTech-com-RS232-Serial-Female-SCNM9FM2MBK/dp/B00CEMGMMM/)
        - [Serial Modem Cable Female RS232](https://www.amazon.com/Serial-Modem-Cable-Female-RS232/dp/B0026KE4CM/)
        - [C2G Female RS322 Adapter](https://www.amazon.com/C2G-Cables-Go-Female-Adapter/dp/B000067RW2/) — No cable, so very short. Useful to minimize the amount of cords
        - [Cables Online Transfer Adapter](https://www.amazon.com/CablesOnline-Slimline-Transfer-Adapter-AD-N04M-2/dp/B00HGIRU3O/) — Even shorter

1. USB to serial adapter

    If you intend to connect to a PC serial port directly, you are already all set with the machine and serial cable. If you want to connect via USB, then you'll also need a USB to serial adapter. If you're not sure if you'll need it, then you probably need it.

    * Serial (Female connector) to USB converter. Once again, here are some options:
        + [Sabrent Serial RS232 Converter](https://www.amazon.com/Sabrent-Serial-RS-232-Converter-CB-DB9P/dp/B00IDSM6BW/)
        + [Tera Grand Premium USB to serial adapter](https://www.amazon.com/Tera-Grand-Premium-Adapter-Supports/dp/B00BUZ0K68/) — No cable, so very short

    Most of these USB to serial adapters come with driver files that you have to install before the adapter works. After installing the driver, make sure you reboot your computer or you probably won't be able to connect to your machine.

**It's important that there is a cross-over cable at some point of the connection, and only one. The Stenograph cable has one built in.** If you purchased any of the "option 2" cables, those are also cross-over cables and will work.

The terms "RS232" and "DB9" mean the same thing and can be used interchangeably. The same goes for "Cross-over" and "Null Modem"

## Putting it all together

If you have a **USB port:**

- Computer USB port → USB to serial adapter → serial cross-over cable → steno machine

If you have a **serial port** on your computer:

- Computer serial port → serial cross-over cable → steno machine

## Connecting to Plover

### Turning on your Stenograph Machine

Turn on the Stenograph with the switch on the face plate.

The green light indicates that the machine is powered on.

The red light signifies connection with a computer.

If the red light is blinking, or the green and red are blinking back and forth, don't worry, it'll still work. If you want to stop the blinking, there are some instructions later.

### Configuring Plover

Next, we can connect Plover to use the device. In Plover, click **Configure**. In the Configuration window, click **Machine**. In the "machine" dropdown, select **Stentura**.

Click the **Scan** button, next to **Port**. This will refresh the Port list. You'll need to find the correct port number. If there is only one, it's probably the one you want. If there is more that one, you can try a few until you find the one that works. If you're using a USB device, it's likely to be the larger number. If you're connecting to the serial port directly, it'll probably be the first one.

When using the USB converter, the other settings should stay at the defaults. Which are 9600, 8, N, 1, no flow control. When connecting with a serial port, it is recommended to use a baud rate of 2400.

Press `OK` to get out of the Configure menu, until you get back to the main Plover screen. Click the refresh button, and it should say `Stentura: connected`. If not, then something went wrong, double check all the steps above.

That's it. You should get output when typing.

## Stop the blinking

The lights blink when the internal memory is full, or if the battery is drained, or both.
if the green light is blinking, then the battery is drained. To charge, leave it plugged in and *turned on*. A good battery will charge in about 8 hours. It's possible that the battery is dead. If you bought the unit second hand and a few years old, then it's very likely to be dead. If that's the case, the light will never stop blinking, no matter how much you try charging it. If you remove the battery, the light will stop blinking and will continue to work with the power cable. The dead battery is useless anyway, so throw it away and now your unit is lighter. (Or buy a new one http://www.stenoworks.com/writer-accessories/writer-batteries/ )

If the red light is blinking, then the internal memory is full or close to full. To clear it:

* turn the Stenograph off
* while holding STK, turn the machine become on.
* the lights should be both blinking back and forth. If not, try again from the start.
* press KWR to clear the memory, or TPH if you change your mind.

The memory will get full regularly so you'll have to do this occasionally. So remember it!

## Manual

Valentin from the [Plover Forums](https://groups.google.com/d/msg/ploversteno/dhLSXsPdGYY/jZQlVdcIAQAJ) has kindly scanned the entire manual. It is very useful to read, and you can get it [here](https://0au.de/~apo/stentura_200_400_srt_manual.pdf).

## Resurrect a dead Stentura 200SRT/400SRT

If the electronics in your 200SRT/400SRT aren't working, you may be interested in replacing them altogether with an Arduino controller. The machine will then be powered over USB through the Arduino -- don't plug in its own power supply lest you destroy your Arduino. The electric paper tape advance will not work; if you want paper tape you'll have to put the mechanism in manual mode (see the instructions) which has a slightly heavier touch, but you don't need paper tape for plover. Likewise, it will no longer have the ability to record strokes for later playback when not connected to the computer.

It is a pretty simple task requiring soldering 6 wires to the I/O Expander board that is located on 
top of the steno mechanism, just under the cover that opens. There's a [video](https://youtu.be/ccxri4A-SbM) and an [Arduino sketch](https://github.com/balthamos/steno-arduino). There is a debouncing delay constant in the sketch that may need to be increased if your machine produces multiple outputs in plover for a single stroke. 

Note: this relies on the electronics on the I/O Expander board still working -- it is a collection of shift register ICs and seems likely to work even if the main electronics board at the bottom of the machine is no longer working. It would be a bigger job to wire the Arduino directly to all 24 switches but it could be done if the I/O Expander electronics did not work.  