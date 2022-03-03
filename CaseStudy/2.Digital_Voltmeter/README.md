Simple case study on Digital Voltmeter.

# Module 2- Overview of embedded software, design,development processes and standards.

## Casestudy 2, ON DIGITAL VOLTMETER:
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
1. Application.
1. References. 
---


# 1.Abstract and Introduction.
## 1.1 ABSTRACT.
* The simple digital voltmeter is made of the ATMEL 8-bit MCU(Main Computational Unit), AT89S52 and national semiconductor's ADC(Analog-to-Digital Converter) 0804, including a certain number of components. The system uses the AT89S52 MCU as the main controller, which processes the acquired analog voltage and realize LED(light-emitting diode) digital display by dynamic scanning. The voltmeter can measure the DC(direct current) voltage in the rage of 0 ∼ 5V and display the measurement results by the four LED digital tube. Because of fewer components, low cost, automated adjustment, high accuracy measurement, stable performance, the voltmeter has a very good application prospect.
## 1.2 INTRODUCTION.
* In the measurement of voltage, current and frequency are the three most basic quantity measured, the voltage measurement is most frequent. With the development of electronic technology, High-precision voltage measurement is needed more as a necessary measure instrument. Digital voltmeter which is called DVM for short is a electronic measuring instrument the which converses the analog signal into discrete digital form and display.

                                    At present, the digital voltmeter composed of a variety of A/D converter has been widely used in electronic and electrical measurement, industrial automation instrument, automatic test system and other fields, showing a strong vitality. 


---

# 2.Requirements.
## There are mainly two types of requirements;
1. High level requirements.
2. Low level requirements.

* Though both the types of requirements are more or less depended on each other while functioning, according to the need and  usage they are termed as high and low level requirements.

## 2.1 High level requirements.
|   Id	   |          High level requirements.                              |
|----------|------------------------------------------------------------------|
|  HLR1	   | The system shall help in performing High-precision voltage measurement.|
|  HLR2	   | The system shall be able to converses the analog signal into discrete digital form and display|
|  HLR3	   | The system shall provide accurate readings, small error, high sensitivity, high resolution, and fast measurement speed.|

## 2.2 Low level requirements.
|     Id	   |     Low level requirements.  |
|------------|------------------------------|
|  LLR1.1(for HLR1)	| The on-chip Flash allows the program memory in system programmable, also suitable for conventional programming which helps to give precise values.|
|  LLR2.1(For HLR2)	| A/D converter is a device converting the analog voltage or current into digital content, and is a interface between a simulation system and computer.|
|  LLR2.2(For HLR2)	| In the data acquisition and control system, A/D converters have been widely used. Successive approximation type A/D converter is composed of a comparator, A/D converter, the memory and control circuit.|
|  LLR3.1(For HLR3)	| Only if the current is large enough, the display can work properly.|
|  LLR3.2(For HLR3)	| Display program is used to display the voltage in digital form which shows the accurate readings, small errors produced are taken care with high sensitivity and gives high resolution.|

---

