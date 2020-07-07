# Zephyros
Multidisciplinary independent project prototype for oxygen generation, medical artificial breathers, PLC, Machine Learning and cloud services. <br />
We update this project after finishing private testing and results.
This is under non-working time in our free time.

![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Zephyros_explanation.JPG?raw=true)

## Team <br />
Mechanical-Electrical Engineering and Render design <br />
Abel Geovanny Loera – Linkedin – https://www.linkedin.com/in/abel-geovanny-loera-navarro-a63542123 <br /><br />

Process engineering, Data Science, Data Engineer, Data Architect and Project Management<br />
Brandon F. Loera – Linkedin – https://www.linkedin.com/in/brandon-f-loera-ba519ab7 <br /> <br />

Medicine <br />
María Jacqueline Martínez – jacquelinemtz_84@Outlook.es <br /> <br />

Legal <br />
Hannia Loera – Linkedin - https://www.linkedin.com/in/hannia-melisa-loera-garcia-2a6779171 <br /> <br />

Diffusion – Marketing – MedMark <br />
Perla Elianne Garza – Linkedin – https://www.linkedin.com/in/perla-elianne-garza-17361a15a <br /> <br />

Collaborators <br />
Abel Loera – Linkedin – https://www.linkedin.com/in/abel-loera-54841050 <br />
Feliciano Loera – Linkedin – https://www.linkedin.com/in/feliciano-loera-18232054 <br /> <br />

Document control versions <br />

|Version|Date|
|:---:|:---:|
|1|27th March of 2020|
|2|29th March of 2020|
|3|1st April of 2020|
|4|3rd April of 2020|
|5|6th April of 2020|

<br />

# Introduction and scope
Currently the Covid-19 pandemic has become an "enemy of humanity"<sup>1</sup> according to the World Health Organization. <br />
Given this situation, we have seen that the main public health problem is in the number of artificial respirators and masks available<sup>2</sup>. <br />
So we decided to work on finding a solution and develop a prototype that can be done by personal and industrial approach.<br />
As part of the good practices to be able to solve a problem, we must first identify the main parameters to be controlled. 
With this in mind we made an investigation on this topic. See Annex A. <br />
Based on our research, the factors to control are: <br />
•	Oxygen concentration. <br />
•	Total volume of air flow. <br />
•	Respiratory rate per minute. <br />
•	Oxygen pressure. <br /> <br />
The first point involves a process of production of oxygen at a certain concentration and its regulation by valves; <br />
the last three points imply mechanical-electrical development. <br /><br />
On the other hand, to build the solution we must take seven main points in the design of the solution: <br />
1.	It must be built with common materials and access to industrial production lines. <br />
2.	Meet medical specifications. <br />
3.	Insurance. <br />
4.	It can be decontaminated, cleaned and reused. <br />
5.	Lower monetary cost compared to a common breathing system. <br />
6.	It's easy to build, maintain and upgrade. <br />
7.	Scalable in improvements. <br /><br />

With all the above in mind, we present you our proposal consisting of: <br />
1.	Oxygen concentrator. <br />
2.	Mechanical-electric respirator. (Design, motor, valves, Arduino and accessories, sensors and control system). <br />
3.	Mask. <br /><br />

Important:
The oxygen concentrator showed does not produce 99% concentrated oxygen and does not generate enough pressure to fill medical oxygen tanks. <br />
If you want to increase concentration and pressure you need more expensive materials and equipment. <br />
By using air filters, we removed much of the impurities in form of powder or particles suspended so the oxygen concentrated can be breathed without complications. <br />
The electric mechanical respirator can be printed with a 3-D printer or produced in parts at an industrial level by cutting material. <br />
The mask can be printed with a 3-D printer or you can create it by hand. <br />
This solution must only be used in mild to moderate cases when there is a partial substitution of the respiratory capacity, which means no intubation or entering systems to the trachea- lungs. <br />
The most severe cases require specialized machinery since sometimes there must be up to 99% oxygen concentration. <br />
For the replacement of the total respiratory capacity at the mechanical-electrical respirator level, we are working on a software update and new sensor connections-components to the Arduino, however, due to issues of time, budget and obtaining parts we have some delays. <br />
This document is under continuous modification. Please see "notice" section for more legal advertising. <br /><br />

## Conceptual diagram of the solution

 ![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Zephyros_solution.JPG?raw=true)

Note: The order of the sections “air compressor” and “water and CO2 elimination” inside the oxygen concentrator depends of the kind of compressor that you use.

## Oxygen concentrator
Given the current pandemic, in our country (Mexico) it is very likely that certain localities will be left without a concentrated oxygen supply for their patients, so we decided to show a concentrated oxygen production process in the simplest possible way. <br />
There are many procedures to obtain oxygen, however, in order to select a procedure we must take into account the following points: <br />
•	It must be built with common materials. <br />
•	It must be safe. <br />
•	Cheap. <br />
•	Simple to operate. <br />
•	Sufficient oxygen production. <br /><br />
Within these procedures we found two procedures as possible candidates to develop, the first is a process based on gas pressures and absorbent material (PSA) and the second based on electrolysis. <br />
Electrolysis, without the appropriate materials, is costly at the electrical energy level, produces little oxygen and is quite unsafe since it generates gaseous hydrogen <sup>3</sup> and it is highly flammable and in appropriate conditions is explosive <sup>4</sup>. <br />
Therefore we select the pressure process called PSA. <br />
Note: See Annex B for the theory behind the PSA. <br />

