# Hawkeye2_video_capture
This setup consists of a modified projector and the T3i Canon camera. The setup provides the 8mm film capture running at 3FPS and outputs the video in ML (Magic Lantern) RAW format in 1728x972 resolution.  
The purpose of this  readme is to provide the instructions to the user on how to modify the existing 8mm film projector for the video capture directly into the camera using a small off the shelf stepper controller.  
Similar to other projects of this type, this one also requires several modifications to the projector including the light change, and motor change but unlike other projects of this type it provides the DSLR camera capability and RAW video format. The DSLR is used in a slow video mode.  
The stepper controller is programmed to precisely control the stepper motor rotation to provide the proper FPS which matches the FPS of the camera.  

System Components  

![system-assembly](https://user-images.githubusercontent.com/48537944/173163427-688c6a8b-efea-417d-83be-57d9c426cfe2.jpg)


## Stepper Controller  
At the heart of the system is the SMC02 stepper controller. 

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
Print out all of the parts from the mechanical folder. If you do not have the printer then you can get them done  outside but it will become rather costly. Getting a new 3D printer will probably be cheaper in a long run.
Use  
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





