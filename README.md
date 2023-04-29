# AC-to-variable-DC-power-supply
AC to variable DC power supply
	Objectives:
The main objective of this project is to create an AC to DC converter which takes 220V AC as input and outputs a regulated DC voltage between the range of +3V to +15V.
	Introduction:
The project consists of three main comparisons which are between theoretical values, simulated values and practical values.
	Statement of problem:
To manage the ripple factor to be under 1% and have a variable voltage between 3V and 15V. 
	Theoretical work:
 
	A Step down transformer (10:1) which steps down the voltage to 24V RMS. This transformer has 0.42A maximum current output.
	The peak voltage, AC, is first calculated. This is the voltage produced from Full wave rectifier chip (KDU4D):
 
	The DC voltage output of the rectifier is then calculated considering that we have a maximum ripple of 1%:
 
 

	The theoretical ripple percentage was calculated as following:
 
	The capacitance was calculated using the design equation. The load voltage was assumed to the maximum output of 15V:
 
	The Resistor values where calculated as following:
	The value of R2 ( variable resistor) was assumed to be 1KΩ.
	After trial and error, we found out that there is always a ratio between R2 and R1; which is R2=0.25R1.
	R3 was calculated by modifying the LM317 Datasheet formula to our needs:
 

	The load current across the 100 Ohm load resistor can be simply calculated by Ohm’s law for V¬0 max:
 
	The load current across the 100 Ohm load resistor can be simply calculated by Ohm’s law for V¬0 min:
 
	As for the output voltages, the maximum should be 15V while the minimum should 3V.

	Simulated work:

 

	The Peak Voltage (Vp) was found as following:
 
This value has to be multiplied by √2 therefore Vp=33.90

	The DC voltage (VDC) was found as following:
 




	The ripple Voltage (Vr) was found as following:
 
	The ripple Voltage (Vr%) was found as following:
 
	The maximum Load current (IL15V) was found as following:
 
	The minimum Load current (IL3V) was found as following:
 
	The maximum output voltage (V0 max) was found as following:
 





	The minimum output voltage (V0 min) was found as following:
 





	Practical work:
 

	Components used:
	Step down transformer: TRIA VPP24-420.
	KDU4D Full bridge rectifier.
	4.7mF, 50V capacitor.
	LM317 Voltage regulator chip.
	35kΩ Resistor.
	250Ω resistor.
	1KΩ Variable resistor.
	PCB solder bread board.
	High power 100Ω Load resistor.

	The Peak Voltage (Vp) was found to be 31.30V

	The DC voltage (VDC) was found to be 38.80V

	The ripple Voltage (Vr) was found as following 2.05V

	The ripple Voltage (Vr%) was found as following:
 
	The maximum Load current (IL15V) was found as 146mA

	The minimum Load current (IL3V) was found as 30mA

	The maximum output voltage (V0 max) was found as 14.70V

	The minimum output voltage (V0 min) was found as 3.08V
 
	Comparison:
 	Theory	Simulated	Practical	Error % Theoretical Vs. Simulation	Error % Theoretical Vs. Practical
Vp/V	32.52	33.90	31.30	4.07	3.75
VDC/V	30.98	31.50	38.80	1.65	20.15
Vr/V	0.32	0.07	2.05	77.50	84.39
Vr %	0.28	0.70	1.52	60.00	81.58
C/mF	4.69	4.70	4.70	0.21	0.21
IL3V/mA	30.00	30.24	30.60	0.79	1.96
IL15V/mA	150.00	150.00	146.00	0.00	2.67
Vo max/V	15.00	15.09	14.70	0.60	2.00
Vo min/V	3.00	3.02	3.08	0.66	2.60

	Discussion of the Results:
In general the results were good but some values need to be discussed:
	Peak voltage as source voltage will become RMS voltage at the capacitor which explains the 38.80 reading the V¬DC practical reading.
	For Theoretical Vs. Practical of VDC the error was 20.15% because as capacitance increases the average voltage increases due to the reduction of ripple voltage.
	As for V¬r results of 77.5% and 84.39%; this is due to the regulator having a resistance. This is not accounted for in the theory and is less in the simulation than in practical.

	Conclusion:
A voltage regulator was created that takes as input a 240V AC source and outputs a DC voltage between +3V and +15V, the range can be obtained by turning the variable resistor. Theoretical, Simulated and practical results were found and compared and found to be acceptable. Some values were different but the reason of that was explained.


	References:
	http://www.alldatasheet.com/datasheet-pdf/pdf/95601/TI/LM317.html
	http://catalog.triadmagnetics.com/Asset/VPP24-420.pdf
	https://www.electronics-tutorials.ws/diode/diode_6.html
	https://elearning.qu.edu.qa/bbcswebdav/pid-2757075-dt-content-rid-4142940_2/courses/Spring_2018_ELEC231_21645/ELEC231_Ch03_SP18.pdf