## Conceptual design oxygen concentrator
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Oxygen_concentrator.png?raw=true)<br /><br />

Where: <br />
1.	Eliminator of water (H2O) and carbon dioxide (CO2). 3 inches in diameter by 12 inches. <br />
2.	Transparent hose. <br />
3.	Compressor. <br />
4.	Compressor hose. <br />
5.	Coil and insulated container with lid filled with cold water. Minimum 5 revolutions. <br />
6.	Air filter. <br />
7.	Air filter-CPVC connector. <br />
8.	Ball valve (on- off) 1/2 inch. <br />
9.	1/2 inch flow valve. <br />
10.	Purge system. <br />
11.	Absorbers. <br />
12.	Pressure gauges (manometers) of 150 psi, except for 12.4, which must be 100 psi. <br />
13.	Oxygen container. You can use a larger container than the one presented in this document but the pressure should not exceed 80 psi unless you use a professional oxygen cylinder and a compressor. <br /><br />
Adjuncts. <br />
A.	Wood or plywood board ½ inch thick. <br />
B.	Metal lugs/handles with screw, nut and washers. <br />
C.	Union nut. Allows the replacement of accessories in case of damage. <br />
D.	Steel mesh. <br />
	D.1 Two steel meshes per adsorbed. One upper and one lower. <br />
	D.2 Two steel meshes per water and carbon dioxide remover. One upper and one lower. <br /><br />
Notes: Name the valves, absorbers, etc; as seen in the diagram. <br />
Mark valve positions when closed, this will help you for control and inspection during the process. <br />
Depending on your type of compressor, it is likely that the water and carbon dioxide eliminator (1) and the compressor (3) change positions. <br />
Whatever the case, these two parts must always be present continuously. <br />
You can connect a compressor to the Val –F - 08 valve tubing outlet to compress oxygen and fill medical oxygen tanks. <br />

## Process indication
According to the theory we will be working at pressures between 45 and 115 psi (4 to 8 bar) maximum. The air around us is at 14.7 psi, therefore we will be working with pressures higher than atmospheric. <br />
It seems to be dangerous but the water you have in your house is between 40 and 80 psi maximum, so we will be working at relatively similar pressures but with gases<sup>5</sup>. <br />
Another factor to consider is the temperatures of the process and the environment around you, however, the temperature range of planet Earth on its surface ranges from -85 ° C (-117.4 ° F) to almost 60 ° C (140 ° F)<sup>6</sup> . <br />
And for the process, we will be working under the shade at a temperature similar to 25 ° C (77 ° F), however, the temperature of your home and region may be different from ours.
Note: See Annex C for the safety data sheets of the chemical products involved in the process. <br /><br />
Table 1. - Process production by type of absorber diameter. Oxygen produced between 60 - 80% concentrations with zeolite<sup>7</sup>. <br />
|Selected Diameter (inch)|Length (inch)|Liters of oxygen / minute|Kg of zeolite|Bucket or container of cold water (gallons)|Maximum tolerable pressure (PSI) 40|Maximum tolerable pressure (PSI) 80|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|8|33|27.2|40|30.00|160.00|250.00|
|6|33|20.4|30|22.50|180.00|280.00|
|4|33|13.6|20|15.00|220.00|320.00|
|3|33|10.2|15|11.25|260.00|370.00|
<br />
Note: Table 1 shows the "selected diameter" column which is the diameter of the absorbers. The calculations are approximate theoretical. <br />
The amount of liters of oxygen depends on the flow or flow of the compressor you use. <br />
For a selected diameter of eight inches with that amount of liters of oxygen and a compressor 6 Hp compressed air flow 9 SCFM (262 L / min). <br /><br />
 
Important:
This process does not generate oxygen at high pressures (150 psi onwards).<br />
A common oxygen tank has a pressure of approximately 600 psi and is made of industrial steel with ASTM standard specification<sup>8</sup>].<br />
Never leave the oxygen concentrator in the sun or near heat sources.<br />
It should not be near the reach of children.<br />
See Annex D for further indications on the proper use of oxygen.<br />

## Selection of the material
To make the oxygen concentrator we selected CPVC since its maximum operating pressure<sup>9</sup> allows us to carry out the process, it is easy to find and it is less expensive than other materials. <br />
Regarding the environment, its absorption capacity of POPs pollutants is lower than other polymers such as: HDPE, LDPE and PP<sup>10</sup> which implies a significant reduction in pollutants accumulation inside the food chain once the materials are discarded and taken away as garbage, however, we strongly encourage a recycling attitude. <br /><br />
Another important point to mention about CPVC is its degradation. <br />
Degradation can be mad by biological entities like fungi "Aspergillus fumigatus", "Phanerochaete chrysosporium", "Lentinus tigrinus", "Aspergillus niger" and "Aspergillus sydowii" which consume the CPVC<sup>11</sup>. On the other hand, if CPVC is burned it will generate compounds like dioxins<sup>12</sup> which are harmful to the human body due to the chemical compound “vinyl chloride” which is a known carcinogen<sup>13</sup>. <br />
For all of the above, we recommend to use stainless steel if you have the appropriate budget. <br /><br />
Table 2. - Maximum pressure of the CPVC according to the internal diameter. <br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/CPVC_Operational_properties.jpg?raw=true)<br />

