# Hawkeye2_video_capture
The purpose of this  readme is to provide the instructions to the user on how to modify the existing 8mm film projector for the video capture directly into the camera using a small MSP430 based board.  
Similar to other projects of this type, this one also requires several modifications to the projector including the light change, and motor change but unlike other projects of this type it provides the DSLR camera capability. The DSLR can be used ina slow video mode or frame-by-frame mode using the external camera trigger. This capability is provided by the Hawkeye2 controller. 
For more information on Howkeye2 send the info request to:  
sjelavic123@gmail.com
In frame-by-frame mode the camera trigger is provided by the Hawkeye2 board and in video mode no trigger is required at all.  
In video mode T=the controller is programmed to precisely control the stepper motor rotation to provide the proper FPS which matches the FPS of the camera.
In frame-by-frame mode the Hawkeye2 board is tuned to provide the camera trigger after each rotation of the projector cam.  
This readme covers teh video mode only and for the farme-by-frame info refer to the following page:
https://github.com/vintagefilmography/Hawkeye2_frame_by_frame  


System Components

![IMG_20220504_144707](https://user-images.githubusercontent.com/48537944/166855115-0297680d-0524-4b80-a290-e62c47861d60.jpg)

## Hawkeye2 Controller  
At the heart of the system is the Hawkeye2 controller. This is a custom design. All design info is available here isn this repository. The board details are included in  the homemade-v3 folder. Download the folder to your Eagle project directory and there you will have access to the schematic and the board layout. 
The MSP430 micro controller firmware is available in the MSP folder. Download the zip file from there and save it in your TI Code Composer project directory. From there you can edit the source and flash the target by using TI Launchpad.  
There are two more boards included. One is for the front panel switches and the other is for the switch interface board. Follow the included wiring diagram to interconnect the system.
## Stepper Driver  
The stepper driver is an off the shelf product. 
https://www.amazon.com/gp/product/B075HBJP51/
There are many other variants available. This particular one is a good choice because it has 256 micro steps allowing for a very precise tuning control. One disadvantage is that it operates from a 24VDC source so that two DC adaprers are required, one for the driver and the other one for the controller that requires 12VDC source.  
Driver dip switches  
The following is recommended:
SW4 - Half Currect
Current - 
1.4A for this type motor https://www.amazon.com/gp/product/B00PNEQKC0/
2.7A for this type motor https://www.amazon.com/gp/product/B00PNEPF5I/
Set the pulse/rev switches for the highest speed that can still hold the torque and there is no skipping of steps. Skipping will result in loss of synchronization.  
## Stepper Motor  
These two motors were tested.
1.4A for this type motor https://www.amazon.com/gp/product/B00PNEQKCdesigned with Spark0/
2.7A for this type motor https://www.amazon.com/gp/product/B00PNEPF5I/
You will have to design a bracket for the motor so that it fits properly in the projector after you remove the old motor. 
A sample stepper bracket is included here as a good staring point. Use the Designspark Mechanical free software to modify the bracket for your projector.

## Pulley
There are quite a few pulleys avaliable online.  
Example:  
https://www.amazon.com/gp/product/B07C4R3PGV/  
https://www.amazon.com/gp/product/B07C4QD1BV/
You can also design your own. A sample design will be included here shortly.

## Belt
This used to be a big problem but with the neophrene Urethane belting that became available it is easy to make your own custom belt.
https://www.amazon.com/gp/product/B07L3W7Z1N  
Follow the following instructions:  
https://www.youtube.com/watch?v=mBtHvPWVgDw

## Control Switches:


![front_panel](https://user-images.githubusercontent.com/48537944/167196521-d25ae0d0-ba29-4e8c-b0fa-85e9202a8518.png)

The control switches control the operation of the unit.  
### RUN Switch
Pauses the operation  
### ALIGN
Not used in video mode.  
### REW
Not used in video mode
### PROJ 
Nt used in video mode
### UP and DOWN switches 
Not used in video mode
### Up and DOWN buttons
Not used in video mode
### REV Switch 
Reverses the motor rotation for film rewind.  

## Operation
Very straight forward. Here is a short video showing the operation.  
Plug in the 24V and 12V external power sources. Make sure that they are not reversed which can result in the Hawkeye2 board damage.  

## Tuning the Stepper  
In video mode no stepper tuning is required. It is preprogrammed for 4 FPS.

## Camera  
The camera used should be capable of caustom frame rates. 
Sony A7iii supports custom rates but it is quite expensive.
An alternative is to obtain the T3i body and add the macro lens. 
The stock camera does not support the custom frame rates but there is a custom software available that enables   
custom frame rates and raw video.
Refer to https://magiclantern.fm/  
for more details.
For setting up the camera refer to:
https://www.youtube.com/watch?v=NYGseJ7Sofk  
Once the Magic lantern firmware is installed, you will have to tune the camera frame rate to the stepper speed. .
Go to  the Magic Lantern Settings (delete key)
Then select the video page.  
Then select FPS Override  
Set the frame rate to 4 FPS.  
Turn Constant Expo to ON. This is important because if set to off the camera will pick up it own shutter speed.
This is not mentioned in the referenced youtube video.
Once done with these changes you can proceed to the tuning part. 
![image](https://user-images.githubusercontent.com/48537944/172065363-53090a44-6c1e-469d-9352-3fc1c2dfb79d.png)  
As shown in the attact picture, turn the camera on and turn on live preview. This will start teh Magic Lantern software. Then press the delete button. The settings screen will pop up. Go to  the Movie screen and select FPS OVerride. Then press the Q button on the T3i. Othe camera types will have a similar button. The FPS Override screen will pop up. 
![image](https://user-images.githubusercontent.com/48537944/172065508-eeb83ff0-b7ae-45aa-86df-2e59e3ea5d34.png)  
Set the desired FPS to 4. 
Go back to the FPS Override screen and set the Optimization for High FPS.
Press the delete button again to get out of the settings screen.
Run a test video with the projector running.   Make sure to set the shutter speed around 300 (use the wheel on the top of the camera)
If the frame rates are off got back to the FPS Override screen and tweak the Timer B value one step at the time and rerun the test until the camera is in full sync with the projector.
Timer A and B and used to set the frame rates and the exposure time. Generally the settings for these timers are not well explained so here is a short explanation that will potentially help.  
The frame rate and the shutter speed  are derived from the main clock. the two timers are used to devide the clock down to get the right frame rates and exposure (shutter speed). Since we use a relatively slow frame rate of 3 FPS the danger is that the rolling shutter can cause some undesired distortions if the shutter speed is too high. The rolling shutter essentially grabs one line of teh sensor at the time so the scene will be different from the bottom and top line. I.e. the scene that was used for the bottom line will not be the same as the scene for the top line. It will be shifted at slow FPS producing the jello like effect. 
This is why Magic Lantern restricts the values of the timers and changes them automatically to reduce the unwanted effects. But unfortunatelly the automatic mode is not very suitable for the film scan and could result in flicker. The way around it is to override the magic Lantern auto settings.  
The good value for Timer B for this setup is FT-39. If your etup is different mechanically then you will have to adjust the values accordingly.  
That is available on the FPS override screen.  
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





