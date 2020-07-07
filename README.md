# Zephyros
Multidisciplinary project for oxygen generation, medical artificial breathers and cloud services. <br />

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
According to the theory we will be working at pressures between 45 and 115 psi (4 to 8 bar) maximum. The air around us is at 14.7 psi, therefore we will be working with pressures higher than atmospheric.
It seems to be dangerous but the water you have in your house is between 40 and 80 psi maximum, so we will be working at relatively similar pressures but with gases [5].
Another factor to consider is the temperatures of the process and the environment around you, however, the temperature range of planet Earth on its surface ranges from -85 ° C (-117.4 ° F) to almost 60 ° C (140 ° F) [6] .
And for the process, we will be working under the shade at a temperature similar to 25 ° C (77 ° F), however, the temperature of your home and region may be different from ours.
Note: See Annex C for the safety data sheets of the chemical products involved in the process.
Table 1. - Process production by type of absorber diameter. Oxygen produced between 60 - 80% concentrations with zeolite [7].
|Selected Diameter (inch)|Length (inch)|Liters of oxygen / minute|Kg of zeolite|Bucket or container of cold water (gallons)|Maximum tolerable pressure [1] (PSI) 40|Maximum tolerable pressure [1] (PSI) 80|
|8|33|27.2|40|30.00|160.00|250.00|
|6|33|20.4|30|22.50|180.00|280.00|
|4|33|13.6|twenty|15.00|220.00|320.00|
|3|33|10.2|fifteen|11.25|260.00|370.00|


