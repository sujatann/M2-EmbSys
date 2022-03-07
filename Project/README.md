## M2-EmbSys
# Module 2- Overview of embedded software, design,development processes and standards.

## REPORT:

## PROJECT TITLE: DISTANCE MEASUREMENT USING ULTRASONIC SENSOR “HC-SR04”.
## Submitted by: Sujata Naikar
## PS:99007669
---
## Table of content.
1. Abstract and Introduction.
    1. 5W's & 1H and S.W.O.T analysis.
2. Requirements.
     1. High level requirements.
     1. Low level requirements.
3. Components.
4. Block diagrams.
     1. Block diagram.
     1. Structural diagram.
     1. Flowchart.
     1. Sensors.
     1. Actuators.
     1. Sub-system.
5. Test plan and output.
6. Application.
7. References.
---
# 1.Abstract and Introduction.
## 1.1 ABSTRACT.
Nowadays, we have some difficulties in obtaining the distance that we want to measure. Even though, measuring tape is an easy option, but this kind of tool will have a limitation of manual error.. Before this, engineers have produced a range finder module but in the end, they find out the module have many disadvantages like limitation for distance, different result for different coloured obstacles, and need a calibration for every time before starts using it. Manual distance measuring is always done at the expense of human error. Precise and fix measurement of low range distance, is the main objective for this project. This device can measure distance in the range of 0.5m to 4m with the accuracy of1cm.This project is used to measure the distance by using ultrasonic sensors. It works by transmitting ultrasonic waves at 40 kHz. Then, the transducers will measure the amount of time taken for a pulse of sound travel to a particular surfaces and return as the reflected echo. After that, the circuit that have been programmed with AT mega microcontroller will calculate the distance based on the speed of sound at 25°C which an ambient temperature and also the time taken. The distance then will be display on a LCD module.

## 1.2 INTRODUCTION.

Ultrasonic sensors are great tools to measure distance and detect objects without any actual contact with the physical world. It is used in several applications, like in measuring liquid level, checking proximity and even more popularly in automobiles to assist in self-parking or anti-collision systems.This is an efficient way to measure small distances precisely. In this project, we have used the HC-SR04 Ultrasonic Sensor with microcontroller or can also be interfaced with an arduino to determine the distance of an obstacle from the sensor. The basic principle of ultrasonic distance measurement is based on ECHO. When sound waves are transmitted in the environment then waves return back to the origin as ECHO after striking on the obstacle. 

