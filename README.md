SRS-
====

final SRS of the project:



Course Project Documentation
CS684 Project





AUTOMATED DRIP IRRIGATION SYSTEM USING EMBEDDED SYSTEM


TEAM NO: 16

BHADARKA PHALGUNI
DINGANE BHAGYASHREE
SHINDE ABHIJEET















Table of Contents
1. Introduction.................................................................................3
2. Problem Statement......................................................................4
3. Requirements...............................................................................5
4. Implementation............................................................................6
5. Testing Strategy and Data............................................................7
6. Discussion of system..................................................................15
7. Future Work...............................................................................17
8. Conclusion.................................................................................17
9. References..................................................................................18







1. Introduction:

Aim:
The continuous increasing demand of the food requires the rapid improvement in food production technology. In a country like India, where the economy is mainly based on agriculture and the climatic conditions are isotropic, still we are not able to make full use of agricultural resources. The main reason is the lack of rains & scarcity of land reservoir water. The continuous extraction of water from earth is reducing the water level due to which lot of land is coming slowly in the zones of un-irrigated land. Another very important reason of this is due to unplanned use of water due to which a significant amount of water goes waste. In the modern drip irrigation systems, the most significant advantage is that water is supplied near the root zone of the plants drip by drip due to which a large quantity of water is saved. At the present era, the farmers have been using irrigation technique in India through the manual control in which the farmers irrigate the land at the regular intervals. This process sometimes consumes more water or sometimes the water reaches late due to which the crops get dried. Water deficiency can be detrimental to plants before visible wilting occurs. Slowed growth rate, lighter weight fruit follows slight water deficiency. This problem can be perfectly rectified if we use automatic microcontroller based drip irrigation system in which the irrigation will take place only when there will be intense requirement of water. 

Irrigation system uses valves to turn irrigation ON and OFF. These valves may be easily automated by using controllers and solenoids. Automating farm or nursery irrigation allows farmers to apply the right amount of water at the right time, regardless of the availability of labor to turn valves on and off. In addition, farmers using automation equipment are able to reduce runoff from over watering saturated soils, avoid irrigating at the wrong time of day, which will improve crop performance by ensuring adequate water and nutrients when needed.  Automatic Drip Irrigation is a valuable tool for accurate soil moisture control in highly specialized greenhouse vegetable production and it is a simple, precise method for irrigation. It also helps in time saving, removal of human error in adjusting available soil moisture levels and to maximize their net profits.

2. Problem Statement:

To build automatic plant irrigation system based on microcontroller 8051.
The Project presented here waters your plants regularly when you are out for vocation. In this the irrigation will take place only when there will be intense requirement of water using automatic microcontroller embedded system. 

The project is to implement the idea of automating the watering phase of gardening using conceal drip irrigation technique to conserve manpower, water and improve the growth, quality and yield of plants. The proposed system is an embedded system which will closely monitor and control the various soil parameters of a greenhouse on a regular basis for cultivation of crops or specific plant species or large natural turfs which could maximize their production over the whole crop growth season and to eliminate the difficulties involved in the system by reducing human intervention to the best possible extent. The system comprises of sensors, Analog to Digital Converter, microcontroller and pump.


3. Requirements:

A) Hardware Requirements
1.   AT89S51:- The AT89S51 is a low-power, high-performance CMOS 8-bit microcontroller with   4K bytes of In System Programmable Flash memory.
2. ADC0808/ADC0809 of National Semiconductor (8-Bit µP Compatible A/D Converters with 8-Channel Multiplexer)
3.   GSM modem AVR323
4.   LM7805 Series Voltage Regulators
5.   MAX 232:- The MAX232 is a dual driver/receiver that includes a capacitive voltage generator to supply TIA/EIA-232-F voltage levels from a single 5-V supply
6.   Relay driver ULN2803
7.   2x16 Serial LCD Display Modules.

B) Software Requirements
8.   BASCOM-8051© is the Windows BASIC COMPILER for the 8051 family. It is designed to run on W95/W98/NT/W2000 and XP.
9.   Eagle



4. Implementation:

A) Functionality:

a) Automatic SMS is send to the farmer with the status report:

We had added three sensor in our project such as water sensor ,soil sensor and voltage regulator such as after rectifying all the condition that to be satisfy the message is to be send to the farmer giving the status report about is drip irrigation system
  
b) Pump on and off automatically:

When all the sensor give its output to the system it rectify whether the value is above or below the threshold value which is to be inserted by the programmer within the system.
According to the threshold values the pump gets on or off automatically as well as notification is to be given to the farmer 


5. Testing Strategy and Data:
STEP 1 Burn the code on chip
•	All the code was burn on the micro controller chip by programmer
•	Such as the PCB can run the code without computer
•	This kind of system development call as embedded  system
•	For this we need MCS Flash Programmer.


