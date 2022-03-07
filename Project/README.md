## M2-EmbSys
# Module 2- Overview of embedded software, design,development processes and standards.

## REPORT:

## PROJECT TITLE: DISTANCE MEASUREMENT USING ULTRASONIC SENSOR “HC-SR04” WITH AVR MICROCONTROLLER.
## Submitted by: Sujata Naikar
## PS:99007669
---
## Table of content.
1. Abstract and Introduction.
1. Requirements.
     1. High level requirements.
     1. Low level requirements.
1. Components.
1. Block diagrams.
     1. Primary block diagram.
     1. Structural diagram.
     1. Flowchart.
     1. Sub-system.
     1. Sensors.
     1. Actuators.
1. Test plan and output.
1. Application.
1. References.
---
# 1.Abstract and Introduction.
## 1.1 ABSTRACT.
Nowadays, we have some difficulties in obtaining the distance that we want to measure. Even though, measuring tape is an easy option, but this kind of tool will have a limitation of manual error.. Before this, engineers have produced a range finder module but in the end, they find out the module have many disadvantages like limitation for distance, different result for different coloured obstacles, and need a calibration for every time before starts using it. Manual distance measuring is always done at the expense of human error. Precise and fix measurement of low range distance, is the main objective for this project. This device can measure distance in the range of 0.5m to 4m with the accuracy of1cm.This project is used to measure the distance by using ultrasonic sensors. It works by transmitting ultrasonic waves at 40 kHz. Then, the transducers will measure the amount of time taken for a pulse of sound travel to a particular surfaces and return as the reflected echo. After that, the circuit that have been programmed with AT mega microcontroller will calculate the distance based on the speed of sound at 25°C which an ambient temperature and also the time taken. The distance then will be display on a LCD module.

## 1.2 INTRODUCTION.

An ultrasonic sensor houses a transducer that emits high-frequency, inaudible acoustic waves in one direction when the transducer element vibrates. If the waves strike and bounce off an object, the transducer receives the echoed signal. The sensor then determines its distance from the object based on the length of time between the initial sound burst and the echo's return. Ultrasonic sensors require fairly accurate timing circuitry, so acoustic sensors really require a processor of some sort to drive them. Ultrasonic sensors should be a first choice for detecting clear objects, liquids, dense materials of any surface type (rough, smooth, shiny) and irregular shaped objects. This makes them one of the most ideal choices for measuring the height of containers which could be of different shapes, sizes, color and material. 
---

# 2.Requirements.
## There are mainly two types of requirements;
1. High level requirements.
2. Low level requirements.

* Though both the types of requirements are more or less depended on each other while functioning, according to the need and  usage they are termed as high and low level requirements.

## 2.1 High level requirements.
|   Id	   |          High level requirements.                              |
|----------|------------------------------------------------------------------|
|  HLR1	   | The system shall maintain the temperature in the required limit.|
|  HLR2	   | The system shall have control over alarm conditions.|
|  HLR3	   | The system shall be able to keep a track on compressor control.|

## 2.2 Low level requirements.
|     Id	   |     Low level requirements.  |
|------------|------------------------------|
|  LLR1.1(for HLR1)	| From initial power-on, the ambient air temperature of the fridge is typically around +21°C.|
|  LLR1.2(for HLR1)	| The user selected temperature is typically setaround +5°C, and may cycle between +8 and +2°C.|
|  LLR2.1(For HLR2)	| There are three possible alarm situations. These are, door open, over, or under temperature conditions.|
|  LLR2.2(For HLR2)	| If the door has inadvertently been opened for a pre-determined time, for example, one minute, an audible alarm will be sounded.|
|  LLR2.3(For HLR2)	| The over temperature situation can occur if the fridge door is not closed properly or there is compressor failure or a refrigerant pressure problem.|
|  LLR2.4(For HLR2)	| The under temperature case may occur if the compressor is permanently powered-on. In all of these situations the objective is to alert the user.|
|  LLR3.1(For HLR3)	| A conventional compressor control case, a more efficient and long-term cost-effective solution can be implemented using the microcontroller to control the compressor motor using a triac and a relay.|
|  LLR3.2(For HLR3)	| The purpose of this relay is to apply power to the compressor motor start and run windings at power-on.|
|  LLR3.3(For HLR3) | And also to maintain power to the motor run winding after the start-up phase has expired.|
---