However, it is also necessary to consider how does the temperature affects the material, in the case of CPVC it is a thermoplastic, which means heat affects the pressure that the material can withstand and heat is closely related with temperature. <br />
Thus, the relationship between the pressure which the material can withstand and the temperature of the process/environment can be seen within the following table<sup>14</sup>: <br /><br />
Table 3. - Stratus factor according to temperature for different thermoplastics.<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/CPVC_temperature_properties.jpg?raw=true)<br />

By using the values of table 3 you can calculate the maximum operating pressure based on the temperature of the place where you live.<br />
For example, we selected 3-inch tubes for absorption, elimination of H2O- CO2, and pipeline which will function as an oxygen container, all or using the Model 80 CPVC; the maximum temperature of our region is 45 °C (113 °F), therefore the CPVC can withstand a maximum pressure of: <br />
370 psi * 0. 8 = 296 psi <br />
Therefore, we recommend that if you want to produce large amounts of oxygen using a larger diameter to 8 inches then change for another material such as stainless steel, this also means that you must change the valves, connecting tubes, elbows and T-type connectors, among other components. <br /><br />

## List of materials
1 air compressor. 
It must be less or equal to 6 HP and with a flow capacity less or equal to 9 SCFM since this power and flow would be for a tube equal or greater than 8 inches in diameter. However, if you have a compressor with these characteristics then use it.
Optional: 1 refrigerator tank for the compressor.
 
CPVC. (Yellow color).
2 tubes. They can be of type 40 or 80. For both tubes, the same diameter. Use table 1. <br />
1 tube 1 1/2 inch in diameter and 4 inches long. Purge / waste. <br />
1 tube 3 inches in diameter and 12 inches long. Water and CO2. Eliminator. <br />
1 tube 6 inches in diameter and 60 inches long. (Container for oxygen). Capacity of 27.8 L. <br />
9 1/2 inch T-type connectors. <br />
5 for pipe joints and 4 for manometers. <br />
  Way of union with the manometers ->  <br />
  ![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Manometer_union.jpg?raw=true)<br />
5 1/2 inch elbow connector. <br />
8 1/2 inch ball-type valves. <br />
1 1/2 inch pressure regulating valve. <br />
5 Nut-union. <br />
Tube-cpvc male-female adapters. <br />
3 meters tube 1 /2 inch in diameter to make connections. <br />
Diameter reductors. <br />
1 CPVC - Serpentine connector. <br />
2 CPVC caps of the selected diameter for absorbers. <br />
Bite union hose. <br />
1 Teflon tape or paste. <br />
3 manometers with measurement capacity up to 150 psi. <br />
1 manometer with measurement capacity up to 30 psi. <br />
1 meter of transparent hose to connect to the compressor inlet (the diameter depends on your compressor). <br />
1 container for cold water and the size must be according to the diameter selected in table 1. <br />
1 steel / aluminum serpentine. <br />
1 bag of ice to cool. <br />
4 round steel net that can be inserted into tubes with the selected diameter. <br />
2 net round steel 3 inches.
Note: Steel nets must have pores that are smaller in size than the absorbent to be used. <br />
1 can of clear CPVC cement that allows pressures between 180 and 250 psi. <br /> 
Cooler. <br />
 
Absorbents. <br />
CMS (Carbon Molecular Sieve), activated carbon or Zeolite type 5A (if any). <br />
The latter can be bought from silica producers or agriculture providers. See table 1 for the specific weight you need inside the absorber and to that amount add 5 kg of absorbent. If you're going to produce your own activated carbon then multiply that amount by 1.3. For more information regarding absorbents see annex B. <br />
2 air filters between 4 and 0.01 microns. <br /><br />

## Assembly
Work below shade and in a ventilated place. Use the conceptual diagram to guide you through the design. <br />
The tubes of the selected diameter and the H2O - CO2 eliminator must have a lower net before ending step 8 inside section “Preparation of absorbents” and at the end of “Preparation of absorbents” you must add the other net. <br />
Label the valves and other sections as in the conceptual diagram. <br />
Clean each of the sections and parts very well before assembling it. The parts must be clean and dry. <br />
Wash your hands continuously when you go to assemble the equipment. <br />
Do not wash or get wet the absorbent, doing this could cause a decreasing effect in effectiveness. <br />

## Absorbent preparation
IF you use CMS or specialized activated carbon for gas separation then go to step 6 of the procedure in this section else you will need to prepare your own adsorbent. <br />
In our case we use zeolite, which is very common to use in aquariums. If you want to use activated carbon then see the procedure to follow in the following link: https://www.wikihow.com/Make-Activated-Charcoal <br />
For this we buy the necessary kg of zeolite according to the amount of oxygen we want to produce by a factor of 1.3 at the required weight (see table 1). <br /><br />
Materials. <br />
•	Absorbent. <br />
•	1 Mortar with pylon (in Mexico you can use a molcajete) or ball mill. <br />
•	1 steel container with lid (steel pot). <br />
•	1 Gas stove or some heat source. <br />
•	1 industrial mask with a 1 micron filter. <br /><br />

