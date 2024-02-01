# AATL Go-Baby-Go Arduino Hat Board

### Designed as a hat board for an Arduino Mega to distribute power and simplify sensor and motor connections. 

## Overall Functions

<p align="center">
  <img src="PCB_V1.2.png" width="350" title="Hat Board V1.2">
</p>

For this design, the input voltage is 12V, which is split to a linear regulator and to the motor controller for power. The 9V regulator steps down the voltage to input into the Vin pin on the Arduino mega, which will output 5V, which will power the sensors and joysticks. 

There are six pin headers for HCSR04 Ultrasonic Sensors. These sensors are connected in two arrays, one forward and one backwards, designated by "North" and "South". Each array contains three sensors to get a large angle to sense objects in front of or behind the car. The current itteration of the code (uploaded in seperate repo linked below), the sensors are triggered to detect distance depending on which direction the input joystick is moving. 

The joystick is a two axis joystick to be used as the only input method for the vehicle. The only info relevant to this repo is that the joystick takes two 5V and two ground inputs, with one pin each for x and y inputs. 

The motor controller is getting 12V power through a single pole double through EStop switch. When in the normally open position, the motor controller will get 12V power to drive the motors. The motor controller is also connected with the other 6 pin header, which contains enable pins for each motor, and two input pins for each motor. 

## GBR and DRL Files

These files are zipped in zip folders labled by their itteration number. Each of these zip files can be uploaded to a PCB printing website or a GBR file viewer and the PCB designs should be fully portrayed.

## V1.2 Changes

There was an error made in the design that when the EStop switch was in the normally common position, the 12V will be connected straight to ground, so a change has been implemented to connect these pins through a 100k resistor. 

