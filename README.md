# VESC
Please read the WiKi 
![image](https://github.com/Electric-Go-Kart/VESC/assets/101066043/ff0245c0-acd6-424c-b144-739bf9c34b17)

# VESC Tool Setup Guide

Before using VESC Tool, follow these steps to set up your electric kart's ESC (Electronic Speed Controller) for optimal performance.

## Preparations

1. Ensure the rear wheels and motors are free of any obstructions. Place the kart on blocks and keep the chain clear of debris.

2. Connect the throttle pedal cable and USB cable to the same ESC; this ESC will serve as the "Master." The CAN BUS cable will enable control of the slave ESC through the Master.

3. Ensure that your batteries are fully charged.

## Using VESC Tool

1. On the Main Menu, select "AutoConnect." If done correctly, both ESCs should appear under CAN devices. The "Master" will be labeled "local," while the slave will have a random number. You should change the slave labels to 1 and 2 later to avoid potential issues with the dashboard code.

2. You can now edit various settings. Remember to press both write buttons to save any changes.
    - **Read Motor Settings**
    - **Reset Motor Settings**
    - **Write Motor Settings**
    - **Read Application (What is saved on your computer)**
    - **Reset**
    - **Write (Save to your computer)**


## Programming the ESC
![image](https://github.com/Electric-Go-Kart/VESC/assets/101066043/12c8a130-4e69-40a7-ae15-195bf470ba7b)

1. On the welcome page, begin by setting up the motors. You will be asked if you want to reset the CAN bus, which means both ESCs and Motors will be reset to default settings. It's recommended to select "Yes" to ensure a clean slate.

2. Specify the following motor and battery details:
    - Motor Type: Medium Outrunner Motors
    - Battery Type: LiPO (verify the number of cells)
    - Measure the wheel diameter and gear ratio (e.g., 220mm wheel and a 30:9 gear ratio).

3. Run a test. Ensure that nothing obstructs the chain, wheels, or motors. They will spin at nearly full speed. Note that the motors should spin independently if the axle is left split.

4. After the test, you can edit the direction the motors consider as "forward," depending on how you connected the 3 phases.

5. The default base settings should be adequate, but you may need to make additional adjustments.

6. Next, use the setup input:
    - Choose the throttle that matches your pedal (usually the motorcycle-style one in the program).
    - You can adjust the input mapping and consider raising the minimum input to reduce the impact of noise on motor behavior.

## Final Configuration
![image](https://github.com/Electric-Go-Kart/VESC/assets/101066043/9bf07837-c621-4796-a0c2-70b7a50bdd84)

1. Click on the Master ESC under CAN Devices; it should be labeled as "local."

2. Under APP settings, go to General. Ensure the master is set as "ADC" under "app to use." The VESC ID must be set to 1. This is crucial for the dashboard code not to break. Save settings using the buttons on the right side.

3. Click on the slave ESC; it should be labeled with random numbers. Under general settings, set the slave as "No App." This way, only the CAN bus can control it. The VESC ID must be set to 2.

From this point, feel free to edit values as you learn more about your setup. You should be close to the desired configuration, but remember that some values may only appear after you plug into the ESC. If you have any questions or need assistance, send screenshots of the VESC Tool for better guidance.

# References:
https://github.com/vedderb/bldc/blob/master/documentation/comm_can.md
