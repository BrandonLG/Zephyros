## Linear mechanical modeling during respiration
Objective: Obtain a transfer function that can be used in a controller for the non-invasive respirator.<br />
![alt text](https://github.com/BrandonLG/Zephyros/blob/master/Images/Mechanical_model_of_breathing_lungs.jpg?raw=true)<br />
Image 1. - Diagram of the mechanical model of breathing to the lungs.<br /><br />

We first need a descriptive linear model of the mechanics of a lung. Air channels are divided into two categories:<br />
Long or central (bronchi- central alveolus). R_C<br />
Small or peripheral (alveolus).  R_P<br />
When air enters the alveolus, there is an expansion of the chest cavity by almost the same volume. This is represented by the connection C_L and C_W in series. <br />
However, a small fraction of the volume of air entering the respiratory system is diverted from the alveolus as a result of the expansion of the central airways and the compressibility of the gas. <br />
The deviated volume is very small under normal conditions, however, as there is a disease, obstructions can occur that increase resistance R_P,  that is, an increase in stiffness of the lung or pectoral expansion, that is, decrease C_L and / or C_W. <br />
To take these effects into account, we consider a deviation conformity called Cs in parallel to C_L and C_W.<br /><br />

Where: <br />
PaO = Inlet air pressure [=]  cmH2O<br />
P_aw = Central air pressure [=]  cmH2O<br />
P_A = Alveolus pressure [=]  cmH2O<br />
P_pl = Pleural space pressure [=]  cmH2O<br />
P_0 = Ambient pressure [=]  cmH2O<br />
Cs = Diversion conformity [=]  L/(cmH2O)<br />
C_L = Partial fraction of the lung [=]  L/(cmH2O)<br />
C_W = Pectoral expansion [=]  L/(cmH2O)<br />
R_C = Central / long flow resistance [=] (cmH2O)/L<br />
R_P = Peripheral / small flow resistance [=] (cmH2O)/L<br />
Q = Air flow [=]  L/min<br />
Q_A = Flow delivered to the alveolus [=]  L/min<br />

Using Kirchhoff's second law (applied to the node P_aw), if the flow delivered to the socket is Q_A, then the outflow from the socket is defined as Q - Q_A. Applying KCL to the closed loop system containing: Cs, R_P, C_L and C_Wthen we have:<br />

R_P Q_A+ (1/C_L +1/C_W ) ∫▒Q_A  dt=  1/C_S  ∫▒(Q- Q_A )dt           Eq.1<br /><br />

Applying Kirchhoff's first law to the containing circuit R_C and Cs, then we have:<br />

P_ao= R_C Q+  1/C_S  ∫▒〖(Q- Q_A )  dt〗            Eq.2<br /><br />

Making the differential equation with Eq. 1 and Eq. 2 with respect to time and reducing the two equations in one eliminating the Q_A we obtain an equation that relates P_ao to Q:<br />

(d^2 P_ao)/〖dt〗^2 +  1/(R_P C_T )  〖dP〗_ao/dt= R_C  (d^2 Q)/〖dt〗^2 +(1/C_S +R_C/(R_P C_T ))  dQ/dt+1/(R_P C_S ) (1/C_L +1/C_W )Q         Eq.3 <br /><br />

Where C_T can be defined as:<br />
C_T= (1/C_L +1/C_W +1/C_S )^(-1)           Eq.4<br /><br />

Using LaPlace transform.<br />
L{(d^2 P_ao)/〖dt〗^2 + 1/(R_P C_T )  〖dP〗_ao/dt= R_C  (d^2 Q)/〖dt〗^2 +(1/C_S +R_C/(R_P C_T ))  dQ/dt+1/(R_P C_S ) (1/C_L +1/C_W )Q}          Eq.3 <br /><br />

This equals:<br />

s^2 P_ao (s)-sP_ao (0)-P_ao (0)+1/(R_P C_T ) (sP_ao (s)-P_ao (0))= R_C (s^2 Q(s)-sQ(0)-Q(0))+(1/C_S +R_C/(R_P C_T ))(sQ(s)-Q(0))+1/(R_P C_S ) (1/C_L +1/C_W )(Q(s))    Ec. 4<br /><br />

Substituting time 0; P_ao (0)=0 and Q(0)=0, and taking the common factor on both sides:<br />

P_ao (s)(s^2+s/(R_P C_T ))= Q(s){R_C s^2+(1/C_S +R_C/(R_P C_T ))s+1/(R_P C_S ) (1/C_L +1/C_W )}    Eq.5 <br /><br />

With all of the above considerations we obtained a transfer function with the following characteristics:<br />

(Q(s))/(P_ao (s))=  ((s^2+s/(R_P C_T )))/{R_C s^2+(1/C_S +R_C/(R_P C_T ))s+1/(R_P C_S ) (1/C_L +1/C_W )}       Eq.6<br /><br />

Considering the pulmonary factors presented on page 31 and substituting the equation Eq. 4 in the equation Eq. 6, we can calculate:<br />

Cs = 0.005  L/(cmH2O)<br />
C_L = 0.2  L/(cmH2O)<br />
C_W = 0.2  L/(cmH2O)<br />
R_C = 1 (cmH2O)/L<br />
R_P = 0.5 (cmH2O)/L<br /><br />

(Q(s))/(P_ao (s))=  ((s^2+420s))/{s^2+620s+4000}       Eq.6.1<br /><br />

So, we already have a control function that would regulate the operation of the valve based on oxygen pressure and volumetric flow to the patient. <br />
However, it is also necessary to take into account the golden rule of inhalation-expiration which tells us that for each second of inhalation, it must be two seconds of expiration.<br />
So we need to include a feedback in the form of negative pressure that regulates the action time inside the procedure programming but not directly to the control system.<br />
For our controller in real life we will use the transfer function shown in the equation Eq. 6.1, however, their coefficients in the denominator and numerator can be adapted as appropriate using equation Eq. 6.<br />
If you model the process of the artificial respirator in “Altair Activate” © you will see that the transfer function allows a flow of a sine type, which is the most similar to natural respiration. For more information see annex A table 4.<br />
Up to this point the model can control partial respiration in mild to moderate cases.<br /><br />
As a future second part, we are considering more severe cases with total respiration which requires taking into account:<br />
1. The gas exchange of CO2, H2O, O2  and other gases during respiration. <br />
Chemoreceptors are required to measure CO2 concentrations, a lower neuron circuit in the brain to measure respiratory rate, and the strength of the muscles of the respiratory system.<br /><br />
2. Extract H2O vapor generated during respiration and expelled during exhalation pipe to prevent condensation water and fill the lungs if it reaches the steam dew point.<br /><br />
3. The maximum pressure that the alveolus can bear (maximum P_A).<br /><br />

Although we can model and explain the solution for each of the cases, we lack the budget, parts and time outside working hours in order to do all the physical and medical tests that are needed in real time, so we have to work with a slowdown pace.<br />

## Source:
Michael C.K. Khoo. Physiological Control Systems: Analysis, Simulation, and Estimation, segunda edición. The Institute of Electrical and Electronics Engineers, Inc. Publicado en 2018 por John Wiley & Sons, Inc. pp 31-61.