Process <br />
1.	Grind the absorbent by using the mortar and pylon until the size of the stones are less than half centimeter. <br />
Note: In case you want to do this step with a ball mill you will need: <br />
•	1 steel container with lid (can be a clean 1L can of paint).<br />
•	40 1-inch steel pellets. <br />
•	Rotary motor. <br />
•	Support for the steel container and the motor. <br /> <br />

Arrange the pieces as seen in the following image. <br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Homemade_ball_mill.png?raw=true)<br />

Image 1.- Homemade ball mill.<br />

Where: <br />
1.	Steel container with lid. <br />
2.	Axis of rotation. <br />
3.	Motor. <br />
4.	Floor of your house. <br /><br />
Process: <br />
1.1. Fill the container without a lid to 1/3 of its capacity, evenly distributing the pellets and the absorbent. <br />
1.2. Cover the container. <br />
1.3. Activate the motor so that it begins to rotate until you are able to hear blows inside the container then you must maintain that speed. <br />
1.4. Stop the motor every 5 minutes to inspect the size of the stone. <br />
1.5. If the rocks are smaller than half a centimeter, the process ends, otherwise go back to step 1.4. <br />
2.	Separate the dust from the rock, there should be only rocks. For this you can use a mesh and move it laterally so all the dust going to the ground. <br />
3.	Put the rocks into the steel pot with dust-free lid. <br />
4.	Heat for at least half an hour at maximum power until you start seeing steam. <br />
5.	If after that minimum time you do not see steam, then turn off the stove and let it cool, you can use water to cool as long as the lid is tightly closed and only wet the exterior part of the steel pot. <br />
6.	Insert the rocks into the absorbers and cover them with the corresponding caps according to their CPVC diameter. <br />
7.	Repeat the procedure until the absorber 1, 2 and disposer of H2O - CO2 are 90% capacity. <br />
8.	Put the upper net for each absorber. <br />
9.	Repeat steps 6, 7, and 8 for the H2O / CO2 eliminator. <br />
10.	Bond all other missing sections with CPVC cement. <br /> <br />

## Oxygen concentrator process
Security procedure. <br />
Note: No pressure gauge should exceed 130 psi, if any exceed that pressure then the process must be aborted.<br /><br />
Follow these instructions for abortion scheme:<br />
I.	Turn off the compressor. <br />
II.	Close all valves. <br />
III.	Open Val-B-03, Val-B-01, Val-B-05 and Val-B-07 valves in that order for 100 seconds and at the end of that time the Val-B-03 valve must be closed. <br />
IV.	Open Val-B-04, Val-B-06 and Val-B-02 valves for 100 seconds and at the end of time the valve Val-B-04 must be closed. <br /><br />
 
Operating procedure.<br />
1.	Make sure that all valves are closed.<br />
2.	Make sure that pressure gauge 3 has a pressure lower than 80 psi, if it is greater than or equal to 80 psi, stop the process.<br />
3.	Open valve Val-B-01.<br />
4.	Turn on the compressor.<br />
5.	Observe gauge 1 and wait until the pressure is 100 psi.<br />
6.	When the pressure is 100 psi, close Val-B-01 and turn off the compressor.<br />
7.	Wait 120 seconds.<br />
8.	First open Val-B-07 and immediately afterwards Val-B-05 valve.<br />
9.	When pressure gauge 1 is 50 psi close valve Val-B-07 and Val-B-05.<br />
10.	If the pressure of pressure gauge 3 is equal to or greater than 80 psi, the process ends, otherwise continues.<br />
11.	Open valve Val-B-03.<br />
12.	Open valve Val-B-02.<br />
13.	Turn on the compressor.<br />
14.	Close Val-B-03 valve when pressure gauge 1 is 20 psi.<br />
15.	Observe gauge 2 and wait until the pressure is 100 psi.<br />
16.	When the pressure is 100 psi, close Val-B-02 and turn off the compressor.<br />
17.	Wait 120 seconds.<br />
18.	First open Val-B-07 and immediately after Val-B-06 valve.<br />
19.	When the pressure of manometer 2 is 50 psi, close valve Val-B-07 and Val-B-06.<br />
20.	Open valve Val-B-04.<br />
21.	Open valve Val-B-01.<br />
22.	Turn on the compressor.<br />
23.	Close Val-B-04 valve when pressure gauge 2 is 20 psi.<br />
24.	If the pressure of pressure gauge 3 is greater than or equal to 80 psi, the process ends, otherwise it returns to point 5. <br /><br />
Important:<br />
Constantly check the pressure on gauge 3. If the pressure is below 30 psi you will have to repeat the process.<br />
If you use CMS then the oxygen will come out of the purge/waste section, therefore, you will have to adapt the process to follow.<br />
Pressure losses through the pipe are minimal due to the size of the prototype.<br />
You can automate the process using check valves, versa valves, etc. and connecting those with Arduino or you can automate it with pneumatic valves and timers.<br />
The Val-F-08 valve and manometer 4 allow to control the concentrated oxygen flow and measure the necessary pressure towards the mechanical-electric respirator respectively.<br /><br />

## Conclusion oxygen concentrator

