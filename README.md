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
Connect the controller to a 24VDC source and turn the power on.  
The display should show initial operaional settings.  
![initial-display](https://user-images.githubusercontent.com/48537944/173248449-61d6c84f-3e33-40d6-957f-e613bfae9d6d.jpg)  
Press and hold the control knob until the unit goes into the setup mode.  
![setup1](https://user-images.githubusercontent.com/48537944/173248480-6f550683-0c8b-4399-b612-039b6713ef3c.jpg)  
turn the knob clockwise until F03 is displayed.  
The bottom line will show the default 010.0  
Pres the control knob again to enter the bottom line edit mode.  
The decimal value will be flashing.  
The decimal value can be changed by rotating the control knob, but leave it at zero.  
Press the knob again and the least significant digit will be flashing. Change it to 9.  
Press again and change the next digit to 2.  
Press again and change the first digit to 3.  
The lower display should  be reading 329.0 with number 3 flashing.  
Do the extended press to get out of the setup mode.  
Now 329.0 should be displayed on the top line and 0000 on the bottom line.  
That sets the stepper RMP.  
Now we have to set the running mode for continuous operation.  
Do the extended press again to get into the setup mode.  
F01 will be displayed on the top line and P01 on the bottom line.  
Press the control knob and the bottom line should be flashing.  
Change the bottom to P03 by rotating the control knob.  
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
Make sure your battery is fully charged. That is very important. You can ruin the camera if you do not follow these instructions carefully. 
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
Thsese two videos give you a pretty good idea on how to set the 3 FPS but there are some devil details missing.  
Will try to cover those in here.  
Set the camera to Movie mode.  
Turn the camera on and turn on live preview.  
This will start the Magic Lantern software.  
Then press the delete button.  
The settings screen will pop up.  
Go to  the Movie screen:  
![movie-setup](https://user-images.githubusercontent.com/48537944/173410631-b84f37f3-2d22-4781-8dc5-e47198cf7e37.png)  
Select FPS OVerride. Press enter to turn it on.  
![fps-override-on](https://user-images.githubusercontent.com/48537944/173410928-b9465114-580a-4dc6-af3b-bd8bc54b9547.png)  

 
Then press the Q button on the T3i. Other camera types will have a similar button.  
The FPS Override screen will pop up.  
![fps-override-2point5](https://user-images.githubusercontent.com/48537944/173411311-96491cbb-5bef-4442-84dd-7921efc8d538.png)  
Hit the Q button.  
![fps-set](https://user-images.githubusercontent.com/48537944/173411557-050bc2e0-c122-4d3a-8280-0a184a5e4afc.png)  

Position highlight over desire FPS and hit Enter. Set desired FPS to 3 by using the left and right keys.
  
 ![fps-set-to-3](https://user-images.githubusercontent.com/48537944/173412055-d738573a-8af2-4d1a-9759-3beae8309035.png)  
Press enter again to go bach to the FPS Override screen. Select the "Optimize for" entry and hit Enter.

![optimize](https://user-images.githubusercontent.com/48537944/173412603-907a7f5f-5c9d-4de9-bf99-3acc218f2fad.png)  

Select High FPS  

![high-fps](https://user-images.githubusercontent.com/48537944/173412899-56c74262-194f-4700-8b71-c97da3110da7.png)  

After selecting High FPS the camera will go back to the FPS override screen.  

![fps-override-1](https://user-images.githubusercontent.com/48537944/173413521-0f9b0cf9-9c6b-4795-b0b9-f9728015c3db.png)  

Select Advanced Mode.  

![advanced-mode](https://user-images.githubusercontent.com/48537944/173413832-12f88ee1-d592-4d3f-a50c-26da8d39a673.png)  

Select Timer B. Leave it as is for now but remebmer how you got to this point becase you will need it later   
for sync procedure.


![tune-fps](https://user-images.githubusercontent.com/48537944/173414357-af3ce939-8aa3-4b1e-8913-95226f334614.png)  

Go back to the FPS Override screen.  

![fps-override-2](https://user-images.githubusercontent.com/48537944/173414728-47bcc136-90b4-48be-8c7a-629bb855be54.png)  

The shutter speed can be changed on the Expo screen.  

![shutter](https://user-images.githubusercontent.com/48537944/173415582-011e393d-8f19-4740-a6cb-866827e335f5.png)  

The shutter rspeed can also be changed while scanning the film by using the main dial. Check the manual fo main dial location (tp of the cam).
The light should be bright enough so that the shutter speed is 1/300 or faster. If the shutter is too slow than some image degradation can happen.
It is to be noted that even at this fast shutter setting, due to low FPS you could experience some jello effect. The jello effect exhibits itself as a 
the video shrinking and expanding as jello and can be very annoying. The cause is the rolling shutter which stores one image line at a time. At slow scan   
there is a shift in the top of the image as compared to the bottom of the image i.e. by the time the scan gets to the bottom the scene has changed somewhat.   
But on a positive note, the postprocessing done in DaVinci Resolve almost completely eliminates this degradation.   


## Macro Lens
There are many out there that will do the job.  
Venus Laowa is a pretty good pick. It has more than enough magnification and good image quality and it is reasonably priced.
https://www.venuslens.net/product/laowa-25mm-f-2-8-2-5-5x-ultra-macro-2/  

## Sync procedure
Back it off and turn it away from the gate and point it to the cam (pulley). Adjust the speed control on the controller until the cam appears stationary. Actually it will jump up and down and possibly drift slowly. If the drift cannot be stopped by the speed control, then adjust the Magic Lantern Timer B to minimize the drift. Once done, refocus the camera back onto the gate. With this procedure I can run for several thousand frames without sync issues. It should be noted that the transport should be in good condition ensuring constant speed. It still may be possible that the drift catches up with you depending on the initial condition. In that case just run one step up for a few minutes if the drift is from the top, or one step down if the drift if coming from the bottom. Then switch back to the original speed. After that you can run for several thousand frames without sync issues
![image](https://user-images.githubusercontent.com/48537944/180618061-7d2a6fb7-f8a7-4087-b8a3-5f7daaafc266.png)

## Operation

Load the film.  
Plug in the 24V and 12V external power sources. 12V is for the takeup and 24 is for the controller.     
Make sure that they are not reversed which can result in the takeup motor damage. 
Turn the light on.  
Connect the camera HDMI port to a monitor.  
Turn the camera on and press the live view button. This will start Magic Lantern. 
Press Live View again to start recording.  
Press  the CW button on the controller.
Once done with the recording, stop the camera by pressing the live view again abd stop the controller by pressing the stop button.  
Remove the SD card and copy the MLV (Magic Lantern Video) to a PC.  

## Post Processing  
Download the MLV app from:  
https://mlv.app/  
Install the app.  
Open it up.  
Drag the video into the session window as shown:  
![mlv-drop-video](https://user-images.githubusercontent.com/48537944/173479549-8c4df25d-a010-47af-9b7b-28c063cb8ecd.png)  
Expand the transformation entry on the right hand side and turn the Upside down control on.  

![upside-down](https://user-images.githubusercontent.com/48537944/173480320-366daada-0fcd-46e0-97f8-a7f7ceb87d69.png)  
Review the video to see if any sections have to be retaken. This app has pretty limited video edit capabilities  
but it has lots of export formats suitable for popular video editors.  
Open up export settings from File pulldown:  
![image](https://user-images.githubusercontent.com/48537944/180661745-8ef49445-3754-4c26-add9-a49aab088496.png)  
Select DNG uncompressed format if exporting to Resolve.  
The DBG images take up lots of space but in return contain the raw information that can be utilied in DaVinci Resolve.  

Export the video by using File->SaveVideo into the directory of your choice.  
Close the mlvApp.  

## DaVinci Resolve  
Open up Davinci Resolve and drag the DNG images into it.
![image](https://user-images.githubusercontent.com/48537944/180619203-704e0f97-1912-41b4-a0dc-79f54f4bb59e.png)  
  
Right click on the clip and create the new timeline:  
![image](https://user-images.githubusercontent.com/48537944/180694116-937ee76a-168a-4275-98ae-e95b0bc34643.png)  
Click on Custom Settings and change the frame rate to what you need.
Switch to Edit Mode:  
![image](https://user-images.githubusercontent.com/48537944/180694518-8c3ce3cc-6a11-4e9b-a1d0-4220dcd03903.png)  
In the transform area on the right hand side, rotate the video by 180 degrees.  
![image](https://user-images.githubusercontent.com/48537944/180694747-e9a97d54-78d8-4ac5-8679-075879563a2a.png)  
Switch to color edit mode. Select Camera Raw and Decode using Clip as shown:  
![image](https://user-images.githubusercontent.com/48537944/180695224-1fa51c51-9f6c-4720-8a38-9d6c45401b00.png)  
Adjust exposure as shown:  
![image](https://user-images.githubusercontent.com/48537944/180695545-dfea4c00-e529-47d1-ad65-131dfeffec46.png)  
If the video shows a jello effect then this would have need adjustment.  
Go back to the edit mode:  
In the transform area on the right hand side scroll down to Stabilization.  
Set mode to Perspective.  
Turn on zoom and then adjust stabilization parameters as needed. It will be a trial and error process. Too little and the  
video will be wavey and too much will cause severe clipping and loss of resolution.  
![image](https://user-images.githubusercontent.com/48537944/180696604-039487f6-b116-4e44-9e9d-1da32f21ff1e.png)  
Click on the stabilize button to run stabilization. It may take a while. 


https://www.youtube.com/watch?v=u6UWJCQB7n0  
If the video has noticable jello effect then apply the Resolve stabilizer as shown the video below.  
https://www.youtube.com/watch?v=73zwjGcbhP4  


### Slow Motion interpolation with speed change  
Save the VirtualDub2 video as a sequence of tiff images first.  
Select all images and drag them into the media window of DR (DaVinci Resolve).  
 
 
You will get the images shown as a clip in the media window.  
![image](https://user-images.githubusercontent.com/48537944/180619212-828a3de1-851f-4cf8-a7a2-47bfa6bb8676.png)  
 
Right click on the clip, select the click attributes and set the frame rate if necessary  
but you can leave it as is since the frame rate change can be done later.  
Right click on the clip and create the timeline from it.  
![image](https://user-images.githubusercontent.com/48537944/180619225-345b8e81-ec78-479b-94b7-e2f97adf7c30.png)  
   
Switch to Edit Mode.  
![image](https://user-images.githubusercontent.com/48537944/180619234-86995e77-761f-44a0-9d12-d6ada4e905de.png)  
   
Click on project settings  
![image](https://user-images.githubusercontent.com/48537944/180619243-e580c29c-0edf-44fb-81d3-7b2deffc2aa8.png)  

Scroll the settings all the way down and change the retime process to optical flow (more info available here  
htps://www.youtube.com/watch?v=m5cO3ZTfSr4 ).  
![image](https://user-images.githubusercontent.com/48537944/180619256-29f35819-dcf0-4f69-85e8-94d3d8003348.png)  
  
Save the settings.  
Now, right click on the clip and change the speed to whatever FPS needed.  
![image](https://user-images.githubusercontent.com/48537944/180619268-b8178c8d-e158-4743-92fd-340c7e210da1.png)  
 
Change the FPS to whatever required.   
![image](https://user-images.githubusercontent.com/48537944/180619315-2dbbaf0f-2f1f-48d7-b8a9-6c3a3933df74.png)  
 
Make sure that Ripple sequence is checked off. If not the clip duration will not change and the clip will be truncated.   
Click on the change button. Note the clip duration change in the timeline window.  
![image](https://user-images.githubusercontent.com/48537944/180619352-2ec00329-eefd-41fb-a8aa-9ccd77d733c9.png)  
   
Once done, complete other changes as necessary and then export the video by switching to deliver mode.  
![image](https://user-images.githubusercontent.com/48537944/180619360-5407f6d7-aed8-4a67-9b4b-78735360357f.png)  
   
Change the video format to whatever you like.  
![image](https://user-images.githubusercontent.com/48537944/180619378-b0e0d92c-463e-4605-9e59-d106182308f2.png)  

  
Add to render queue  
![image](https://user-images.githubusercontent.com/48537944/180619395-ef1c1233-b613-4d20-a9e7-7a56be25882d.png)  
 
And then start render.  
![image](https://user-images.githubusercontent.com/48537944/180619406-686878cc-9b0b-4b1b-81fa-793b59724582.png)  
 
  
### Interpolation without Speed Change  
The above instructions were for interpolated frames that result in smooth slow motion speed.  
In many cases however we want to interpolate the frames but want to maintain the original speed.  
In order to do that just follow the above instructions but do the following changes.  
1.	Make sure your project settings are set to optical flow for retiming.  
2.	Before creating the timeline set the clip attributes FPS to 60 FPS.  
3.	Create new timeline  
4.	Using the above procedure change timeline speed to 24 FPS or whatever final speed you need  
The rest is the same as the above procedure.   
Here are the details.  
Project settings optical flow selection.  
![image](https://user-images.githubusercontent.com/48537944/180619455-12188348-1c33-4169-89d3-2126d460e21a.png)    
![image](https://user-images.githubusercontent.com/48537944/180619472-358fd16f-9dc0-4bfc-a6a0-b8dee4f0f4a2.png)    

  
 
Drag the images into the media window. Make sure all images are selected.  
![image](https://user-images.githubusercontent.com/48537944/180619481-8ba11c67-dd62-42ce-8d37-5ee0768b0d79.png)  
   
Switch to edit mode if not already there.    
![image](https://user-images.githubusercontent.com/48537944/180619490-9fe5d6c1-8b4f-48ff-8be0-1a5253c04d61.png)  
   
 Right click on the images file in the media window and select clip attributes.  
 Set clip FPS to 60 or whatever interpolation rate you prefer.  
![image](https://user-images.githubusercontent.com/48537944/180619499-66b07d4a-c497-45a7-b44c-6966d76eb3bb.png)   
Click on OK.   
Right click on the clip again and create the timeline. The timeline create window pops up.  
Click on custom settings.  
![image](https://user-images.githubusercontent.com/48537944/180619568-1988a295-b602-457b-a992-b2c11cec7259.png)  
 
It is to be noted that in version 17.2 of DaVinci the timeline popup window is a bit different.  
It does not have custom settings but it has a button to use the Poject Settings.  
Make sure that button is not checked off. 
![image](https://user-images.githubusercontent.com/48537944/180619574-8853da27-8870-420d-bec1-f48e559c691d.png)  
  
   

Select Format tab and set the desired interpolation FPS.  
![image](https://user-images.githubusercontent.com/48537944/180619589-226c44c1-573a-4007-8735-dcc559f3d300.png)  
 
The new timeline will show up in the timeline window.  
Right click on the timeline in the timeline window and select Change clip speed.  
![image](https://user-images.githubusercontent.com/48537944/180619600-a8a8fc41-1e4a-43a5-988a-2de2381fea93.png)  
  
 
Change clip speed back to normal speed i.e. 24 or 18 FPS or whatever the original speed was.   
You can also go lower if slow motion is preferred. Make sure Ripple sequence is checked off.  
![image](https://user-images.githubusercontent.com/48537944/180619606-c68f281b-b053-4d03-a859-6c10d2425c68.png)  
 
Note the clip stretching out after the speed change.   
If t does not then make sure that Ripple sequence is checked off.  
At that is basically it.   
You can test run the clip to make sure that additional frames got added by stepping through the video (left, right arrows).  
The next step is to render and save the video.  
Switch to Deliver Mode.  
![image](https://user-images.githubusercontent.com/48537944/180619623-8000a8ab-3fb0-4a8f-a379-966e5285d7ce.png)  
   
Select proper video format and add to render queue. 
![image](https://user-images.githubusercontent.com/48537944/180619633-f6376daf-8817-432f-91b2-fc6f34be8866.png)  
   
Start rendering.  
![image](https://user-images.githubusercontent.com/48537944/180619641-b2f8921d-034b-40f7-a57d-aac214f38538.png)  
 
And that completes the procedure.  








