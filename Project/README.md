Project on refrigerator.

REPORT ON REFRIGERATOR :

Module 2- Overview of embedded software, design,development processes and standards.

Submitted by: Sujata Naikar
PS:99007669

Embedding a  Microcontroller into any domestic appliance has
numerous advantages, both through the development life cycle and
production environment. Such one example is a Refrigerator. Establishment of a common hardware and software development platform can be done which can further support a range  of appliances for present and potential future needs.

1.REQUIREMENTS

There are mainly two types of requirements, namely;
1.high level requirements.
2.low level requirements.
 Though both the types of requirements are more or less depended on each other while functioning, according to the need and   usage there are termed as high and low.

1.	High level requirements.

•	The  primary requirement is that within less amount  of time it should serve the purpose in cooling the things.
•	Maintaining  refrigerated foods at a low temperature which helps to slow the growth of microorganisms, so thus reduces the occurances of foodborne illness and also to retain the nutritional qualities of food.
 
2.	Low level requirements

•	Power consumption must be as less as possible.
•	The depth of the refrigerator should be more in order to place as many as items /things and more space for airflow.





2.Components

    	The main components are,
     
1.The compressor.

2.The condensor.

3.The expansion device.

4.The evaporator.

•	Compressor – It is a hermitically sealed reciprocating pump. It is the heart of the refrigeration system. It pumps refrigerant gas to the different components to effect the refrigeration cycle. Their sizes are from 1/12 horse power to 1 horse power. R-12 refrigerant gas is commonly used. Newer environmentally friendly refrigerant gas such as R-134a is being used for the newer models.

•	Condenser –  It is made of serpentine copper tubes with aluminum fins. The combine heat of gas refrigerant from the evaporator and the heat of the compressed gas refrigerant from the compressor is being dissipated into the atmosphere, and changes the gas refrigerant into liquid refrigerant.


•	Expansion Valve – copper capillary tube, or "expansion valve", is widely used on refrigeration appliances. Their outside diameter is 2.5mm, and their length is between 8 feet to 12 feet. High pressure liquid refrigerant leaves the capillary tube into low-pressure low-temperature liquid refrigerant.
•	Evaporator – is a serpentine aluminum tubes with aluminum fins. It absorbs the heat in the freezing and refrigerating compartments and transfers it to the condenser. The low pressure liquid refrigerant turns to gas after absorbing the heat. And is ready to make its journey through the accumulator then to the compressor.
 Other components are;
•	Filter/dryer – It filters the dirt and iron particles from the refrigerant. Some filter Dryer have moisture absorbent materials like, Silica gel or synthetic silicates, which removes moisture from the refrigerant. The filter/dryer protects the compressor by restricting and filtering the impurities and moisture contents in the refrigerant.

•	Accumulator – is a refrigerant tank. It stores refrigerant so that the evaporator will not run out of it. Without an accumulator, the 2-door no-frost refrigerating unit will exhibit the symptom of refrigerant starvation.


•	Refrigerator-Fan-motor – The fan motor of a 2-door no-frost is situated at the back of the evaporator coils, and it blows the air into the freezer-coils and distribute the air into the freezing and refrigerating compartments. The room area of the freezer is very much smaller than that of the refrigerator, therefore the temperature can be maintained at a few degrees below 0 Centigrade.

•	Freezer-Fan-Motor – The fan motor of a freezer is used to cool the compressor. It is situated beside the compressor in the compressor room. It has a stand and steel bracket, and is bolted into a cross-member. The fan runs together with the compressor. Care should be taken not to bend the fan blade during maintenance. The aluminum blade can vibrate furiously and is detrimental to the shaft bearings and can cause early breakdown.

3.There are various sensors used while designing the refrigerator.
Which includes,
•	Dual Sensor Control with Two Thermo Sensor Controls which enable to increase or decrease the temperature in Freezer & Fridge zone independently.
•	 A reed sensor or Hall effect sensor can be used to detect the door's position. For example, in refrigerators, a reed sensor is mounted to the frame of the appliance and a permanent magnet actuator is mounted to the door


4.Architecture

•	Design 

•	PRIMARY BLOCK DIAGRAM OF REFRIGERATOR
![image](https://user-images.githubusercontent.com/46914341/155455793-7c34ce98-d469-4c7d-b04c-2f281d5d825d.png)

.
 
The above figure gives the overall idea about how the system is arranged in the form of block diagram.
![image](https://user-images.githubusercontent.com/46914341/155571420-a32a04ad-53f7-44e3-b089-cbeb78e57fa4.png)


 
o	Embedded within a domestic Fridge compartment is an Evaporator, and
on the outside a Condenser, heat exchanging coils and the refrigerant
compressor. 
o	The compressor is driven by an electrical motor. 
When power is applied to the compressor the pressure of the refrigerant is
     increased. 
o	This increase in pressure causes an increase in refrigerant
temperature and the heat produced by this action is dissipated through
the heat exchanging coils at the rear of the appliance. 
This action is illustrated in the above diagram.
o	The refrigerant then condenses and passes through from the
high-pressure environment of the condenser through an expansion
valve to the low-pressure evaporation system inside the Fridge
compartment. 
o	On evaporating, the refrigerant absorbs heat and
subsequently reduces the enclosure temperature. 
o	The warmer refrigerant is circulated to the outside of the compartment where the cycle repeats under thermal control.
![image](https://user-images.githubusercontent.com/46914341/155571525-319d1565-7603-4bc9-a39f-5cc035aded26.png)

 
Fig 1.1
Schematic diagram of refrigerator.

![image](https://user-images.githubusercontent.com/46914341/155571604-aaa36a55-807b-4b63-96d8-cb3ceefa2c90.png)

 
Fig 1.2
Freezer system, includes main components of a refrigerator system.


Working of refrigerator:

The basic principle is that whenever a liquid coolant is passed through things at a higher temperature, it absorbs the heat; gets evaporated and the cooling effect is produced. The Refrigerator works on the principle of evaporation.

          i.e, When the temperature of the fridge compartment rises above the
          pre-selected thermostat setting, the bi-metallic contact closes and line
          voltage is applied to both the start and run windings simultaneously. The
start winding has a lower resistance than the run winding and provides
the initial current surge required to start the motor. This inrush of current
subsequently raises the temperature of the PTC and increases its
resistive property, which in turn reduces the current flow to the start
winding. At this point in time, the current through the start winding has
been minimised by the PTC, the current through the run winding is stable
and the motor continues to run. When the fridge compartment reaches
the desired temperature the thermostat contact opens, removing power
from the motor. When the compartment air temperature again rises, the
temperature control cycle repeats.


Testing

The purpose of testing,

1.Increases use-age life of the refrigerators.

2.Save money & save energy as well with using star rating product or CE certified components.

3.Provide faith in product.

4.Improve safety of the product.

5.Improve performance as well.

6.Provide safety to user


There are various methods of testing,such as;

1.Testing temperatures.

2.Cool-down test.

3. Stable running and power consumption test.