With all the aforementioned specifications and following each of these steps correctly you will have the ability to generate oxygen at a certain concentration in case of oxygen tanks shortage.<br />
It is important to emphasize that the amount of oxygen produced depends on the air flow of your compressor since the filling times depend on it.<br />
Do not work above the guidelines pressures, if you do, it will be at your own risk.<br />
Seal each part very well to each other, if any part breaks, you can replace it using CPVC material.<br />
You can increase the amount of production by creating more hubs.<br />
If you want to produce large quantities of oxygen, you will need to change the material to steel tubes and you will need a change to other materials from CPVC to steel equivalent.<br />
The support of the oxygen concentrator is essential, in this design a wooden support was used and screwed on the wall, however if you use steel you will have to adapt it.<br />
Apply each of the safety instructions, for this read the safety sheets in annex C.<br />
Also check all the recommendations of “handling concentrated oxygen containers”, please read Annex D.<br />

## Mechanical-electrical respirator
The mechanical respirator consists of several sections:<br />
•	Mechanical-Electrical.<br />
•	Control system. See Annex E for further explanation of biomechanics and its control.<br />
Conceptual design of the respirator without electronics:<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Mechanical_electrical_respirator_conceptual.png?raw=true)<br />

Image 2. – Conceptual design full solution.<br />

Where:<br />
1.	Concentrated oxygen and air input.<br />
2.	Electric mechanical respirator.<br />
3.	Pressure valve.<br />
4.	Humidifier with water based on patient weight.<br />
5.	Expiration output.<br />
6.	Humidifier for patient breathing.<br />
7.	Pressure gauge for negative pressure.<br />
8.	Mask.<br />

## Mechanical-Electrical
The following respirator model allows three parameters to be regulated in a controlled manner during mechanical action.<br />
•	Total volume of air flow.<br />
•	Respiratory rate per minute.<br />
•	Pressure.<br /><br />
It also meets the following requirements:<br />
1.	It must be built with common materials and access to industrial production lines.<br />
2.	Meet medical specifications.<br />
3.	Insurance.<br />
4.	It can be decontaminated, cleaned and reused.<br />
5.	Lower monetary cost compared to a common breathing system.<br />
6.	It's easy to build, maintain and upgrade.<br />
7.	Scalable in improvements.<br /><br />

## Mechanical respirator
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Mechanical_electrical_respirator.jpg?raw=true)<br />

Image 3. - Basic render design of the artificial respirator.<br />

Where:<br />
1.	It is a "Nema 17" engine, widely used in 3-D printers, cheap and easy to get.<br />
2.	It is an axis made up of an endless screw with a big distance between each threaded shank. It allows the control of the pressure exerted and controls the air flow.<br />
3.	Gear system for mechanical work transfer between motor and worm gear.<br />
4.	Balloon flattening plate.<br />
5.	Skeleton and mechanism support. Avoid moving parts. Manual respirator type “Ambu” (Airway Mask Bag Unit).<br />
6.	Balloon.<br />
7.	Air intake and concentrated oxygen entrance.<br />
8.	Connection to mask pipe with non-return valve.<br /><br />

Important:<br />
Parts 6, 7 and 8 are glued together when buying it.<br />
It can also be adapted to infants by replacing a smaller manual respirator and one of the flattening plate (4) by adapting the axis (2).<br />
According to the literature, the oxygen flow at its maximum concentration when supplied to the AMBU ventilator represents a flow of 10 L per minute towards the entrance of the AMBU and presents the highest concentration points when you decrease the respiratory cycle from 1 minute to half a minute<sup>15</sup>.<br />
Since the highest volumetric flow of concentrated oxygen is 10 L per minute for the most extreme cases where the concentration is the highest possible indefinitely, if you have a 100 L tank you will be without oxygen in ten minutes while maintaining that flow.<br />
According to the literature, between 15 and 20 minutes the patient will have to breathe oxygen at the highest concentration possible, after this point the oxygen flow will decrease until reaching fifty percent. The oxygen container presented in the oxygen concentrator has a capacity of 27.8 L. This means if the container is full you will have concentrated oxygen for less than 2.5 minutes when the flow is at its maximum.<br />
When the pressure of the container equals the pressure of the environment the oxygen will stop flowing at the necessary pressure and it will not reach the machine.<br />
It should be noted that the oxygen production capacity of the oxygen concentrator is always above 10 L per minute even using the smallest pipe in Table 1 but it depends on the compressor air flow.<br />
See Annex D for recommendations and precautions regarding the use of medicinal oxygen.<br />
 
## Maintenance
Since the parts of the section 1 respirator are assembled with screws, nuts and washers. The maintenance is quite simple. Technically unscrew, replace the part and re-screw.
<br />

## Electronic

Protoboard. 
3.3V and 5V breadboard Power source or 12 V power supply and resistances.<br />
Arduino Mega.<br />
ESP8266 connection Wi-Fi.<br />
Driver A4988.<br />
Nema 17.<br />
Acme screw.<br />
Bearings.<br />
Nuts.<br />
12V power supply.<br />
Water containers and tubes.<br />
Pressure gauge for negative and positive pressure.<br />

## Control system

A control system regulates the outflow channel to the patient according medical indications and it is essential for the machine in order to operate in a semi-autonomous way.<br />
The control system regulates the machine's concentrated oxygen air outlet valve, below you can see graphs of behavior within the control system used with a set of 2.5 cmH2O and 15 breaths per minute. However you can change settings for other conditions without affecting control. <br />
These graphs showed the behavior of the control system through simulation with “Altair Activate” © open source.<br /><br />