## 5W's & 1H and S.W.O.T analysis.
![W AND HOW](https://user-images.githubusercontent.com/46914341/156984874-024b8089-f91e-4d01-85ba-58de657e0ee7.PNG)

![SA](https://user-images.githubusercontent.com/46914341/156991290-fe6edd1c-172b-450c-94d1-d88bd057d82d.PNG)
---

# 2.Requirements.
## There are mainly two types of requirements;
1. High level requirements.
2. Low level requirements.

* Though both the types of requirements are more or less depended on each other while functioning, according to the need and usage they are termed as high and low level requirements.

## 2.1 High level requirements.
|   Id	   |          High level requirements.                              |
|----------|------------------------------------------------------------------|
|  HLR1	   | The system shall be used to find precise and fix measurement of low range distance.|
|  HLR2	   | The system shall be able to measure a distance of any obstacle. |
|  HLR3	   | The system shall be able to operate at the range of 2cm-400cm with an accuracy of 3mm.  |

## 2.2 Low level requirements.
|     Id	   |     Low level requirements.  |
|------------|------------------------------|
|  LLR1.1(for HLR1)	| Ultrasonic sensors generate high frequency sound waves and evaluate the echo which is received back by the sensor.|
|  LLR1.2(for HLR1)	|  calculates the distance depending upon the time taken by the echo signal to travel back after reflecting from the desired target.|
|  LLR2.1(For HLR2)	|The size of the object should be of the order of wavelength of signal for it to be detected. So object should not be very small.|
|  LLR2.2(For HLR2)	| The object should be placed near the rotational axis of transmitter.At wider angles less reflection takes place.|
|  LLR2.3(For HLR2)	| The object should be a good reflecting surface.|
|  LLR3.1(For HLR3)	|Sensors calculate the time interval between sending the signal and receiving the echo to determine the distance to an objectin the particular range of distance.|
|  LLR3.2(For HLR3)	| Make sure about provided range of operation because above the range of the specification provided it might won't provide accurate values.|

---

# 3.Components
## The main components are,
* Arduino Uno.
* Ultrasonic sensor Module
* 16x2 LCD.
* Scale
* Bread board
* 5 volt battery
* Connecting wires

**Arduino Uno: Arduino is an open-source electronics platform based on easy-to-use hardware and software. Arduino boards are able to read inputs - light on a sensor, a finger on a button, or a Twitter message - and turn it into an output - activating a motor, turning on an LED, publishing something online.

**Ultrasonic sensor Module:(The ultrasonic Sensor is considered to be a digital sensor because the microcontroller reads a digital signal from it.)
There are many types of Arduino distance sensors, but in this project we have used the HC-SR04 to measure distance in range of 2cm-400cm with an accuracy of 3mm. The sensor module consists of an ultrasonic transmitter, receiver and control circuit. The working principle of ultrasonic sensor is as follows:

* High level signal is sent for 10us using Trigger.
* The module sends eight 40 KHz signals automatically, and then detects whether pulse is received or not.
* If the signal is received, then it is through high level. The time of high duration is the time gap between sending and receiving the signal.

**LCD(Actuator):This display offers a way to interface your microcontroller to the outside world. It's one of the main output devices in your kit.


# 4. Block diagrams.
## 4.1 BLOCK DIAGRAM..

![BD](https://user-images.githubusercontent.com/46914341/157050047-47e2be8e-0b47-4b21-8979-0de5bd0cc812.PNG)
* Fig 4.1.1The above figure gives the overall idea about how the system is arranged in the form of block diagram.

![hardware](https://user-images.githubusercontent.com/46914341/157051582-0da52b17-d95a-4235-984d-caaa258a8eb4.png)
* Fig 4.1.2The above figure shows hoe the each of the components are connected to each other.

## 4.2 Structural diagrams.

![flow](https://user-images.githubusercontent.com/46914341/157058453-d177ddd8-4a13-4ec6-b71f-e8ebecfd571f.PNG)
* Fig 4.1.3The above figure also explains about how the blocks are arranged with respect to each other.

Block diagram of the working principle of an ultrasonic radar As shown in the above Fig, Arduino UNO receives power supply from the computer. Then microcontroller sends signals to the other two components: the ultrasonic sensor and servo motor. The feedback from these components is sent back to the microcontroller. The ultrasonic sensor has a transmitter to send out the ultrasound and a receiver to catch the reflected sound waves. The total travelling time of this sound wave is the distance.


 ## 4.3 Flowcharts.
 
 ![flowchart](https://user-images.githubusercontent.com/46914341/157056917-ce29cf9e-ab7d-4947-b2a2-a697c4cf2afa.PNG)
* fig 4.3.1 Flowchart of the Distance measurement meter.

## 4.4 Sub-systems.
![image](https://user-images.githubusercontent.com/46914341/155833448-65e5fb9d-ef14-4d44-973b-02762063ae7b.png)
* Fig 4.4.1 Schematic diagram of refrigerator.

![image](https://user-images.githubusercontent.com/46914341/155833695-7cda74e6-cd24-456a-8adc-8fbba0e308c3.png)
* Fig 4.4.2 Freezer system, includes main components of a refrigerator system.


## Explaination to the block diagram.

• Embedded within a domestic Fridge compartment is an Evaporator, and on the outside a Condenser, heat exchanging coils and the refrigerant compressor. 

• The compressor is driven by an electrical motor. When power is applied to the compressor the pressure of the refrigerant is increased. 

• This increase in pressure causes an increase in refrigerant temperature and the heat produced by this action is dissipated through the heat exchanging coils at the rear of the appliance. 

• The refrigerant then condenses and passes through from the high-pressure environment of the condenser through an expansion valve to the low-pressure evaporation system inside the Fridge compartment.

• On evaporating, the refrigerant absorbs heat and subsequently reduces the enclosure temperature.

• The warmer refrigerant is circulated to the outside of the compartment where the cycle repeats under thermal control.

## 4.5 Sensors.
1. Dual Sensor.
 
Dual sensor Control with Two Thermo Sensor Controls which enable to increase or decrease the temperature in Freezer & Fridge zone independently.

2. A reed sensor or Hall effect sensor.

It can  can be used to detect the door's position. For example, in refrigerators, a reed sensor is mounted to the frame of the appliance and a permanent magnet actuator is mounted to the door

## 4.6 Actuators.

1. Compressor power relay.

The purpose of this relay is to apply power to the compressor motor start and run windings at power-on, and maintain power to the motor run winding after the start-up phase has expired. Additionally, as the relay contact has a low resistance, it does not dissipate power unnecessarily under normal running conditions.

2. A thermostatic actuator .

It acts as a valve actuator to open or close a valve based on a temperature setpoint to. i.e The regulating system, consists of thermostatic valve means for controlling the flow of refrigerant to the evaporator having an actuator chamber filled with a refrigerant medium having liquid an vapor phases, and electrical heat supply element in the actuator chamber.
## Working of refrigerator:

* The basic principle is that whenever a liquid coolant is passed through things at a higher temperature, it absorbs the heat; gets evaporated and the cooling effect is produced. The Refrigerator works on the principle of evaporation.

 i.e, When the temperature of the fridge compartment rises above the pre-selected thermostat setting, the bi-metallic contact closes and line voltage is applied to both the start and run windings simultaneously. The start winding has a lower resistance than the run winding and provide the initial current surge required to start the motor. This inrush of current subsequently raises the temperature of the PTC and increases its resistive property, which in turn reduces the current flow to the start winding. At this point in time, the current through the start winding has been minimised by the PTC, the current through the run winding is stable and the motor continues to run. When the fridge compartment reaches the desired temperature the thermostat contact opens, removing power from the motor. When the compartment air temperature again rises, the temperature control cycle repeats.

# 5.Test plan and output.
• Testing

## The purpose of testing,
1. Increases use-age life of the refrigerators.
	
2. Save money & save energy as well with using star rating product or certified components.
	
3. Provide faith in product.
 
4. Improve safety of the product.
 
5. Improve performance as well.

6. Provide safety to user.

** There are various methods of testing,such as;

1. Testing temperatures.

2. Cool-down test.

3. Stable running and power consumption test.


# 6.Applications:

## Applications of Refrigeration in 7 Different Industries
I.	District Cooling.

II.	Electricity Production.

III.	Chemical and Petrochemicals.

IV.	Pharmaceutical.

V.	Food & Beverages.

VI.	Data Centres.

VII.	Other industries.

# 7.REFERENCES.
1. The information is referred from some papers and from browser.
2. Idea of block diagram is taken from available sources. 

