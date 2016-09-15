## What you need
* Stentura Stenograph device. This was done with a Stentura 400SRT, but it should work with others versions, as long as it is the electric version.
* A cable. There are a few options here:
 + Option 1: The Stenograph realtime cable kit. The one that usually comes with the Stentura comes in three parts. A grey connector, a black connector, and a cable. There's nothing special about this cable, even though they try to pretend there is. So if you don't already have it, don't spend the amounts of money they are charging to get one. Use Option 2 instead.
 + Option 2: Any RS232 (Also called DB9) male to female cross over-cable (Also known as Null Modem). Here are a few options from Amazon:
    - https://www.amazon.com/StarTech-com-RS232-Serial-Female-SCNM9FM2MBK/dp/B00CEMGMMM/
    - https://www.amazon.com/Serial-Modem-Cable-Female-RS232/dp/B0026KE4CM/
    - https://www.amazon.com/C2G-Cables-Go-Female-Adapter/dp/B000067RW2/  (No cable, so very short. Useful to minimize the amount of cords)
    - https://www.amazon.com/CablesOnline-Slimline-Transfer-Adapter-AD-N04M-2/dp/B00HGIRU3O/ (Even shorter)
 + Option 3 (Not really an option): A serial (with Female connection) to USB converter with *built in cross-over*. This is more expensive, but simplifies the amount of cords and connections. Also I'm pretty sure that doesn't actually exist, since you can only get a male connector version of this.

If you intend to connect to a PC serial port directly, or you somehow chose option three above, that's all you need. If you want to connect via USB, then you'll also need the following. If you're not sure if you'll need it, then you probably need it.

* Serial (Female connector) to USB converter. Once again, here are some options:
 + https://www.amazon.com/Sabrent-Serial-RS-232-Converter-CB-DB9P/dp/B00IDSM6BW/
 + https://www.amazon.com/Tera-Grand-Premium-Adapter-Supports/dp/B00BUZ0K68/ (No cable, so very short. Useful to minimize the amount of cords)

**It's important that there is a cross-over cable at some point of the connection, and only one. The Stenograph cable has one built in.**

The terms "RS232" and "DB9" mean the same thing and can be used interchangeably. The same goes for "Cross-over" and "Null Modem"

## Putting it all together
Connecting all the pieces together is pretty straight forward. You can either connect directly to the PC's serial port (if it has one), or you can use the serial to USB converter. The RS232 cable will connect to the back of the Stenograph, and the other end to the USB connetor (or directly to the PC).

## Connecting to Plover
First, turn on the Stenograph. The green light should turn on, and the red light is usually off. If it's blinking, or the green and red are blinking back and forth, don't worry, it'll still work. If you want to stop the blinking, there are some instructions later.

Next, we can connect Plover to use the device. In Plover, click Configure. Select Stentura as the Stenotype machine. Click Configure.

Click the scan button, next to Port. This will refresh the Port list. You'll need to find the correct port number. If there is only one, it's probably the one you want. If there is more that one, you can try a few until you find the one that works the. If you're using a USB device, it's likely to be the larger number. If you're connecting to the serial port directly, it'll probably be the first one.

The other settings should stay at the defaults. Which are 9600, 8, N, 1, no flow control.

Press OK to get out of the Configure menu, until you get back to the main Plover screen. Click the refresh button, and it should say Stentura: connected. If not, then something went wrong, double check all the steps above.

That's it. You should get output when typing.

## Stop the blinking
The lights blink when the internal memory is full, or if the battery is drained, or both.
if the green light is blinking, then the battery is drained. To charge, leave it plugged in and *turned on*. A good battery will charge in about 8 hours. It's possible that the battery is dead. If you bought the unit second hand and a few years old, then it's very likely to be dead. If that's the case, the light will never stop blinking, no matter how much you try charging it. If you remove the battery, the light will stop blinking and will continue to work with the power cable. The dead battery is useless anyway, so throw it away and now your unit is lighter. (Or buy a new one http://www.stenoworks.com/writer-accessories/writer-batteries/ )

If the red light is blinking, then the internal memory is full or close to full. To clear it:
* turn the Stenograph off
* while holding STK, turn the machine become on.
* the lights should be both blinking back and forth. If not, try again from the start.
* press KWR to clear the memory, or TPH if you change your mind.

The memory will get full reguarly so you'll have to do this occasionally. So remember it!

## Manual
Valentin from the [Plover Forums](https://groups.google.com/d/msg/ploversteno/dhLSXsPdGYY/jZQlVdcIAQAJ) has kindly scanned the entire manual. It is very useful to read, and you can get it [here](https://0au.de/~apo/stentura_200_400_srt_manual.pdf).