![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Oxygen_pressure_and_breaths.jpg?raw=true)<br />
Image 4. - Behavior of oxygen pressure at a pressure of 2.5 cm H2O and 15 breaths per minute (PaO2).<br /><br />

![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Tydal_volume.jpg?raw=true)<br />
Image 5. - Delivery air volume behavior (V or Tidal Volume).<br /><br />

![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Volumetric_flow.jpg?raw=true)<br />
Image 6. - Delivered volumetric flow behavior (Q).<br /><br />

![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Behavior_of_predictions_for_PaO2.jpg?raw=true)<br />
Image 7. - Behavior of predictions for PaO2, Q y V.<br /><br />

These graphs showed the regulations of the concentrated oxygen pressure towards the patient, the volumetric flow of air and the Tidal volume to the patient for each breath.<br /> Following a sine pattern which, according to Annex A Table 4, is the best flow type since it increases the inspiratory time and is the most similar to normal breathing.<br />
Even with the transfer function proposed in annex E equation Eq. 6, we would have a convergence problem after the 200 iterations, for this we insert a memory block to the system. This memory block only adds a delay of 1 integration per step-time to the circuit. It should be noted that this arrangement with the memory block, under certain circumstances, could incur numerical instability.<br /><br />

## Control system conclusion

We have a device that can provide concentrated oxygen at a certain respiratory frequency for non-invasive cases that complies with the literature<sup>16</sup>.<br />
There should not be a big time gap between the control system and its implementation since reaction time for the valves and the engine is pretty quick.<br />
Furthermore, by solving the equation Eq. 1 and Eq. 2 of Annex E, you could estimate the pressure of the alveolus and the air flow that the pulmonary alveolus would receive. This will be very useful for a total breathing system.<br />
Finally, this control system is insufficient to regulate total respiration. In order to accomplish this we need different sensors and a new control system.<br /><br />
Some of the main parameters to measure and regulate for total respiration are:<br />
•	CO2 concentration.<br />
•	Extraction of H2O as vapor product of respiration.<br />
•	Frequency and respiratory force given by the brain to the lungs.<br />
•	Maximum pressure that an alveolus can support.<br /><br />
We are working to solve the problem of total respiration in a future software update through an update for control system and a procedure manual which will deliver all the connections from the new sensors and valves to the arduino without modifying the basic machinery and principles showed, however, we lack the budget, parts and time outside of working hours to be able to continue beyond the theory since they require medical tests in real time.<br />

## Monitoring visualization
One of the most important but not critical point in a respirator is viewing machine and patient statement.<br /><br />
In our prototype design we decided that the use of monitoring screens per device is quite expensive and not scalable, therefore, we decided to migrate to the cloud with the idea of:<br />
•	Any device connected to the internet with a physical screen, projectors, holograms, etc. it is a potential monitoring screen.<br />
Therefore, we created a monitoring board in the cloud so that it can be accessed by the staff in charge of patients in order to better control each patient and a maintenance monitoring board for technical staff.<br />
If any of the devices fails, then it would be an indication of failure on both boards and cause the taking of actions, even though the respirator has an audible alarm.
However, it is important to emphasize that in our prototype is not 100% online at the moment.<br />
Cloud conceptual diagram:<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Cloud_monitoring.png?raw=true)<br />

Where:<br />
1.	Mechanical-electrical respirator and sensors.<br />
2.	Cloud platform to support a large number of connected respirators.<br />
3.	Visualization on phone, laptop, tablet, etc.<br /><br />
Projected improvements to the platform and digitalization:<br />
•	Setting almost 100% online channel by developing improvements in the platform within the cloud to allow almost real time synchronization.<br />
•	Analytical to review potential improvements in the control systems so that it can later be implemented in the respirators automatically through an internet connection.<br />
•	Internet updates.<br />
•	Mobile app.<br />
•	Notifications system through mobile application.<br />

## Mask for partial breathing

The mask is essential in an assisted breathing system. There are invasive and non-invasive. The difference lies in entering external devices into the body and in the case of total assisted respiration an invasive system such as intubation must be required.<br />
In this project we are seeing a non-invasive type mask.<br /><br />
The most common mask model is as follows:
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Breath_mask.jpg?raw=true)<br /><br />

You can create it using PET bottles and garter.<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Artesanal_mask.jpg?raw=true)<br /><br />

Materials:<br />
•	Scissors.<br />
•	PET bottle 1 L or higher.<br />
•	Plastic hose.<br />
•	Garters.<br />
•	Scotch tape.<br />
•	Plastic cable ties.<br /><br />
Process:<br />
1.	Wash hands, scissors, hoses, rubber bands, and the bottle with soap and water without leaving soap traces.<br />
2.	Use a 1 liter or larger PET bottle.<br />
3.	Cut the bottle as the image marks:<br />
Note: Make a slight bend so it can fit your nose smoothly. We will use the part of the mouthpiece to take, we will call it "upper part". <br />
4.	Insert garters to the sides of the top.<br />
5.	Use the tape to cover the cut edges with the scissors to avoid discomfort.<br />
6.	Remove the top cover.<br />
7.	Wash with soap and water.<br />
8.	Dry the top very well.<br />
9.	Connect the hose to the nozzle.<br />
10.	Seal the hose and the nozzle using tape - garters-plastic cable ties.<br /><br />
With this you will have your own mask. Adjust it very well avoiding gas leaks.<br />
Remember to wash the mask in case it is going to be used by someone else.<br />

