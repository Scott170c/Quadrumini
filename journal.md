### Quadrumini Journal started for [Highway to Undercity](https://highway.hackclub.com/)
total hours worked: `6`

# `6/3/2025` - Research on Electronics Design (1 hr)
I did some calculations for the power source I need in order to power my quadruped, and I have come up with two options:
- Stay with 8 motors and have 4 DOF
- Upgrade to 12 motors and have all 6 DOF
I think I will be ambitious, and go for the 12 motors to have all 6 DOF, but the power consuption will be really high 👀

Also did research on motors, and I will be sticking with the MG90! I want to keep my robot affordable 🥳

# `6/4/2025` - Research on General Design (1.5 hrs)
Today, I did some research on different types of legs, and since one of my goals is to have my robot jump I was thinking of using a compliant leg. I looked into many designs and if I do end up going for a compliant leg I will most likely be going with this one! I like it's simplicity.

<img src="images/compliant-leg.jpg" height="300px"> 

[Design by Adam Beedle](https://www.youtube.com/watch?v=bDxItdyQ3jc)

On Saturday, I hope to start working on my first CAD and print out a couple iterations :)

# `6/10/2025` - More Research & CAD (3.5 hrs)
I looked into which MCUs to use and came to the conclusion that the Raspberry Pi Pico would be the best option for me, coupled with a PCA9685 Servo Driver. It is able to give me the power I need to move all 12 servos at once and keep it cost efficient :) It's power will be a massive upgrade from the Arduino Nano I have been testing with.
<img src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/52b794703264e8a8eebe371b5e74464ebdd3ddaa_pi_pico.png">
<br></br>
I also started cading the leg for the robot, and got some progress. A lil rusty with Fusion 360 so it took me longer than I would like to admit (which is why I spent so much time here) but I got the CAD done and learned how to put articulate joints on! Each leg has 3 DOF!
<br></br>
<img src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/91dfc603a6b065818cd4dfe51f1b302d0a68d026_image.png" height="400px"> 
<br></br>
Because there is now 3 DOF per leg, I have decided to not design a compliant leg. I may design one in the future but I have decided to go for more degrees of freedom 🕺 over jumping ⬆️ for now.

# `6/14/2025` - Title (4 hrs)
Today, I got a lot done! I remade the CAD for the hip flexor to shed some weight and also make it easier to use, and started working on the PCB for the robot, which I intend to use to drive the entire thing off of!
<br>
Hip Flexor Redesign:
<br></br>
<img src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/09045d5d56b372126f6a17f4356aa750195ee9b2_image.png" height="200px"> 
<br></br>
The last design was very boxy, and took up a lot of space laterally, which was limited. With this redesign, I moved it's bracing to be vertical and made it overall thinner! It is also now way easier to put in the servo horn :)
<br>
Current PCB Schematic:
<br></br>
<img src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/c801dd129de85170f7912f296416dcfc8e0e7cdd_image.png" height="400px"> 
<br></br>
I am using the Raspberry Pi Pico as my MCU (Microcontroller Unit) and will be using the PCA9685 chip to drive everything, which makes it so that I can drive all of the servos through one I2C connection! I decided to put everything on a PCB, as I wanted to minimize the amount of wires as much as possible. This design option will give me more space in the housing to cram the servo wires in, and put my MPU chip in a more precise spot! (will be implementing that very soon)

# `0/0/2025` - Title (_ hrs)
