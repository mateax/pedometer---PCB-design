# pedometer-PCB-design

PCB design and electrical schematic for step counter by EAGLE software

### Circuit

Components required: 
* Attiny85 IC
* MPU6050
* OLED Display Module
* 2× Push Buttons
* 5× 10KΩ Resistors (SMD)


### How it works?
This Arduino based step counter is powered by a 3V coin cell, making it easy to carry when you go out for a walk or jog.
The program in this project uses the MPU6050 to measure the magnitude of the acceleration along the 3 axis (X, Y, and Z). Then it calculates the difference of the acceleration magnitude between the previous and current values. If the difference is greater than a certain threshold (For walking greater than 6 and for running greater than 10), then it increases the step count accordingly. The total steps taken are then displayed on OLED Display.

### Circuit diagram
The schematic for the MPU6050 Step Counter is given below:

![schematic](https://github.com/mateax/pedometer-PCB-design/blob/main/step_counter%20-%20EAGLE%20files/Step_counter_Schematic.jpg)

The above image shows the circuit diagram for interfacing MPU6050 and OLED Display with Attiny85 IC. The interface between MPU6050, OLED Display, and Arduino must be implemented using I2C Protocol. Hence, the SCLPin (PB2) of the ATtiny85 is connected to the SCLPin of the MPU6050 and OLED Display respectively. Similarly, the SDAPin (PB0) of the ATtiny85 is connected to the SDAPin of the MPU6050 and OLED Display. Two pushbuttons are also connected to the PB3 & PB4 pin of ATtiny85 IC. These buttons can be used to scroll the text or change the text on display.

### 
### PCB - top layer
![top-layer-wires](https://github.com/mateax/pedometer-PCB-design/blob/main/PCB%20-%20final%20design/Wires_Top.PNG)
![top-layer-gnd](https://github.com/mateax/pedometer-PCB-design/blob/main/PCB%20-%20final%20design/GND_Top.PNG)

#### 
### PCB - bottom layer
![bottom-layer-wires](https://github.com/mateax/pedometer-PCB-design/blob/main/PCB%20-%20final%20design/Wires_Bottom.PNG)
![bottom-layer-gnd](https://github.com/mateax/pedometer-PCB-design/blob/main/PCB%20-%20final%20design/GND_Bottom.PNG)

####  
### 3D PCB view
![3D](https://github.com/mateax/pedometer-PCB-design/blob/main/PCB%20-%20final%20design/3D%20PCB.PNG)