## Medical Operation Guide – Partial breathing substitution

Important: This is only an operation guide, it does not imply the substitution of a health professional.<br />
Before you start, make sure you have oxygen on hand, a stopwatch or alarm phone, print out the procedures for making oxygen, and have the printed guide. You should also read Annex A in its entirety.<br />
You must have everything connected and ready including the oxygen tank or concentrator connected to the mechanical-electric respirator.<br />
Remember that the total volume of your oxygen container defines the number of minutes according to the flow to be used in the "procedure" section. If your tank is 100L then divide 100 by the supplied oxygen flow and it will be the maximum minutes of available oxygen.<br />
If you could not automate the process of the oxygen concentrator or do not have enough oxygen cylinders, will n to take turns and guards among several person as to assist those affected and execute procedures.<br />
If the affected person has any previous or chronic illness, please contact a health professional first.<br /><br />
 
Process:<br />
1.	Lay the affected person down in a comfortable place with a shape as semi fowler.<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Pacient_As_semi_fowler.jpg?raw=true)<br />
2.	Turn on the electrical mechanical respirator and set it to run at 15 breaths per minute.<br />
3.	Set the respirator to a constant flow of 10 L per minute.<br />
4.	Fill the two containers with water, the first must have 4 ml per Kg of mass and is connected between the systems so it humidify the air to the affected person. The second is at the end of the tube for expiration, the tube must be hitting the water. <br />
5.	Schedule alarms on your cell from 1 minute to complete 20 minutes, set 5 minute alarms after the first 20 minutes for the next 45 minutes and then keep those alarms indefinitely.<br />
6.	Put the mask on the affected person. It should be tight, not tight.<br />
7.	Verify that the mask has no outdoor sections and is glued to the face.<br />
8.	Ask the affected person how they feel about the mask. Does it bother you? Where?<br /><br />
9.	Activate alarms.<br />
10.	Opening the oxygen valve connected to the cylinder of oxygen or concentrate r oxygen with a flow rate of 10 L / minute.<br />
11.	Constantly check the pressure of the oxygen cylinder or oxygen concentrator.<br />
12.	When the pressure is less than 35 psi, run the procedure for generating oxygen in the oxygen concentrator or prepare the next cylinder at your disposal.<br />
13.	Repeat steps 11 and 12 for until the last 20-minute alarm ends.<br />
14.	Regulates the respirator flow to 8 L per minute and the oxygen flow to 8 L per minute.<br />
15.	Every 15 minutes you will reduce 1 L per minute with respect to your last flow until you are at 5 L per minute.<br />
16.	Constantly check the condition of the mechanical-electrical respirator and the oxygen pressure in your oxygen cylinder or concentrator. If you built the oxygen container in this document, when you reach 5 L per minute you will have oxygen for five minutes.<br />
17.	Set alarms continuously and keep an eye on the affected.<br />
18.	Wait for the affected person to recover, follow the instructions of the health doctors, if it worsens, please call the emergency numbers of your country and region.<br />

In Jalisco, México: +523338233220<br />

## Prototype costs
Note: The costs are only for material, we do not include costs for labor.<br />
As of April 2, 2020. The cloud platform is on our side. The cost of the mask is not included since it is handmade.<br /><br />

Table 4.- Oxygen concentrator
|Equipment/Material|(USD)|
|:---:|:---:|
|CPVC Tubes|25|
|T type connectors x 9|5|
|Elbow type connectors x 5|5|
|Diameter reductors|10|
|CPVC Caps x 2|2|
|Teflon tape|2|
|Ball valves x 8|10|
|Threaded valve x 1|15|
|Manometer x 4|45|
|Union nut x 5|5|
|Tube-cpvc male-female adapters|3|
|Compressor|80|
|Wood panel|3|
|Lug/Handles x 4|10|
|Cooler|2|
|absorbent (depends on the size) 25 kg|6|
|Steel nets x 6|36|
|Cement x 1 can|3|
|Transparent hose x meter|1|
|Filters (sheet) m2|5|
|Total|283|


Table 5.- Mechanical-electrical respirator

|Equipment/Material|(USD)|
|:---:|:---:|
|SMC|120|
|Arduino Mega|20|
|Wifi Module|8|
|Driver A4988|1.5|
|12V power supply|10|
|Nema 17 stepper motor|9.2|
|3/8" screw stud|25|
|3/8" bearings|3|
|3/8" nuts|3|
|M4 screws|3|
|AMBU|26|
|3-D printing|11|
|Protoboard|4|	
|Total|238.7|


These costs will decrease in environments like industrial production lines. <br />
In addition, only the presented mechanical-electric respirator is at least twice cheaper than the cheapest model of fans for this item in industrial production, and the fan shown online does not include an oxygen generation capacity or allow working under the appropriate conditions. <br />
For air-assisted breathing with concentrated oxygen, however it is smaller the cheapest model.  
https://m.alibaba.com/amp/product/60776944726.html<br />

