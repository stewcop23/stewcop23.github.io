# Ion Instructions
The massive 659 page manual can be found [here](https://acrobat.adobe.com/link/review?uri=urn:aaid:scds:US:e845d96c-000c-4da3-be38-ac0d52587f6c)
# Timeline
I would recommend watching the (currently non-existant) videos in the order presented below

# Patching

Patching is one of the first things you learn as it is the skeletal structure that keeps your light show together. As you may have learnt, our patch allows us to patch our addresses to channels, as a way of organising the lights. For example address 127 and 234 may be on other sides of the theatre, but the function they perform on stage may be similar so we may patch address 127 to channel 10 and address 234 to channel 11. This makes our lives much easier when we are actually programming this show.

To get started with patching click the plus button in the bottom of the screen and select Patch (Tab 12). You will notice that your screen has turned blue, this means that you are in blind mode. Blind mode is used to edit things like patches, palettes, macros, and effects. To get out of blind mode use the F1 key on your keyboard to go back to Live mode. If you do not have access to your function keys, by clicking on the virtual keyboard in the upper right you can also get back Live mode. Live mode is where we will end up doing the majority of our programming.

Looking now at the main area in our screen, there are several columns, but the three most important ones are the first three: Chan (which stands for channel), address (this will display the address or addresses patched to a particular channel), and type (this will be important later and tells the computer what properties you are allowed to change on a fixture as well as the amount of addresses that need to be patched for that channel).

At this point you should have been given a list of channels and their addresses. To get started with patching, first type the channel you want to patch, you may notice that the software has automatically added “Chan” before the number you have inputted, this is important to notice because whenever you are programming the software automatically assumes you are talking about a channel when you type a number, unless you tell it otherwise. Follow this number with  “a” which as you will show as “Address” , because this Channel is at an Address, followed by the address that that channel should be patched to. In the command line it will look something like this:

![Chan 10 Address 127](/Images/Chan10Addr127.png)

This means that channel 10 will be patched to address 127.

Finally you can select the type of fixture. Click on the type field beside the address of the channel you just patched. “Dimmer” is the default, this is for any conventional style lights that have no additional features. Select the fixture you want using the “Show”, “Manfctr”, or “Search” buttons at the bottom of the screen. “Show” shows you any fixtures that you have used in your current file (useful if you have to change to this fixture type many times), “Manfctr” shows you a list of manufacturers and the fixtures that they have made, and “Search” allows you to search for a specific fixture type.

## Batch patching

Picture
It is possible to patch addresses in batches, this is useful if all of the addresses that you want to patch come sequentially, for example patching many LED fixtures at the same time. Bach patching is very similar to regular patching, but you add more than one channel to the command that you use to patch. For example: Channels 11 through 14 need to be patched into addresses 111 through 114, this can easily be done by typing “11” then the letter “t” gives us “through” allowing us to select a range of channels, then “14” to specify the end of the range, follow this with “a” for “Address” then the first address that you want to patch, in our case “111”. Hitting enter will automatically entre these addresses the way we want them to. If you have set the fixture type before running this command, it will automatically give each channel its required number of addresses before it starts doing the next one. This is because most non-conventional light types require more than one address to function, and the start point of these addresses can be set on the light itself, so these lights can be easily batch patched.

Add Picture
A fully completed patch looks something like this:

# Display

Once you have been given the full show file from Mr. Stusek, it is time to start understanding the software you are working in. In front of you should be the “Live Table” as indicated by the label at the bottom of the window. This window shows you the current status of all of the channels in this show file. Given that we will only be programming lights that we have patched, it is sensible that we would only want those to be visible. To do this, go to the virtual keyboard (in the upper right corner) and hit the button labelled “Flexi” this should change the “Live Table” to “Live Table Patched”, this is how i keep my display most of the time. If you hit the button a few more times, the display will cycle through a few other options before returning to the basic “Live Table”.

Some useful displays are:

“Live Table Patched” → the current state of all of your patched channels

“PSD” → displays all of your recorded cues (more about those in a minute)

“Augment3d” → provides a 3d rendering of the theatre and your lights

## Split screen

It is also possible to split the screen, allowing you to see multiple displays at once, to do this hit the plus button at the bottom of the screen. Now in the upper left corner there are many options, I personally use the “3 Right” setting, with the “PSD” in the long column on the right, “Live Table Patched” in the bottom left corner, and “Augment3d” in the upper left corner, however that is just personal preference, and you can make your setup whatever you want.

# Setting a light

## Intensity

Now it is time to start programming, the most basic thing you can do to a light it turn it on, and doing that is super easy, all you have to do is specify the channel (or range of channels (using “Thru” as before)) followed by the letter “a” which will be replaced by the “@” symbol, as you are setting this Channel At (some brightness). Setting intensity can be a bit strange, if you input a one digit number, it will automatically multiply that number by 10. This is because the maximum intensity of any fixure is 100, so any one digit number is multiplied by 10 to reduce some keystrokes. To enter intensities below 10, preface the number with a zero. As an example of this: just typing “5” will set the intensity at 50(%), but typing “05” will give you 5%.

To set the intensity to full, hit “F” on your keyboard twice (F for Full), you could also just hit “F” once, then hit enter but it is usually faster to hit “F” twice. And to turn the light off hit the “O” key (O for Out), note that you do not need to hit enter for the light to turn off, as hitting O will automatically hit enter for you.

## ML Controls

Any other parameter on a light can be controlled from the “ML Controls” Display (Tab 5). Some other parameters include: colour, focus (where the light is pointed), and beam info. Example: Chan 10 is a channel patched with colour options, typing: “10 [Enter]” ([Enter] as in the enter key on your keyboard) then looking in “ML Controls” will allow you to change the colour by, either clicking on the colour picker or adjusting the RGB values.

# Recording cues

Once you have created something that looks good, it's time to record your first cue. Hitting “R” will put “Record” into the command line, now you will specify the cue number that you want to be recorded, note that the software automatically added the word “Cue” before the number you inputted, much like channels, when recording, the systems assumes you are recording cues, unless you tell it otherwise. Hitting “Enter” will then record the cue. Back in our virtual keyboard, on the left side you will notice a Go button and a stop button, right now, the Go button will not do anything, as Go means that it will Go to the next cue in our list (but we have no cues to go to). If you press the Stop/Back button it will bring you into what is known as “Cue Out”, every time you Go to Cue Out every fixture will move to their home position and turn their intensity off.

When I refer to being “IN” a cue, I mean the cue that is currently in control of the lights. The number of this cue is in the yellow box at the bottom of your PSD List. the number in the grey box next to it is the cue that will be executed when the “Go” button is pressed.

## Times

The time on a cue is how long it takes for the cue to change from the previous cue to this cue, the default is 5 seconds but that may not be what you want. To change the time of a cue:

1. Specify the cue you want to change using “q” (q as in Cue), followed by the number of the cue you would like to change.
1. Hit the “I” key (I for t**I**me) followed by how long you want the cue to take, then hitting enter.
   1. Step 1 can be skipped if you are currently in the cue that you want to change, as the computer assumes that you are talking about the current cue when you hit “I”

## Updating a cue

Now let's say that i had a light turned on in a cue that i didn't want on, fixing this is pretty simple, just make the change you want in the cue that you want to fix, then hit “U” (U for Update).

## fw/hang

“Follows” and “hangs” (abbreviated to F for follow, H for hang are displayed in the fw/hang column of your PSD) refer to the softwares ability to automatically hit the “Go” button in specific timings (1/100th of a second accuracy). Follows and Hangs are similar in that, you specify a follow or a hang time for a specific cue, then, when that cue is executed, once that time has passed the cue executes the next cue. Where they differ is when they start counting, Follows start immediately after the cue is executed, whereas Hangs wait until after the cue’s Time has completely elapsed. This means that if a cue has a time of 0, a follow of 1 and a hang of 1 are one and the same, but if your cue has a time of 1 second, a follow of 1 will execute immediately after the time has elapsed as they are the same length, but a hang will execute 1 second after the cues time has elapsed.

Personally I recommend sticking to Follows for this project as it allows you to keep the time of your cues separate from the timings of your cues (confusing i know). By this I mean that, when using the following, if you want the cue time to be shorter, you can adjust the time without losing the accurate timings between your cues.

### Timing your cues

Herein lies the main challenge of this project: Timing your cues to your music.

## Labels

## home/sneak

# Palettes

## Colour Palettes

### By Type Palettes

## Focus Palettes

## Beam Palettes

## Intensity Palettes

## Presets

# Effects

# Macros

# Magic Sheets

# Fan

# Pixel Maps

# Submasters

## Faders

# An Analysis of One of My Shows
