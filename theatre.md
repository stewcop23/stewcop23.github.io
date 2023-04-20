# Ion Instructions
The massive 659 page manual can be found [here](https://acrobat.adobe.com/link/review?uri=urn:aaid:scds:US:e845d96c-000c-4da3-be38-ac0d52587f6c)
# Timeline
I would Recomend witching the videos in the order presented below

## Patching
Patching is one of the first things you learn as it is the skeletal structure that keeps your light show together. As you may have learnt, our patch allows us to patch our addresses to channels, as a way of organising the lights. For example address 127 and 234 may be on other sides of the theatre, but the function they perform on stage may be similar so we may patch address 127 to channel 10 and address 234 to channel 11. This makes our lives much easier when we are actually programming this show.

To get started with patching click the plus button in the bottom of the screen and select Patch (Tab 12). You will notice that your screen has turned blue, this means that you are in blind mode. Blind mode is used to edit things like patches, palettes, macros, and effects. To get out of blind mode use the F1 key on your keyboard to go back to Live mode. If you do not have access to your function keys, by clicking on the virtual keyboard in the upper right you can also get back Live mode. Live mode is where we will end up doing the majority of our programming.

Looking now at the main area in our screen, there are several columns, but the three most important are the first three: Chan (which stands for channel), address (this will display the address or addresses patched to a particular channel), and type (this will be important later and tells the computer what properties you are allowed to change on a fixture).

At this point you should have been given a list of channels and their addresses. To get started with patching, first type the channel you want to patch, you may notice that the software has automatically added “Chan” before the number you have inputted, this is important to notice because whenever you are programming the software automatically assumes you are talking about a channel when you type a number, unless you tell it otherwise. Follow this number with  “a” which as you will show as “Address” , because this Channel is at an Address, followed by the address that that channel should be patched to. In the command line it will look something like this:

This means that channel 10 will be patched to address 127.

Finally you can select the type of fixture. Click on the type field beside the address of the channel you just patched. “Dimmer” is the default, this is for any conventional style lights that have no additional features. Select the fixture you want using the “Show”, “Manfctr”, or “Search” buttons at the bottom of the screen. “Show” shows you any fixtures that you have used in your current file (useful if you have to change to this fixture type many times), “Manfctr” shows you a list of manufacturers and the fixtures that they have made, and “Search” allows you to search for a specific fixture type.

### Batch patching
It is possible to patch addresses in batches, this is useful if all of the addresses that you want to patch come sequentially, for example patching many LED fixtures at the same time. Bach patching is very similar to regular patching, but you add more than one channel to the command that you use to patch. For example: Channels 11 through 14 need to be patched into addresses 111 through 114, this can easily be done by typing “11” then the letter “t” gives us “through” allowing us to select a range of channels, then “14” to specify the end of the range, follow this with “a” for “Address” then the first address that you want to patch, in our case “111”. Hitting enter will automatically entre these addresses the way we want them to. If you have set the fixture type before running this command, it will automatically give each channel its required number of addresses before it starts doing the next one. This is because most non-conventional light types require more than one address to function, and the start point of these addresses can be set on the light itself, so these lights can be easily batch patched.

A fully completed patch looks something like this:

## Display
Once you have been given the full show file from Mr. Stusek, it is time to start understanding the software you are working in. In front of you should be the “Live Table” as indicated by the label at the bottom of the window. This window shows you the current status of all of the channels in this show file. Given that we will only be programming lights that we have patched, it is sensible that we would only want those to be visible. To do this, go to the virtual keyboard (in the upper right corner) and hit the button labelled “Flexi” this should change the “Live Table” to “Live Table Patched”, this is how i keep my display most of the time. If you hit the button a few more times, the display will cycle through a few other options before returning to the basic “Live Table”. 

Some useful displays are:

“Live Table Patched” → the current state of all of your patched channels

“PSD” → displays all of your recorded cues (more about those in a minute)

“Augment3d” → provides a 3d rendering of the theatre and your lights

### Split screen
It is also possible to split the screen, allowing you to see multiple displays at once, to do this hit the plus button at the bottom of the screen. Now in the upper left corner there are many options, I personally use the “3 Right” setting, with the “PSD” in the long column on the right, “Live Table Patched” in the bottom left corner, and “Augment3d” in the upper left corner, however that is just personal preference, and you can make your setup whatever you want.
## Setting a light

### Intensity
Now it is time to start programming, the most basic thing you can do to a light it turn it on, and doing that is super easy, all you have to do is specify the channel (or range of channels (using “Thru” as before)) followed by the letter “a” which will be replaced by the “@” symbol, as you are setting this Channel At (some brightness). Setting intensity can be a bit strange, if you input a one digit number, it will automatically multiply that number by 10. This is because the maximum intensity of any fixure is 100, so any one digit number is multiplied by 10 to reduce some keystrokes. To enter intensities below 10, preface the number with a zero. As an example of this: just typing “5” will set the intensity at 50(%), but typing “05” will give you 5%. 

### ML Controls
Any other parameter on a light can be controlled from the “ML Controls” Display (Tab 5). Some other parameters include: colour, focus (where the light is pointed), and beam info. Example: Chan 10 is a channel patched with colour options, typing: “10 [Enter]” ([Enter] as in the enter key on your keyboard) then looking in “ML Controls” will allow you to change the colour by, either clicking on the colour picker or adjusting the RGB values.
## Recording cues

### Updating a cue

### fw/hang
### Timing your cues

### Labels

### home/sneak

## Palettes

### Color

### Focus

### Beam

### Intensity

### Presets

## Macros

## Effects

## Link / loop
## Magic Sheets

## Fan

## Pixel Maps

## Submasters

### Faders



