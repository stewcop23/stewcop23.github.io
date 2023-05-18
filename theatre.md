# Ion Instructions
The massive 659 page manual can be found [here](https://acrobat.adobe.com/link/review?uri=urn:aaid:scds:US:e845d96c-000c-4da3-be38-ac0d52587f6c)
## Timeline
I would recommend watching the videos in the order presented below:
* [Patching](https://youtu.be/6R9d4xmNLew)
* [Displays](https://youtu.be/9_Egeesk_G4)
* [Turning on a Light](https://youtu.be/_aXignbm9_s)
* Grouping
* [Cues](https://youtu.be/9eeFnZ-CT_4)
* Timing Your Cues
* [Palettes](https://youtu.be/-H3i9fWpOjg)
* Effects
* Magic Sheets
* Fan
* A Brief Look at My Shows

# Patching
Patching is one of the first things you learn as it is the skeletal structure that keeps your light show together. As you may have learnt, our patch allows us to map addresses to channels, as a way of organising the lights. For example addresses 127 and 234 may be on other sides of the theatre, but the function they perform on stage may be similar so we may patch address 127 to channel 10 and address 234 to channel 11. This makes our lives much easier when we are actually programming this show, as we no longer need to turn every light on and off to see where it is.

To get started with patching click the plus button in the bottom of the screen and select Patch (Tab 12).

You will notice that your screen has turned blue, this means that you are in blind mode. Blind mode is used to edit things like patches, palettes, macros, and effects. To get out of blind mode use the F1 key on your keyboard to go back to Live mode. If you do not have access to your function keys, click on the virtual keyboard in the upper right and you can also get back Live mode. Live mode is where we will end up doing the majority of our programming, but we will stay in blind mode to complete our Patch.

Looking now at the main area in our screen, there are several columns, but the three most important ones are the first three: Chan (which stands for channel), address (this will display the address or addresses patched to a particular channel), and type (this will be important later and tells the computer what properties you are allowed to change on a fixture as well as the amount of addresses that need to be patched for that channel).

At this point you should have been given a list of channels and their addresses. To get started with patching, first type the channel you want to patch, you may notice that the software has automatically added “Chan” before the number you have inputted, this is important to notice because whenever you are programming the software automatically assumes you are talking about a channel when you type a number, unless you tell it otherwise. 

If, instead of ‘Chan’ it says ‘Address’ you are in the wrong Format. To change to the correct Format, either use the shortcut “F4” or find the “Format” button on the virtual Keyboard (far right middle, bottom left button)

Follow the Channel number with  “a” which as you will show as “Address”, followed by the address that the channel should be patched to. In the command line it will look something like this:

![Chan 10 Address 127](/Images/Chan10Addr127.png)

This means that channel 10 will be patched to address 127.

Finally you can select the type of fixture. Click on the type field beside the address of the channel you just patched. “Dimmer” is the default, this is for any conventional style lights that have no additional features. Select the fixture you want using the “Show”, “Manfctr”, or “Search” buttons at the bottom of the screen. “Show” shows you any fixtures that you have used in your current file (useful if you have to change to this fixture type many times), “Manfctr” shows you a list of manufacturers and the fixtures that they have made, and “Search” allows you to search for a specific fixture type.

If you make an error while patching, it is easy to fix. Select the channels you want to fix by typing the channel number, Then in the bottom right corner hit the “Unpatch” button, then enter. This “unpatch” button is one of what is known as “Soft keys”. If you keep watching this bottom corner, you will notice that these buttons change as you do various things.

## Batch patching
It is also possible to patch addresses in batches, this is useful if all of the addresses that you plan on patching come sequentially, for example patching many LED fixtures at the same time. Bach patching is very similar to regular patching, but you add more than one channel to the command that you use to patch. 

If you have set the fixture type before running this command, it will automatically give each channel its required number of addresses before it starts doing the next one. This is because many non-conventional light types require more than one address to function, and the start point of these addresses can be set on the light itself, so these lights can be easily batch patched.

For example: Channels 11 through 14 have the type “ColorSource Deep Blue” This can easily be done by typing “11” then the letter “t” gives us “through” allowing us to select a range of channels, then “14” to specify the end of the range. If the channels you want to patch are not in order, you can combine multiple channels by hitting “=”, it's weird, but it will show as a “+” and then you can add another channel. Then as before, press enter to select the channels then left click on the type column. I am going to go to the manufacturer tab, go to “ETC Fixtures”, then select “	ColorSource SPOT DB”, then the 5 address variant.

Because each of these channels takes 5 addresses, for the sake of an example we want these channels to be patched into addresses 200 through 219.

Select your channels as before, then hit “a” for “Address”, as before, then type the first address that you want to patch, in our case “200”. Hitting enter will automatically patch these addresses the way we want them to. 


A fully completed patch looks something like this:
# Display
Once you have been given the full show file from Mr. Stusek, it is time to start understanding the software you are working in. In front of you should be the “Live Table” as indicated by the label at the bottom of the window. This window shows you the current status of all of the channels in this show file. Given that we will only be programming lights that we have patched, it is sensible that we would only want those to be visible. To do this, go to the virtual keyboard (in the upper right corner) and hit the button labelled “Flexi” this should change the “Live Table” to “Live Table Patched”, this is how I keep my display most of the time. If you hit the button a few more times, the display will cycle through a few other options before returning to the basic “Live Table”. 

If you want to add more displays to your current window, hit the plus button at the bottom of the screen to bring up the list of displays you can choose from.

Some displays I would recommend are:

“Live Table Patched” → the current state of all of your patched channels

“PSD” → displays all of your recorded cues (more about those in a minute)

“Augment3d” → provides a 3d rendering of the theatre and your lights

## Split screen
It is also possible to split the screen, allowing you to see multiple displays at once, to do this hit the plus button at the bottom of the screen. Now in the upper left corner there are many split screen options, I personally use the “3 Right” setting, with the “PSD” in the long column on the right, “Live Table Patched” in the bottom left corner, and “Augment3d” in the upper left corner, however that is just personal preference, and you can make your setup whatever you want.
# Setting a light

## Intensity
Now it is time to start programming, the most basic thing you can do to a light it turn it on, and doing that is super easy, all you have to do is specify the channel (or range of channels, using “Thru” or “+” as before) followed by the letter “a” which will be replaced by the “@” symbol, as you are setting this Channel At (some brightness). Setting intensity can be a bit strange, if you input a one digit number, it will automatically multiply that number by 10. This helps remove tedious keystrokes when programming. To enter intensities below 10, preface the number with a zero. As an example of this: just typing “5” will set the intensity at 50(%), but typing “05” will give you 5%. 

To set the intensity to full (equivalent to 100%),type the channel number, then hit “F” on your keyboard twice (F for Full), you could also just hit “F” once, then hit enter but it is usually faster to hit “F” twice. And to take a light Out (i.e.: turn the light off) , type the channel number, then hit the “O” key (O for Out), note that you do not need to hit enter for the light to turn off, as hitting O will automatically hit enter for you.

## ML Controls
Any other parameter on a light can be controlled from the “ML Controls” Display (Tab 5). Some other parameters include: colour, focus (where the light is pointed), and beam info. Example: Chan 10 is a channel patched with colour options, typing: “10 [Enter]” ([Enter] as in the enter key on your keyboard) then looking in “ML Controls” will allow you to change the colour by, either clicking on the colour picker or adjusting the RGB values.

## Fan
Fan is an advanced feature that allows you to smoothly spread a parameter across many fixtures.

To do a simple fan, all you need to do is specify more that one of a specific parameter, something like: “10 Thru 14 @ Full Thru Out” this will fan the intensity across these channels.

This can also be done with palettes: “10 Thru 14 a Color Palette 1 + 2” 

In this example channel 10 will be entirely in colorpalette 1, and chan 14 will entirely be in color palette 2.

Notice the difference between “Thru” and “+”, Intensity will only allow Thru, but when using palettes the difference is very important. If you use “+” the software will fade between the two palettes that you have specified., but if you use “Thru” it will fade between those palettes, but numerically, so “10 Thru 14 @ Color Palette 1 + 5”, will fan through color palette 1 and 5, but “10 Thru 14 @ Color Palette 1 Thru 5” will fan through 1 and 5, but also will pass through 2, 3 and 4, so you may perceive some unintended patterns.

Fans can also be made more advanced by, after typing one of the previous commands, hitting the “Fan” Soft-Key, you will notice the Soft-Keys change again. These new options are different patterns that the fan could be, I recommend you try some of these out.

# Grouping
It is possible to group many different channels into, well, Groups. As you may have noticed I've been typing “10 Thru 14” an awful lot, and grouping these channels together would allow me to shorten the required number of keystrokes to select those channels.

Creating groups is really easy:

1. Specify the channels you want to add to the group
   1. In our case “10 thru 14”
1. Then ‘R’ followed by ‘G’ (will show as Record Group)
1. Then specify the group number
   1. I’ll use group 10 as an example. (this is because when grouping, usually the group number is the lowest Channel number in the group)
1. Hit enter

Now that group can be used exactly the same as Channel or range of Channels, however you do need to specify that you are talking about a group by using ‘G’. 

As an example, to take all of Group 10 Out, you can input this:

“G 10 O”

This selects group 10, then sets all of their intensities out.

# Recording cues
Recording cues is how we can save what is on stage and play that back at a later date, so for this example we are going to just turn some lights on, when programming your actual show, this will be what you want it to look like on a specific beat.

Once you have created something that looks good, it's time to record your first cue. Hitting “R” will put “Record” into the command line, now you will specify the cue number that you want to be recorded, note that the software automatically added the word “Cue” before the number you inputted, much like channels, when recording, the systems assumes you are recording cues, unless you tell it otherwise. Hitting “Enter” will then record the cue. Back in our virtual keyboard, on the left side you will notice a Go button (triangle pointing right) and a stop/back button (triangle pointing left), Go means that it will Go to the next cue in our list (but we have no cues to go to). If you press the Stop/Back button it will bring you into what is known as “Cue Out”, every time you Go to Cue Out every fixture will move to their home position and turn their intensity off. 

The space bar can be used instead of the virtual keyboard to travel through cues. If you press ‘Alt +G’ you will see “Spacebar Go Enable” this means that, now pressing Space is equivalent to pressing Go, pressing ‘ctrl + space’ is the same as pressing the Stop/Back button, when you do this for the first time on a new installation, it will ask you 

When I refer to being “IN” a cue, I mean the cue that is currently in control of the lights. The number of this cue is in the yellow box at the bottom of your PSD List. The number in the grey box next to it is the cue that will be executed when the “Go” button is pressed.


## Times
The time on a cue is how long it takes for the cue to change from the previous cue to this cue, the default is 5 seconds but that may not be what you want. To change the time of a cue:

1. Specify the cue you want to change using “q” (q as in Cue), followed by the number of the cue you would like to change.
1. Hit the “I” key (I for t**I**me) followed by how long you want the cue to take, then hitting enter.
   1. Step 1 can be skipped if you are currently in the cue that you want to change, as the computer assumes that you are talking about the current cue when you hit “I”

## Updating a cue
Now let's say that i had a light turned on in a cue that i didn't want on, fixing this is pretty simple, just make the change you want in the cue that you want to fix, then hit “U” (U for Update). There are a few modifiers that can be applied to this, but we won't change anything for now. Keep in mind that any changes will be tracked forward, so if you turn on a new channel, that channel will stay on as you go into the next cue. This can be avoided by using the “Q Only” key when updating. This will ensure that, this “Q Only” (cue only), will be updated, and and changes will not be 
## fw/hang
“Follows” and “hangs” (abbreviated to F for follow, H for hang are displayed in the fw/hang column of your PSD) refer to the softwares ability to automatically hit the “Go” button in specific timings (up to 1/100th of a second accuracy). Follows and Hangs are similar in that, you specify a follow or a hang time for a specific cue, then, when that cue is executed, once that time has passed the cue executes the next cue. Where they differ is when they start counting, Follows start immediately after the cue is executed, whereas Hangs wait until after the cue’s Time has completely elapsed. This means that if a cue has a time of 0, a follow of 1 and a hang of 1 are one and the same, but if your cue has a time of 1 second, a follow of 1 will execute immediately after the time has elapsed as they are the same length, but a hang will execute 1 second after the cues time has elapsed.

Personally I recommend sticking to Follows for this project as it allows you to keep the time of your cues separate from the timings of your cues (confusing i know). By this I mean that, when using follows, if you want the cue time to be shorter, you can adjust the time without losing the accurate timings between your cues.

To set a Follow/Hang:

1. Specify the cue you want to change using “q” (q as in Cue), followed by the number of the cue you would like to change.
1. Either press the Soft-Key “Fw/Hang” or use the shortcut ‘Alt +2’ (this presses the second Soft-Key)
   1. Due to the nature of the Fw/Hang button being a Soft-Key, you need to specify the cue that you want to apply the fw/hang to. Although, just hitting ‘q’ will show the fw/hang Soft-key, and if you press that without specifying a cue, it will assume the current cue.
   1. It is also possible to set the fw/hang (as well as other cue parameters) by, first being in the cue you want to change (to avoid selecting multiple cues), then clicking on the fw/hang space, then entering the time you want.

## Labels

Labels are very useful when you are going back and trying to figure out what the follow of a cue is.

Setting a label is easy, and very similar to setting the time of a cue:

1. Specify the cue you want to change using “q” (q as in Cue), followed by the number of the cue you would like to change.
1. Hit the “L” key (I for Label) followed by what you want the label to be (usually a lyric ), then hitting enter.
   1. Step 1 can be skipped if you are currently in the cue that you want to change, as the computer assumes that you are talking about the current cue when you hit “L”

## Home/Sneak

Home and sneak are two useful functions that help when you want ro reset a fixture. Home sets all non-intensity values to their home values (the same as if you did “Go To Cue Out”).

Sneak is a little bit different. If you are in a recorded cue, you may notice that the values of some recorded channels have changed color. These colors show you how that light is changing in this cue.

- Gray Default or the value is a null value
- Bright Red Manual Data (any data that has been set but not yet stored to an active cue or submaster) When manual channels are used, there will be an advisory that says "Manual Channels" in red in the upper left hand corner of any Live display.
- Blue The intensity value is higher than in the previous cue.Non-intensity parameters (NPs) are in blue when any move instruction has occurred. Unmarked. 
- Green The intensity value is lower than in the previous cue. Also used in reference marking to indicate a channel is marked.
- Magenta Value is unchanged from the previous cue (tracked).
- White The value is blocked.

Sneak resets the fixture to whatever was there before you put that channel into manual control (ie:before you made it red). This is a bit complicated to explain, but by this I mean, if you were in cue 5 and changed channel 10 from Out to 50%, you will notice that the intensity of the light, in the Live Table, has changed to red, this means that the light is currently under “Manual Control”, this means that the number is not what has been recorded in this cue. If you were to enter “Chan 10 Sneak” (Shortcut is “N” for S**N**eak), then Chan 10 would go back to being Out.

# Timing your cues

Herein lies the main challenge of this project: Timing your cues to your music. This is the most tedious and time consuming thing you will have to do to complete this project.

There are many ways you can time your cues, but the method I will show you has worked well for me, so hopefully it will work well for you too. 

Start by downloading and installing audacity, other softwares may work, but I've found that audacity works well for this process. Now import your song into audacity. Then, work your way through the song, adding “Labels” where you want the cues to be executed (ie: ignoring the cue time, what would want to be your follow time), using the shortcut “ctrl + b”. To make this process easier, I would recommend switching the track display of your song to “Waveform” or “multi-view”,as this makes it easier to visually see where you should be placing these labels.

Once you have labelled everything, by selecting between two labels (the selection tool should snap to the labels), then looking at the bottom of our screen we can see the ‘Start and End Time’ of our selection, this can be changed to ‘Start and Length of Selection’ using the little gear icon, at which point the ‘Length of Selection’ can be inputted as the Follow time of the first cue (chronologically, not in the order selected). I would suggest that, once you have added the following time to the cue, change the text of the audacity Label for that cue, as it will make it easier to read when you are polishing your show.

When going back through you song and seeing if your cues line up with the music, ideally you would play the file that will get played when presenting you show NOT the one from inside audacity (I have had issues with audacity causing delay and messing up my cue times)

# Palettes
Palettes are a useful way of storing information about a specific fixture or a type of fixture, functioning similarly to variables in modern coding languages, allowing them to be accessed and changed as needed, with any reference to them being updated automatically. There are many different kinds of palette, but given that they all function in the same manner, I will only explain how to use Color Palettes.

## Color Palettes
To use color palettes: First, set some lights that are able to change color to some colors that you like. Then, as if we were going to record a cue, hit ‘r’, but remember how the software assumes that you are talking about cues? Well, we now need to specify that we are talking about color palettes. To do this either: a) use the shortcut ‘Alt + C’ (or ‘Option + C’ for mac users) or b) select ‘Color Palette’ from the Virtual Keyboard. Finally specify a number to record the Color Palette into. And, much like cues, Palettes can be given labels (I would highly recommend doing this) this greatly increases the chance that you will remember what this palette looks like, and thus be able to use it again.

Like cues, color palettes can be updated, you just need to specify the color palette that you want to update when updating. Keep in mind that this will update all channels, unless you specify specific channels

Update All Channels (Keyboard entry):

“U Alt+C {Color Palette Number} enter”

Update specific Channel (Keyboard entry):

“U {Channel Number or range} Alt+C {Color Palette Number} enter”

### By Type Palettes

“By Type” is a Soft-key that can be pressed when recording a Palette (before you have hit enter). When activated, only one fixture of each fixture type needs to be recorded, because when this palette is used later, all fixtures of that type will replay the information of that one fixture that you recorded earlier.

## Focus Palettes

Like Color Palettes, but stores information about where the light is pointed.

Shortcut is ‘Alt + F‘

I would highly recommend using these if you plan on using any moving lights, because every year the lights aren't pointing where they should and someone has to go home and re-edit their lights to point in the right direction. If you use focus palettes, then you won't have to go through every cue, you will just need to update the FP once and it will automatically propagate to all of your cues.

## Intensity Palettes

Like Color Palettes, but stores information about the brightness of a fixture.

Shortcut is ‘Alt + I‘
## Beam Palettes
Like Color Palettes, but stores anything that isn't Colour, Focus, or Intensity

Shortcut is ‘Alt + B‘

## Presets
While similar, Presets are a bit more than palettes. Presets store all information about a fixture, it is also possible to reference a palette from within a preset.

Shortcut is ‘Alt + P‘

# Effects
THIS SECTION WILL NEED LOTS OF VIDEO EXAMPLES THAT ARE HARD TO SCRIPT.

Effects are a way of making fixtures or groups of fixtures make continuous changes without changing cues. There are several types of effects, the simplest way to use effects is to use some of the pre-built effects that come bundled with the software.

There are several types of effects:

- Step Based
- Absolute
- Focus
- Linear
- Color

To open the effects display, click the plus button, then Effects. From here you can see a list of all of the pre-built effects. By typing a number then hitting enter you can either view the effect with that number (if it exists), or it will create a new effect with that number.  

When looking at an Effect, all relevant information is displayed at the bottom of the screen. On the left side is the effect itself, (ie: how does the output change over time), and on the right is various parameters of the effect. ‘Parameters’ are the parameters of the fixture with this effect that will be affected. Scale sets the maximum and minimum of this function’s parameters (eg: if the scale is 25, and the parameter is intensity, the Effect can only increase or decrease the intensity of the fixture by 25). Cycle Time is how long it takes for what is on the left side to repeat. Duration sets how long the effect runs for, this can be in seconds or a specific number of cycles.

## Focus, Linear, and Color Effects
All of the prebuilt effects are either Focus, Linear or Color. All three of these types work by defining some curve that indicates how the variables will change over time. If the effect only targets one parameter, one of the axes will be the time axis, if there are two or more parameters, then the output will follow the drawn curve, in the direction of the arrow, as time passes.

## Step Based Effects
Unlike Linear effects, which run based off of curves, step based effects run off of, well, steps. Step Based Effects only affect channels that have been inputted into the “Channels” column. The easiest way to understand steps is to think of it like a mini-cue. With Step time being the follow time, and In Time being the cue time, and Channels being the affected Channels. To be more precise, In time is the time it takes to go from the Previous Step’s Off State to the On State of this Step. Dwell time is the amount of time that the Step will wait at the On State. Decay time is the time to go from On state to Off state. And Step time is the time to go from the beginning of this Step’s In Time to the beginning of the next Step’s In Time.

To create more Steps use the Soft-Key “Step” then input “1 through {however many steps you need}”, it will ask you to confirm, and then it will create those Steps.
## Absolute Effects
Absolute effects are similar to step based effects, but there are three main differences, the first is that they run on actions instead of steps, the second is that Absolute Effects can be applied to any Channel that has the required parameters, and finally, there is no On State and Off State, but rather a Level, and this level can be either a number (an intensity), Bkgrd (as if this effect was never applied), or any other palette. 

Actions, unlike Steps, only have Step Time, Time, and Dwell. This means that compared to Step Based Effects, when it comes to timing, you are missing that Decay, this means that sometimes programming an Absolute Effects can be a bit more tedious, as it takes one action to turn the light on, and one action to turn it off, as opposed to step based effects, were you can turn it on and off in one Step. This increase in tediousness comes with an increase in customizability though, as the level can be set to anything, including Palettes.

Absolute Effects are useful if you aren't sure which channels you want to be in an effect and want to be able to easily change it later.

The step time will automatically be the sum of Time and Dwell by default, although you can set it to a custom value.

# Tips and Tricks
You can create labels, fw/hangs, and cue times, while recording said cue (Labels have to go last if are using multiple)

Anything that can be edited in blind (Palettes, presets, effects, etc.) can be opened by pressing their shortcut twice in a row.

Anything (except for channels which would need to be unpatched), can be deleted by pressing the delete key on your keyboard (i believe it’s ctrl+delete for mac) followed by what you want to delete.
# Magic Sheets
Magic Sheets are a great way to organise your show file, and can greatly increase your productivity within this software. The basic idea behind a Magic Sheet is that you can arrange objects that allow you to access Channels, Groups, Color Palettes, etc. at the click of a button.

To get started, navigate to the “Magic Sheet” display, importantly, NOT the “Magic Sheet List” display. From here, click on the plus button labelled “New Magic Sheet”. This will create a new magic sheet and move you into blind mode. When in blind mode on a magic sheet, you can move objects around as well as edit their properties, when in live mode, you can click on the objects to select their objects target, this may sound intimidating right now, but i will explain in a minute.

The large black space with a grid of dots that takes up the majority of this screen is the Magic Sheet itself, this is where you will be placing your objects. On the right at the top is where you can access all of the objects you can place.The first 9 options are buttons for Channels, Groups, Palettes, and Macros. To use these, click on the one you want to place, then click on the Magic Sheet where you want to place it. The lower section is where you can edit the properties of the currently selected object. Let's start with a Channel, Click the channel button over on the right, then click on the Sheet. To move an object after it has been placed, first select the object then drag it to where it should go. Right now this Button is targeting Channel 1, to see this we can look over at the lower section on the right and see that under the “Target:” section, it is targeting a channel, and that target is channel 1. I'm going to change this number to 10, then switch back to Live Mode. Now you can see that if I click on this button, my command line will have “Chan 10” added to it.

To easily get back into editing your Magic Sheet, click on the little arrow on the right.


Sometimes individually adding Channels or Palettes can get really tedious. To speed it up, above the different objects you can place there are 4 menus to help speed up your workflow. 

The leftmost menu allows you to change how the cursor places objects. There are three different modes.

1. Normal
1. Quick Place
   1. Quick Place mode allows you to quickly place many objects of the same type, and accurately set their targets. To get started, click the cursor labelled “Quick Place” then set the target type right below that, then set the target starting number, and the increment. The increment is how much the target will increment each time you place an object.
   1. As an example, let's say we wanted to place channels 10 through 14 in a row. Now you could click one by one back and forth but that can be slow, especially when you are adding more than just five channels. Turn on Quick Place, set the target type to Channel, then set the Start to 10, and the increment to 1. From here, click on the channel button on the right. You should now notice that a red Done button has appeared in the bottom right corner of the Sheet. Now you can click wherever you want these channels to be placed, and as you click you can see that the number is being automatically incremented with each subsequent channel that gets placed. After we have placed all of the objects that we want to, we just need to hit the red Done button in the bottom right corner.
1. Quick Target
   1. Quick Target works similarly to QuickPlace, but instead of placing new tiles, it changes the targets of existing tiles. Other than that the functionality is identical

The menu second from the left gives you some zoom options. The third menu contains the arrangement options. Although i will specifically mention the “Create Array…” option. This will, somewhat predictably, create an array of whatever object you have selected when you click the “Create Array…” button, to the dimensions that you have specified. 

These are the fundamentals of magic sheets, I would encourage you to explore them on your own, as there is so much more that I don't have time to explain here.


# A Brief Look at My Shows
Things to look for:

- Color Palettes
- Labelling
- Magic Sheets
- Use of Effects


[Hayloft II](/Show_Files/Hayloft_II.esf3d):

Good cue timing example, good labeling

[In The Flesh? (Rigg Show)](/Show_Files/In_The_Flesh.esf3d):

Point out use of effects, as well as my poor job of labeling these cues

[Rinzler](/Show_Files/Rinzler.esf3d):

A great showcase of the utility of effects