# 3.Components
## The main components are,
* The compressor.
* The condensor.
* The expansion device.
* The evaporator.

•Compressor – It is a hermitically sealed reciprocating pump. It is the heart of the refrigeration system. It pumps refrigerant gas to the different components to effect the refrigeration cycle. Their sizes are from 1/12 horse power to 1 horse power. R-12 refrigerant gas is commonly used. Newer environmentally friendly refrigerant gas such as R-134a is being used for the newer models.

•Condenser –  It is made of serpentine copper tubes with aluminum fins. The combine heat of gas refrigerant from the evaporator and the heat of the compressed gas refrigerant from the compressor is being dissipated into the atmosphere, and changes the gas refrigerant into liquid refrigerant.

•Expansion Valve – copper capillary tube, or "expansion valve", is widely used on refrigeration appliances. Their outside diameter is 2.5mm, and their length is between 8 feet to 12 feet. High pressure liquid refrigerant leaves the capillary tube into low-pressure low-temperature liquid refrigerant.

•Evaporator – is a serpentine aluminum tubes with aluminum fins. It absorbs the heat in the freezing and refrigerating compartments and transfers it to the condenser. The low pressure liquid refrigerant turns to gas after absorbing the heat. And is ready to make its journey through the accumulator then to the compressor.

 ** Other components are;
 
•Filter/dryer – It filters the dirt and iron particles from the refrigerant. Some filter Dryer have moisture absorbent materials like, Silica gel or synthetic silicates, which removes moisture from the refrigerant. The filter/dryer protects the compressor by restricting and filtering the impurities and moisture contents in the refrigerant.

•Accumulator – is a refrigerant tank. It stores refrigerant so that the evaporator will not run out of it. Without an accumulator, the 2-door no-frost refrigerating unit will exhibit the symptom of refrigerant starvation.

•Refrigerator-Fan-motor – The fan motor of a 2-door no-frost is situated at the back of the evaporator coils, and it blows the air into the freezer-coils and distribute the air into the freezing and refrigerating compartments. The room area of the freezer is very much smaller than that of the refrigerator, therefore the temperature can be maintained at a few degrees below 0 Centigrade.

•Freezer-Fan-Motor – The fan motor of a freezer is used to cool the compressor. It is situated beside the compressor in the compressor room. It has a stand and steel bracket, and is bolted into a cross-member. The fan runs together with the compressor. Care should be taken not to bend the fan blade during maintenance. The aluminum blade can vibrate furiously and is detrimental to the shaft bearings and can cause early breakdown.

# 4. Block diagrams.
## 4.1 PRIMARY BLOCK DIAGRAM OF REFRIGERATOR.

![image](https://user-images.githubusercontent.com/46914341/155833529-939bfc4f-625e-40ab-b76e-a7f49086add7.png)
* Fig 4.1.1The above figure gives the overall idea about how the system is arranged in the form of block diagram.

![image](https://user-images.githubusercontent.com/46914341/155833285-d685d905-da01-494f-9d36-484a93cce4c3.png)
* Fig 4.1.2 The main focus in this design is to implement a system solution that will control a domestic fridge compressor based on temperature measurement, with some additional functionality.

## 4.2 Structural diagrams.

![image](https://user-images.githubusercontent.com/46914341/155833306-bdbd4f6f-871f-4109-bfae-1d999e5477de.png)

 ## 4.3 Flowcharts.
 
 ![image](https://user-images.githubusercontent.com/46914341/155833347-5c9ed3cf-711b-49ab-b1d0-822445a302fc.png)
* fig 4.3.1 Flowchart of the refrigerator function.

![image](https://user-images.githubusercontent.com/46914341/155833388-913212ee-578d-493e-8950-58343be805ab.png)
* Fig 4.3.2 Time base module interrupt module.

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

