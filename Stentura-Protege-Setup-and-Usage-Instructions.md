Congratulations on getting a Stentura Protege. This page will show you how to connect it to your computer and setup Plover. 

[Photo of my Protege. Note: Mine did not come with the removable name plate.](https://imgur.com/vKbiTOJ)

## What you need

You will need two cables:

1. **Data Cable:** 
USB to RS-232 DB9 Male Serial Cable. (Make sure the cord has a male serial with 9 pins)
- [Amazon link](http://a.co/9KWXIMP)
2. **Power Cable:**
USB 2.0 Cable - A-Male to B-Male. (The Stentura Protege can be powered either by USB or by a proprietary A/C charger. Your machine may come with a power chord. Mine did not.)
- [Amazon link](http://a.co/fQDbqWD)

Note: Both of those Amazon links are for 6 foot cables. Make sure you get a cord long enough for your setup.

**Why can't we just use the USB to transfer data?**
Ideally, the USB cable could carry both power and data, but this is not possible because modern drivers are not available for the Protege and the USB link was only designed to work with Stentura software. Using a Serial-to-USB cable solves this problem. This cable carries the data and the cable has drivers that work with modern computers and Plover. So it really doesn't matter that Stentura no longer supports the Protege. 

## Setup

**Step 1.** 
Connect power cord: Connect USB A-to-B cable to Stentura machine and computer. Your machine now has power. On the front of your Stentura is a row of 6 grey buttons. Press and hold the 1st one to turn it on. 

**Step 2.**
Connect data cord: Connect serial-to-USB cable to Stentura machine and computer. 

[Photo of both cables connected.](https://imgur.com/wGc9y4p)

**Step 3.** 
Download the latest version of Plover for your OS.

**Step 4.**
Open Plover. Click the configure button. A new configuration window will open. Click the tab for machine. Select Stentura from the drop down menu. Go back to the window where you clicked the configure button. Click the radio button "enable" to enable output. Click the reload button (arrows going in a circle) until the dot turns green and it says "Stentura: Connected"

**Step 5.**
Thanks to Plover, your Stentura can now type on your computer. Start learning Steno with Plover [lessons](https://sites.google.com/site/learnplover/lesson-1-fingers-and-keys) and [interactive drills](http://stenoknight.com/plover/haxeploverlearn/). 

## Something went wrong

I ran into a problem because I was using an older Serial-to-USB cable and Windows was not able to load the correct Prolific drivers for the cable. I found a solution. [This site](http://www.totalcardiagnostics.com/support/Knowledgebase/Article/View/92/20/prolific-usb-to-serial-fix-official-solution-to-code-10-error) explains the problem and gives you a link to download the right drivers. 

## Stentura Protege Manual

[Link to user guide PDF](https://www.stenograph.com/content/files/documents/Stentura%20Protege%20User%20Guide.pdf)

## Stop The Beeping

My Stentura Protege did not come with a battery. As long as it has power it runs just fine, but it makes an annoying little beep every minute. This is the low battery beep and it beeps even if you have no battery connected. I searched through the manual and did not see a way to disable this. But, I discovered two approaches to remove the beeping. I will explain how below. I was successful but please try this at your own risk.

**What is making the beep?** The beep is made by a small little speaker called a Piezo Electric Buzzer (cylinder with hole in it and plus sign). It is soldered to the circuit board and labeled "Alarm." (If you are curious, you can learn more about how these work in this [video](https://www.youtube.com/watch?v=77h1JhD9Syw).)

**Opening up the machine** To see this beeping speaker you have to turn the machine over. Then, remove some screws. There are two sets of different sized screws. Make sure you keep track of which screws go where. (Hint: The smaller screws go with the metal washers. [Photo.](https://imgur.com/P0RR4dy)) Take the back cover off carefully because the battery wires are still attached to the case. [Photo.](https://imgur.com/kTWBKbM) Locate the beeping speaker. It is labeled Alarm on the circuit board. [Photo.](https://imgur.com/4kgY1kC) 
 
**Option 1**: Mute the speaker by putting a small bit of tape over the hole next to the plus sign shown in this [photo.](https://imgur.com/4kgY1kC) I used masking tape, but you might want to try experimenting with other types of tapes. This will lower the volume a lot and is non-destructive. 

**Option 2**: Permanently remove the ability of your stenograph to make sounds. This will destructively remove all capabilities of your machine to make beeping sounds. Make sure you really want to go in this direction before moving forward. If you plan on using this machine with a battery, the low battery beep could be useful. I plan on only using it plugged in and I don't plan on getting a battery. I successfully completed this modification, but please do this at your own risk. 

The speaker, a Piezo Electric Buzzer makes sound by vibrating a ceramic plate. This can be carefully broken. I used a screw. [Photo.](https://imgur.com/a/BRrsZ) Place it into the hole and gently twist. [Photo.](https://imgur.com/a/mQI5H) You can plug in the machine again to test if you have successfully disabled the speaker. If you no longer hear the chirp then you have been successful.  

Alt option: I did not do this, but it should be possible to desolder the Piezo Electric Buzzer from the board. Since I have not done this I can not confirm that this would be without side effects.
