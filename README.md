# SMC02 video capture
This setup consists of a modified projector and the T3i Canon camera. The setup provides the 8mm film capture running at 3FPS and outputs the video in ML (Magic Lantern) RAW format in 1728x972 resolution.  
The purpose of this  readme is to provide the instructions to the user on how to modify the existing 8mm film projector for the video capture directly into the camera using a small off the shelf stepper controller.  
Similar to other projects of this type, this one also requires several modifications to the projector including the light change, and motor change but unlike other projects of this type it provides the DSLR camera capability and RAW video format. The DSLR is used in a slow video mode. 
The stepper controller is programmed to precisely control the stepper motor rotation to provide the proper FPS which matches the FPS of the camera with no flicker. 
System Components  

![system-assembly](https://user-images.githubusercontent.com/48537944/173163427-688c6a8b-efea-417d-83be-57d9c426cfe2.jpg)


## Stepper Controller  
At the heart of the system is the SMC02 stepper controller. 
https://www.ebay.com/itm/175028855543

## Stepper Motor  
Use the following stepper.
2.7A for this type motor https://www.amazon.com/gp/product/B00PNEPF5I/
Other steppers may also work but are not covered in this readme.  
If you are planning to pull the projector transport out, then you can use the mounting bracket from this repo.  Check the mechanical parts folder. 

## Pulley
This pulley is recommended. You will also need a sleeve because the pulley bore is slightly larger than the motor shaft. 
Check t mechanical folder for the sleeve sdl.
https://www.amazon.com/gp/product/B07C4QD1BV/

## Belt
This used to be a big problem but with the neophrene Urethane belting that became available it is easy to make your own custom belt.
https://www.amazon.com/gp/product/B07L3W7Z1N  
Follow the following instructions:  
https://www.youtube.com/watch?v=mBtHvPWVgDw

## Assembly
Print out all of the parts from the mechanical folder. If you do not have the printer then you can get them done outside but it will become rather costly. Getting a new 3D printer will probably be cheaper in a long run.
Use a 14"x10"x0.63": piece of wood to mount the components on.  
https://www.homedepot.com/p/Rubbermaid-Black-Laminated-Wood-Shelf-10-in-D-x-36-in-L-4B2500BLA/100200907
Additionally cut two additional pieces of wood size 7"x7"x0.63"and 7"x3.6"x0.63". These will be used as a standoff for the projector transport. 
This will work for the Chinon 2500GL but if other type of projector is used then you will have to figure out how high the the transport has to sit for the proper alignment with the camera.
Assemble the three pieces of wood as shown.
![base](https://user-images.githubusercontent.com/48537944/173167740-4549d843-7a39-4b3f-81aa-acde52419084.jpg)
Mount the projector transport bracket to the base as shown.
![transport_bracket_assembly](https://user-images.githubusercontent.com/48537944/173168094-8e724da4-6d37-4858-b55a-3e116a983f5c.jpg)
Mount the transport onto the bracket using the original transport mounting screws.
The transport mounting will need additional support to prevent the film shake. Use an L bracket  
https://www.homedepot.com/p/Everbilt-3-in-Black-Corner-Brace-4-Pack-13741/300985591
and mount it as shown. Install the spacer underneath the bracket so that the transport sits perfectly vertical. The spacer is included in the mechanical folder. If the transport is not vertical then adjust the spacer accordingly. Tilted transport will cause focus issues.
![L-bracket1](https://user-images.githubusercontent.com/48537944/173203915-0b7c2205-18c9-4ed2-acd2-2f6386e38e1f.jpg)

Mount the macro lens onto the camera.  
Mount the camera onto the slider.  
Turn the camera on and position it so that the film gate is visible and adjust the zoom so that the film gate covers most of the camera display. Set the slider knobs about half way of the travel. Now, slide the camera on the base board left and right and forward and backwards until the gate is centered in the camera display. Mark the position of the slider  on the base board.  
Remove the camera from the slider.
Place the slider upside down on the table and place a piece of white paper over it. Trace the outline and teh mounting holes as the first graders do.  
https://craft-art.com/tracing-pictures/  
Cut the outline with the scissors and place it on the board so that it is aligned with the marked up outline on the board done in the previous step. Drill the holes. Remove the paper template and mount the slider onto the board using the appropriate size screws.  
Light Mounting.    
The light has to be mounted in front of the gate.    
(This is still work in progress -- will be updated shortly)    
Takeup reel mount.    
Use the microphone stand  
https://www.amazon.com/dp/B07F82BPLV  
Remove the microphone adapter and install the takeup motor bracket.   
Mount the takeup motor onto the bracket using the M3x8 screws  
https://www.amazon.com/gp/product/B076J3W7R4  
Slide the takeup spindle over the motor shaft.  
Slide the takeup reel over the spindle.  
Install an M3 wingnut onto the M3x25 flathead screw and tighten it.  
Slide a flat M3 washer over the screw shaft to create the "clutch" mechanism.  
Push the screw through the spindle center until it engages with the motor shaft.  
Turn the wingnut in until snug. The tightness will determine the amount of pull on the film.  
You do not want it too tight becaue it can cause film damage.  
Solder two wires to the motor terminals.  
Connect the wires to the speed controller.  
https://www.amazon.com/gp/product/B071H2YQG5/  
Connect the controller to the 12VDC source.  

Proceed similarly with the supply reel. 
Remove the mic adapter from the microphone stand. install the reel mount assembly onto the mic stand.
Install the small clip onto the reel spindle using a small metal pin. 
https://www.amazon.com/Neiko-50412A-Assortment-Storage-Pieces/dp/B076B4WT1V/

![supply-reel-mount_assy](https://user-images.githubusercontent.com/48537944/173245376-b92633f0-b09d-489a-a38e-4be9c1ece796.jpg)
Controller installation  
Afix the mounting bracket onto the base board by using two wood screws.
Mount the SMC02 cntroller onto the controller mount but sliding it into the mount opening all the way until locked in. 
Wire up the controller as shown.
![smc02-wiring](https://user-images.githubusercontent.com/48537944/173245893-993bcfc1-24d4-49e9-b0c8-dc20c5d2387e.jpg)

Stepper Installation  
Mount the stepper onto the stepper racket using the M4 screws and nuts.
Mount the sleeve over the motor shaft and then side the pulley over the sleeve. Do not tighten the locking slugs. 
Align the pulley with the transport cam and install the belt. Slide the stepper assembly left and right on the base board until the belt is aligned and has 
good enough tension on it. Mark up the stepper bracket location.  
Remove the stepper from the bracket and install the bracket by using 2 wood screws. Mount the stepper back onto the bracket and install the belt.

## Tuning the Stepper  
The FPS (fremes per second) of the film transport is not the same as the stepper RPS (revolutions per second) due to different pulley diameters.  
The ratio has to be determined experimantally.  
Connect the controller to a 24VDC source and turn the power on. The display should show initial operaional settings.
![initial-display](https://user-images.githubusercontent.com/48537944/173248449-61d6c84f-3e33-40d6-957f-e613bfae9d6d.jpg)
Press and hold the control knob until the unit goes into the setup mode.
![setup1](https://user-images.githubusercontent.com/48537944/173248480-6f550683-0c8b-4399-b612-039b6713ef3c.jpg)
turn the knob clockwise until F03 is displayed. 
The bottom line will show the default 010.0  
Pres the control knob again to enter the bottom line edit mode.
The decimal value will be flashing. 
The decimal value can be changed by rotatin the control knob, but leave it at zero.
Press the knob again and the least significant digit will be flashing. Change it to 9.
Press again and change the next digit to 2.
Press again and change the first digit to 3.
The lower display should  be reading 329.0 with number 3 flashing.
Do the extended press to get out of the setup mode.
Now 329.0 should be displayed on the top line and 0000 on teh bottom line.
That sets the stepper RMP.
Now we have to set the running mode for continuous operation.
Do the extended press again to get into the setup mode.
F01 will be displayed on the top line and P01 on teh bottom line.
Press the control knob and the bottom line should be flashing.  
Change the bottom to P03 by rotating teh control knob.  
Do the extended press to get out of setup.

Quick Test  
Press the CW button - the motor should run clockwise and the film cam should rotate at 3 RPM.
Press the stop button. The motor should stop.  
Note: If the motor rotation is reversed then reverse the green and black wire connections.
Another Note: The reverse speed is set to 10 rpm which is slow. If planning to use the reverse operation then the reverse speed is set by changing the F05 field  
by using similar procedure as listed above.  

## Camera  
The camera used should be capable of caustom frame rates. 
Sony A7iii supports custom rates but it is quite expensive.
An alternative is to obtain the T3i body and add the macro lens. 
The stock camera does not support the custom frame rates but there is a custom software available that enables   
custom frame rates and raw video.
Listed below are the instrustions on how to install Magic Lantern and set it up for FPS override, but before that here is a quick overview:  
Download the build to your PC and unzip it.
Format the SD card by the camera itself.
Make sure your battery is fully charged. That is very important. You can ruin the camera if you do not follown these instructions carefully. 
Install the SD card into the camera and power it up.  
BTW - going forward any time you open the SD card cover, do not remove the  SD card immediately, wait for the red led to stop flashing.
Set the camera to Manual mode
Press the MENU button 
Go to the second last screen and press the Firmware button.
Double check the Magic Lantern instructions
https://builds.magiclantern.fm/600D-102.html
Do the update
Recycle power and you are ready to go.

Refer to https://magiclantern.fm/  
for more details.
Specifically refer to this page for the T3i:  
https://builds.magiclantern.fm/600D-102.html
For setting up the camera refer to:
https://www.youtube.com/watch?v=NYGseJ7Sofk  
https://www.youtube.com/watch?v=RvZHmOgzm2Q&t=6s
Once the Magic lantern firmware is installed, you will have to tune the camera frame rate to the stepper speed.  

![image](https://user-images.githubusercontent.com/48537944/172065363-53090a44-6c1e-469d-9352-3fc1c2dfb79d.png) 
Set the camera to Movie mode.
Turn the camera on and turn on live preview. This will start the Magic Lantern software. Then press the delete button. The settings screen will pop up. Go to  the Movie screen and select FPS OVerride. Then press the Q button on the T3i. Other camera types will have a similar button. The FPS Override screen will pop up. 
![image](https://user-images.githubusercontent.com/48537944/172065508-eeb83ff0-b7ae-45aa-86df-2e59e3ea5d34.png)  
Set the desired FPS to 3. 
Go back to the FPS Override screen and set the Optimization for High FPS.  
Timer A and B and used to set the frame rates and the exposure time. 
Set Timer A to 584. The desired FPS shown should be 3.010  
Note: If your pulley and film transport cam are different sizes then both the controller RPM and camera Timer A values will be different.  

![image](https://user-images.githubusercontent.com/48537944/172066458-05501697-061e-405c-bfe0-dad2fb506449.png)
Scrawl down to the "Optimize for" line and hit the Q button.
Set the optimization to High FPS.  
This will allow for custom shutter speed. 
There is a discussion on this topic in the Magic Lantern forum. It may help a bit.
https://www.magiclantern.fm/forum/index.php?topic=4718.0;prev_next=prev#new


## Macro Lens
There are many out there that will do the job.  
Venus Laowa is a pretty good pick. It has more than enough magnification and good image quality and it is reasonably priced.
https://www.venuslens.net/product/laowa-25mm-f-2-8-2-5-5x-ultra-macro-2/  


## Operation
Very straight forward. Here is a short video showing the operation.  
Plug in the 24V and 12V external power sources. Make sure that they are not reversed which can result in the Hawkeye2 board damage.  