STEP 2 Execute the project and run the project
•	Execution of the project has been started by doing power on.
•	First it will first show name of our project on LCD display.
•	Then it shows the name of our guide.
•	Mean while microcontroller will check the input values by sensor as per the conditions given in the code.
•	According to that the next step will be performed as it displays the result or message on LCD display. 

 
STEP 3 See the LCD display
•	LCD display shows the status of the project.
•	That is Pump ON/OFF.
•	It also includes the three parameters of sensor input as M for Moisture, W for Water Level and V for Voltage.
•	This is the actual Output which we have considered in our project.  
It will also shows reason in the text format why the Pump gone OFF


STEP 4 Result Pump on and off
•	This step will show the result or the output of our project.
•	As per the checked conditions by step 7 it will conclude that Pump will be on or off.
•	It also show the parameters of input values and reason why pump is off. 


STEP 5: Sending SMS to user by project
•	In this step micro controller will send the notification/message to the user.
•	The message includes status of the pump and the three parameters values.
•	As it shows the Pump is ON and values of sensors are as M:” ” W:” ”V:” ”.
•	If due to some input problem pump will OFF then it will again send a message to the user that Pump is OFF and values of the sensors are as M:” ” W:” ”V:” ”.
•	It also sends a text that due to what reason Pump goes OFF. E.g. as above “Voltage Problem”.



Test plan and Test Results:

a)	UNIT TESTING:
1	UNIT TESTING OF VOLTAGE:
TEST CASE	VOLTAGE	EXPECTED PUMP STATUS	PUMP STATUS
Low Threshold Value	182	ON	ON
High Threshold Value	260	ON	ON
Middle Value	192	ON	ON
Below Low Threshold Value	150	OFF	OFF
Above High Threshold Value	300	OFF	OFF


2	UNIT TESTING OF WATER:

TEST CASE	WATER LEVEL	EXPECTED PUMP STATUS
	ACTUAL PUMP STATUS
Minimum Threshold	25	ON	ON
Maximum Threshold	100	ON	ON
Below Minimum Threshold	15	OFF	OFF


3	UNIT TESTING OF MOISTURE:

TEST CASE	MOISTURE	EXPECTED PUMP STATUS
	ACTUAL PUMP STATUS
Threshold Value	100	ON	ON
Below Threshold Value	75	ON	ON
Maximum Value Above Threshold	255	OFF	OFF
Above Threshold Value	150	OFF	OFF


b)	STRESS TESTING:

DESCRIPTION	VOLTAGE	MOISTURE	WATER LEVEL	EXPECTED PUMP STATUS
	ACTUAL PUMP STATUS
Minimum Threshold Voltage Value	182	70	30	ON	ON
Maximum Threshold Voltage Value	260	75	50	ON	ON
Threshold Value Of Water	210	60	25	ON	ON
Threshold Value Of Moisture	190	100	50	ON	ON
c)	WHITE BOX TESTING:

Observation Table
SR no.	Sensor Readings	Output
	Moisture
(100 cut-off)	Water level
(25 cut-off)	Voltage
(180-260V)	

1	0	24	28	Pump OFF, Water level low/ voltage problem
	0	0	BR	
2	0	24	243	Pump OFF, water level low
	0	0	IR	
3	0	0	AR	Pump OFF, water level low/ voltage problem
4	8	84	24	Pump OFF, voltage problem
	0	1	BR	
5	0	84	210	Pump ON
	0	1	IR	
6	0	1	AR	Pump OFF, voltage problem
7	135	17	99	Pump OFF, moisture OK/ voltage problem
	1	0	BR	
8	183	17	240	Pump OFF, moisture OK/ water level low
	1	0	IR	
BR = Below Range        IR = In Range        AR = Above Range
6. Discussion of System:
A) What are worked as per plan?
1. Automated work is done without user interference
2. Irrigation system automatically gets off when water exceed or tanks get empty
3. Status report is automatically forwarded to the user as any problem occur with in the system
4. Nofication of water moisture or voltage drop is also given to the user via SMS.

B) What we added more than discussed in SRS?
LCD display is also added with mobile notification

(C) Changes made in plan:
1) In spite use of MPLAB software we had use BASCOM8051 software just only to make more easily compatible with the system.
2) We had made use of cheap water sensor only to detect the presence of water.

7. Future Work:

We can add an additional constraint to our project.
There is always a chance to improve any system as research and development is an endless process. Even our system is no exception to this phenomenon. The following improvements can be done:
•	Other Sensors like pH sensors, temperature sensors can be added.
•	Automation using Call facility can be included.
•	As discussed earlier the system can be implemented to grow lawn in stadiums or grounds like hockey, polo, golf on large scale basis etc.
•	Also we can control our Drip Irrigation system by using Internet connection remote access.


8. Conclusions:
The Microcontroller based drip irrigation system proves to be a real time feedback control system which monitors and controls all the activities of drip irrigation system efficiently. The present proposal is a model to modernize the agriculture industries at a mass scale with optimum expenditure. Using this system, one can save manpower, water to improve production and ultimately profit


9. References:

	Albert Melvin and David Bates “Electronic principles”.
	www.datasheet.com
	 www.microchip.com
	www.jaindripirrigation.com
	www.processsensors.com 
	www.vegatronics.com 
	www.google.com 
	BASCOM-8051:Windows basic compiler for 8051 by Dusko Duricin