# 3.Components
## The main components are,

  AT89S52 single-chip system, A/D system, LED display system, clock circuit, reset circuit and voltage measurement input circuit. 
 
 * AT89S52 single-chip system: The AT89S52 is a low power, high performance CMOS 8 bit microcontroller, with 8K in system programmable Flash memory. Using Atmel's high density non-volatile memory technology manufacturing, fully compatible with 80C51 products and industrial orders and pin. The on-chip Flash allows the program memory in system programmable, also suitable for conventional programming. In a single chip, with smart 8 bit CPU and in-system programmable Flash, such that AT89S52 is widely used in many embedded control applications.
 
 * A/D system: The analog to digital conversion is achieved through the A/D converter. A/D converter is a device converting the analog voltage or current into digital content, and is a interface between a simulation system and computer. In the data acquisition and control system, A/D converters have been widely used. Successive approximation type A/D converter is composed of a comparator, A/D converter, the memory and control circuit. It uses the internal registerto test comparison from high to low.
 
 * LED display system: LED has been widely used because of the advantages of simple structure, low price, and convenient and MCU interface. LED display is composed of a plurality of light emitting diode display device field display. In single-chip microcomputer seven digital display is the mostly used. 
 
 * Reset circuit and Clock circuit: The reset circuit usually adopts automatic power-on reset and reset button in two ways. For the sake of convenience, the design is a power-on reset circuit.SCM each functional unit operation clock control signal for the benchmark, everything in good order and well arranged. Therefore, the clock frequency directly affect the speed of MCU, clock circuit quality also directly affects the stability of single chip microcomputer system. The clock circuit used in two ways, one is the internal clock mode, another is the external clock mode. This system uses the internal clock mode, using the high gain of the inverting amplifier chip internal, the external circuit is simple, requiring only a crystal and 2 capacitors.

 * Voltage measurement input circuit: A digital voltmeter (DVM) measures an unknown input voltage by converting the voltage to a digital value and then displays the voltage in numeric form. DVMs are usually designed around a special type of analog-to-digital converter called an integrating converter.
 

# 4. Block diagrams.
## 4.1 PRIMARY BLOCK DIAGRAM OF DIGITAL VOLTMETER.

![image](https://user-images.githubusercontent.com/46914341/156607250-11cbd096-e008-4b3d-a4fa-0d8a80f8c837.png)
* Fig 4.1.1The above figure gives the overall idea about how the system is arranged in the form of block diagram.

## 4.2 Structural diagrams.

![image](https://user-images.githubusercontent.com/46914341/156607535-a5d3c1d7-a9fe-4250-9649-0cd264b8ddbf.png)

 ## 4.3 Flowcharts.
 
 ![image](https://user-images.githubusercontent.com/46914341/156607610-4a9a23a4-1d8c-47b3-8225-20f1ef2b0635.png)
* fig 4.3.1 Flowchart of the main part of the system.

 Based on the principle of modular program, the program is divided the initialization module, A/D conversion and display program, the three program modules of the main program software of the system.

![image](https://user-images.githubusercontent.com/46914341/156607757-1b35daee-343b-42f8-8a2e-71929e51315d.png)
* Fig 4.3.2 Flow chart of ADC conversion.

 Two key in program design is simulation of voltage and display code convert.
 Calculation formula of the analog voltage value can be calculated by the voltage V -- the calculated values; D 8 digit A/D converter output. In programming, if A/D conversion result is multiplied by 0.0196, the result is a decimal number, in the computer called a floating point number. On 8 bit MCU, do not have floating-point operation ability, if t calculating a floating point number is necessary, a lot of memory unit and MCU CPU time will be occupied. 


## Working of Digital Voltmeter:

Digital Voltmeter displays the voltage readings of a circuit numerically. Initially analog voltmeters were used to take the readings of the voltage where in a pointer or indicator moves across a scale in proportion to the voltage of the circuit and later, digital voltmeters were introduced which gives the numerical display of voltage with accuracy.

Working Principle of Voltmeter:

The main principle of voltmeter is that it must be connected in parallel in which we want to measure the voltage. Parallel connection is used because a voltmeter is constructed in such a way that it has a very high value of resistance. So if that high resistance is connected in series than the current flow will be almost zero which means the circuit has become open.

Digital Voltmeter abbreviated as DVM is an instrument used to measure the electrical potential difference between two points in a circuit. The voltage could be an alternating current (AC) or direct current (DC). It measures the input voltage after converting the analog voltage to digital voltage and displays it in number format using a convertor. The usage of digital voltmeter has increased the speed and accuracy with which the readings are noted


# 5.Applications:

## Applications of Digital Voltmeter.
* Digital Voltmeter is used to know the actual voltage of different components.
* DVM is widely used to check if there is power in the circuit, such as mains outlet.
* Knowing the voltage across a circuit, current can be calculated.

# 6.REFERENCES.

1. The information is referred from some papers and from browser.
2. Idea of block diagram is taken from available sources. 