## Improvements
As part of any project we are continually improving.<br />
We have decided to include the main improvements in process that we are making.<br />
Adaptability for other compression systems, an example would be the compressible accordion type container, among others.<br /><br />
Conceptual example:<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Mechanical_electrical_improvements.png?raw=true)<br />

Where:<br />
1.	Mechanical-electric respirator presented.<br />
2.	Adaptation to accordion type respirator.<br /><br />

Oxygen concentrator.<br />
	•	Automation of the oxygen generation process and emergency process.<br />
	•	Increase in the concentration of oxygen generated during the process.<br /><br />

Mechanical-electric respirator<br />
	•	System capable of adaptation in case of replacement of the AMBU respirator.<br />
	•	System with capacity of adaptation for infants.<br />
	•	Cover the replacement of total breathing for the patient.<br />
		o	Improvements in the control system for total breathing.<br />
		o	Incorporation of new sensors.<br />
		o	Technical manual for the implementation of physical components-connection.<br />
	•	Updating of software-control system via internet.<br /><br />

Mask<br />
	•	Include other models of mask for 3-D craft printing.<br /><br />

Medical operation<br />
	•	Include manual of medical operation for invasive cases.<br /><br />

Strengthen cloud platform.<br />
	o	Online channel with the machine.<br />
	o	Robust access security system.<br />
	o	Include patient sensors.<br />
	o	Improved dashboard for patients / technicians.<br />
	o	Analytics.<br />
			Improvement in the control system control cycle.<br />
			Patient regulation.<br /><br />

Improvements in long-term vision.<br />

Mobile app.<br /><br />
Oxygen concentrator<br />
	•	Physical reduction of the oxygen generation process.<br />
	•	Change of materials for the oxygen generation process.<br /><br />
Complete Solution<br />
	•	Machine operation configuration from portable devices.<br />
	•	Smart system.<br />
	•	Data Lake.<br />

## Conclusion

With all these investigations, iterative calculations and constant design modifications, we obtained a first prototype of a partial artificial respirator that: <br />
|Point|To consider|Status|Comments|
|:---:|:---:|:---:|:---:|
|1|It must be built with common materials and access to industrial production lines.|Done|Electrical control devices are easily accessible for production lines.|
|2|Comply with medical specifications.|Done|Concentrated oxygen free of impurities through filters.|Control system for respiratory regulation and medical parameters.System with manual configuration capacity.Sensitivity to expiration.|
|3|insurance|Done|As long as it is in a box and out of the reach of children. Non-toxic materials.|
|4|Can be decontaminated, cleaned and reused.|Done|Being segmented, it allows quick disarmament.|
|5|Lower monetary cost compared to a common breathing system.|Done|| 
|6|Simple to build, maintain and upgrade.|Done|Few parts, segmented and easy to replace. Update online.|
|7|Scalable in improvements.|Done|Module-based design with quick installation and adaptation.|


This solution is made up by:<br />
1.	Oxygen concentrator.<br />
2.	Mechanical-electric respirator. (Design, motor, valves, arduino and accessories, sensors and control system).<br />
3.	Mask.<br /><br />
We also include a user manual and include annexes to support what is presented in this development.<br />
Document subject to modifications and updates.<br />

## References
1. https://www.msn.com/en-in/finance/news/who-chief-says-covid-19-enemy-against-humanity-as-global-cases-top-200000/ar-BB11nXqI
2. https://www.nytimes.com/2020/02/29/health/coronavirus-preparation-united-states.html
3. http://www.hydrogencarsnow.com/index.php/hydrogen-from-water/
4. https://www.sciencedirect.com/science/article/pii/B978012812036100007X
5. https://www.familyhandyman.com/plumbing/boost-low-water-pressure-in-your-house/
6. http://earthguide.ucsd.edu/eoc/special_topics/teach/sp_climate_change/p_planet_temp.html
7. https://www.ijser.org/researchpaper/Oxygen-Separation-from-Air-Using-Zeolite-Type-5A.pdf
8. https://healthfully.com/o2-cylinder-hydrostatic-test-requirements-7482823.html ; https://www.astm.org/Standards/G175.htm
9. https://www.engineeringtoolbox.com/cpvc-pipes-pressures-d_240.html
10. https://web.archive.org/web/20140907211639/http://www.algalita.org/blog/?p=3740
11. Ishtiaq Ali, Muhammad (2011). Microbial degradation of polyvinyl chloride plastics (PDF) (PhD). Quaid-i-Azam University. pp. 45–46 & 122. 
12. Costner, Pat (2005) "Estimating Releases and Prioritizing Sources in the Context of the Stockholm Convention" Archived 27 September 2007 at the Wayback Machine, International POPs Elimination Network, Mexico.
13. International Agency for Research on Cancer (IARC). "Vinyl chloride, polyvinyl chloride, and vinyl chloride-vinyl acetate copolymers." Vol 19, 1979. IARC. "Vinyl chloride." Supplement 7, 1987. Lyon.
14. https://www.engineeringtoolbox.com/thermoplastic-pipes-temperature-strength-d_794.html
15. https://pubmed.ncbi.nlm.nih.gov/16053945/
16. Michael C.K. Khoo. Physiological Control Systems: Analysis, Simulation, and Estimation, segunda edición. The Institute of Electrical and Electronics Engineers, Inc. Publicado en 2018 por John Wiley & Sons, Inc. pp 31-61.





