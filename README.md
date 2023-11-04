# Womble
This is a repository with resources from my one watt Dumble ODS style build. 

This is a repository with resources from my one watt Dumble ODS style build. 

Thank you all for showing interest in my 1 Watt Dumble ODS style build. I would like to stress that because I didn't intend on posting this stuff in detail, I **did not** create a full layout, schematic, etc. Like all amp builds, just because this worked for me doesn't mean it will work for you, so please **build at your own risk**, especially given that this build is not currently well documented. 

Now, for the fun stuff! In this repository, I have included a few resources to help you with your build. Below is the table of contents. Everything should be quite well labeled, however. 

wombleDocumentation - This is the section for the very little documentation I have. The documentation here will be directly from The Amp Garage. **I do not take credit for the layout or design of this amplifier**, I only made a PCB and a chassis. **IMPORTANT BUILD NOTES:** 

Regarding the power side of the amp, the wiring is a little different than is given on the layout given. Please follow these steps: **NOTE THAT IF YOU PURCHASED A BOARD FROM ME, THE LABELING IS SLIGHTLY DIFFERENT, AND I WILL GIVE YOU INSTRUCTIONS IN AN EMAIL**
* From the hole labeled STBY, take a piece of wire and run it to the positive lug of the 100uF cap. 
* From that same lug of the 100uF cap, run another piece of wire to one side of the STBY switch
* From the other lug of the STBY switch, connect one lead of the choke 
* To this same lug of the STBY switch, also connect the red lead of your OT
* Connect the other lead of the choke to the hole labeled choke
* 
In the layout I provided (and in most Dumble amps), a relay is used for switching between the overdrive and clean channel. I did not include this relay, and am instead using analog switching. Wire it like you would a typical DPDT signal switching switch: 
* 1-1 on the board → pole 1- lug 1 on OD switch
* 2-1 on the board → pole 2- lug 1 on OD switch
* 2-2 on the board → pole 2- lug 2 on OD switch
* 1-2 on the switch → to master vol pin 1
* 1-3 and 2-3 on switch → together

Power amp section
You will notice that some of the values on the PI on the board are different than on the schematic. This is because I took inspiration from Rob Robinette (https://robrobinette.com/Amp_Stuff) on the phase inverter to make it so a more appropriate load goes to the power tube. For the power tube, I am using a 12AU7, which has a pretty low gain, making it perfect for this application. Pins 1 and 6 of this tube go to the Blue and Brown leads from the OT. Output leads will depend on the impedance desired. For me, I wanted 8 ohms so I did yellow and orange. 

The space for a resistor labeled NFB is the NFB resistor. Dumble used a value of 820 ohms in this specific layout of this specific amp, but as this is a highly opinionated thing, I left it up to interpretation. 

Switches being used as SPDTs
The layout has them wired in a weird way. I just wired them like I would a normal SPST.

Don’t forget that because the heater tap on the PT isn’t center tapped, you must create an artificial CT using 2 100 ohm resistors to ground

womblePCB 
This will have the latest version of the PCB. I will include both a .brd and a gerber file (for uploading to JLC). 
**as of the writing of this,** I have 4 PCBs left (I made one and JLC sells in minimum quantities of 5). If you live in the US, I am happy to ship some of my leftover PCBs to you, as long as you pay for shipping. That way, you don’t have to wait for JLC to make them, for them to come over from china, etc., and so you don’t have to get 5. Please note that when I wrote this (after making the amp), I noticed some mistakes on my board and have corrected some of the labeling and one trace. If you want to get a board from me, I will give you instructions on what to do. Please shoot me an email at Evan@sharkbomb.net. 

wombleChassis
Here, I have uploaded the STEP file for the chassis. I ordered mine from https://www.oshcut.com. The step is made with a 0.075 in thick piece of steel. 

* Please note that as of right now, some of the mounting holes in the chassis are not large enough for the screws I have specified in the BOM. This means you will have to drill some of them out a little bit wider. I used a step bit. There's only a few, it took me like 5 minutes. I may change this later, depending on interest in the amp. 
* The mojotone cap can holders also did not have a dimension for how far apart screws had to be. I just left it out and drilled it myself. Depending on interest, I may change this later.  
* I also feel like one of the mounting holes for the choke or OT was off slightly, but that is again an extremely easy fix. Depending on interest, I may change this later.  


wombleBOM
This is the BOM that I used for the amp. Notes on the BOM are as follows:
* For the power resistors, I used quite high values to keep the volume down a little bit (less voltage going into the tubes). Feel free to use ohms law or a step down resistor calculator to calculate what value you want these to be at (highlighted in dull yellow)
For the 100uF power cap can, I chose this value because it is half of what dumble used (220/2) and because I like the extremely tight, dry sound you get from overspecing a cap. You may not like this, so play around with different cap can values for this specific can
* I used this lamp because it kinda looks like what Dumble put on his original early series ODSs, which is what I designed the aesthetics of this amp off of. Most traditional lamp bulbs will work in this scenario.

wombleReference
This includes reference images of my own version of this build. Maybe it will help a little bit with the ambiguity of my layout and such. 

Mods I did to the original circuit
I did 2 mods to the preamp from the layout shown. Because they are personal mods, I didn’t include the parts in the BOM. 
One was adding a cap between the plate and cathode on the OD tube. This reduces the brightness of the overdrive signal. I forget exactly what value I used, but I experimented with a few to get the right balance 
The other one was adding a local NFB switch to V1B. This was simply done by putting a 22M resistor and .047uF cap in series between pin 6 and a switch (which I mounted on the bottom of the chassis). On the other side of the switch, I simply put another 22M resistor to pin 7. This creates a negative feedback loop around that one stage of the tube. 

If you have any questions, Please reach out to me at evan@sharkbomb.net. I will try to respond as quickly as I can. Sorry my documentation is so bad. Because I am a student, I don’t really have that much time to work on stuff like this, but if enough interest is garnered for the project, I will take some time to create a layout. Thanks for your interest. 
