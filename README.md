# Zephyros
Multidisciplinary project prototype for oxygen generation, medical artificial breathers, PLC, Machine Learning and cloud services. <br />

![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Zephyros_explanation.JPG?raw=true)

## Team <br />
Engineering <br />
Abel Geovanny Loera – Linkedin – https://www.linkedin.com/in/abel-geovanny-loera-navarro-a63542123 <br />
Brandon F. Loera – Linkedin – https://www.linkedin.com/in/brandon-f-loera-ba519ab7 <br /> <br />
Medicine <br />
María Jacqueline Martínez – jacquelinemtz_84@Outlook.es <br /> <br />
Legal <br />
Hannia Loera – Linkedin - https://www.linkedin.com/in/hannia-melisa-loera-garcia-2a6779171 <br /> <br />
Diffusion – Marketing – MedMark <br />
Perla Elianne Garza – Linkedin – https://www.linkedin.com/in/perla-elianne-garza-17361a15a <br /> <br />
Collaborators <br />
Abel Loera – Linkedin – https://www.linkedin.com/in/abel-loera-54841050 <br /> <br />
Feliciano Loera – Linkedin – https://www.linkedin.com/in/feliciano-loera-18232054 <br /> <br />

Document control versions <br />
Version	Date <br />
1.-	27th March of 2020 <br />
2.-	29th March of 2020 <br />
3.-	1st April of 2020 <br />
4.-	3rd April of 2020 <br />
5.-	6th April of 2020 <br /> <br />
	
# Introduction and scope
Currently the Covid-19 pandemic has become an "enemy of humanity"[1] according to the World Health Organization. <br />
Given this situation, we have seen that the main public health problem is in the number of artificial respirators and masks available [2]. <br />
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
Electrolysis, without the appropriate materials, is costly at the electrical energy level, produces little oxygen and is quite unsafe since it generates gaseous hydrogen [3] and it is highly flammable and in appropriate conditions is explosive [4]. <br />
Therefore we select the pressure process called PSA. <br />
Note: See Annex B for the theory behind the PSA. <br />

## Conceptual design oxygen concentrator
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Oxygen_concentrator.png?raw=true)

## Process indication
According to the theory we will be working at pressures between 45 and 115 psi (4 to 8 bar) maximum. The air around us is at 14.7 psi, therefore we will be working with pressures higher than atmospheric. <br />
It seems to be dangerous but the water you have in your house is between 40 and 80 psi maximum, so we will be working at relatively similar pressures but with gases [5]. <br />
Another factor to consider is the temperatures of the process and the environment around you, however, the temperature range of planet Earth on its surface ranges from -85 ° C (-117.4 ° F) to almost 60 ° C (140 ° F) [6] . <br />
And for the process, we will be working under the shade at a temperature similar to 25 ° C (77 ° F), however, the temperature of your home and region may be different from ours.
Note: See Annex C for the safety data sheets of the chemical products involved in the process. <br /><br />
Table 1. - Process production by type of absorber diameter. Oxygen produced between 60 - 80% concentrations with zeolite [7]. <br />
|Selected Diameter (inch)|Length (inch)|Liters of oxygen / minute|Kg of zeolite|Bucket or container of cold water (gallons)|Maximum tolerable pressure [1] (PSI) 40|Maximum tolerable pressure [1] (PSI) 80|
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
A common oxygen tank has a pressure of approximately 600 psi and is made of industrial steel with ASTM standard specification [8].<br />
Never leave the oxygen concentrator in the sun or near heat sources.<br />
It should not be near the reach of children.<br />
See Annex D for further indications on the proper use of oxygen.<br />

## Selection of the material
To make the oxygen concentrator we selected CPVC since its maximum operating pressure [9] allows us to carry out the process, it is easy to find and it is less expensive than other materials. <br />
Regarding the environment, its absorption capacity of POPs pollutants is lower than other polymers such as: HDPE, LDPE and PP [10] which implies a significant reduction in pollutants accumulation inside the food chain once the materials are discarded and taken away as garbage, however, we strongly encourage a recycling attitude. <br /><br />
Another important point to mention about CPVC is its degradation. <br />
Degradation can be mad by biological entities like fungi "Aspergillus fumigatus", "Phanerochaete chrysosporium", "Lentinus tigrinus", "Aspergillus niger" and "Aspergillus sydowii" which consume the CPVC [11] On the other hand, if CPVC is burned it will generate compounds like dioxins [12] which are harmful to the human body due to the chemical compound “vinyl chloride” which is a known carcinogen [13]. <br />
For all of the above, we recommend to use stainless steel if you have the appropriate budget. <br /><br />
Table 2. - Maximum pressure of the CPVC according to the internal diameter. <br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/CPVC_Operational_properties.jpg?raw=true)<br />

However, it is also necessary to consider how does the temperature affects the material, in the case of CPVC it is a thermoplastic, which means heat affects the pressure that the material can withstand and heat is closely related with temperature. <br />
Thus, the relationship between the pressure which the material can withstand and the temperature of the process/environment can be seen within the following table [14]: <br /><br />
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
2 tubes. They can be of type 40 or 80. For both tubes, the same diameter. Use table 1.
1 tube 1 1/2 inch in diameter and 4 inches long. Purge / waste.
1 tube 3 inches in diameter and 12 inches long. Water and CO2. Eliminator.
1 tube 6 inches in diameter and 60 inches long. (Container for oxygen). Capacity of 27.8 L.
9 1/2 inch T-type connectors.
5 for pipe joints and 4 for manometers.
  Way of union with the manometers ->  
5 1/2 inch elbow connector.
 
8 1/2 inch ball-type valves.
 
1 1/2 inch pressure regulating valve.
  
5 Nut-union.
Tube-cpvc male-female adapters.
3 meters tube 1 /2 inch in diameter to make connections.
Diameter reductors.
 
1 CPVC - Serpentine connector.
2 CPVC caps of the selected diameter for absorbers.
Bite union hose.
1 Teflon tape or paste.
3 manometers with measurement capacity up to 150 psi.
 
1 manometer with measurement capacity up to 30 psi.
 
1 meter of transparent hose to connect to the compressor inlet (the diameter depends on your compressor)
 
1 container for cold water and the size must be according to the diameter selected in table 1.
1 steel / aluminum serpentine.
1 bag of ice to cool.
4 round steel net that can be inserted into tubes with the selected diameter.
2 net round steel 3 inches
Note: Steel nets must have pores that are smaller in size than the absorbent to be used.
 
1 can of clear CPVC cement that allows pressures between 180 and 250 psi.
  
Cooler.
 
Absorbents.
CMS (Carbon Molecular Sieve), activated carbon or Zeolite type 5A (if any). The latter can be bought from silica producers or agriculture providers. See table 1 for the specific weight you need inside the absorber and to that amount add 5 kg of absorbent. If you're going to produce your own activated carbon then multiply that amount by 1.3. For more information regarding absorbents see annex B.
2 air filters between 4 and 0.01 microns.




