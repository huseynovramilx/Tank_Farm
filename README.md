# Introduction
“Tank Farm” project is a SCADA project made in Tia Portal for simulating a process.

# Process Overview
Our process consists of four tanks, three of which are slave while the other one is
master. There are inlet and outlet for each tank which lets operators to control
them individually and 3 pumps, one for charging slave tanks, one for charging
master tank and discharging slave tanks and the last one for transmitting the
process fluid to customers. In normal conditions they are going to be operated
manually by operator, however, there is also an automatic control for both valves
and pumps in the case of anormal situations. For example, inlet valve to slave tank is
automatically activated when the level in the tank is lower than limit.

# Design Envelopes
As mentioned above one of the concerns is to keep process fluid in each tank at moderate level. Therefore, there are predefined high level and low levels that activate alarms. These alarms are used to automatically turn on or turn off pumps and valves. When the low level alarm is activated for slave tanks, inlet valves and pump charging these tanks are turned on. As for high alarm, it turns off inlet valves and activates outlet valves. Here is the table illustrating the capacities of tanks. 


|                  |  Tank140 |	Tank150 |	Tank160 |	Tank170 |
|------------------|----------|---------|---------|---------|
| High level       |	2000    |	3000    |	4000    |	10000   |
| High alarm level |	1425    |	2250    |	2700    |	9000    |
| Low alarm level  | 	100     |	150     |	200     |	300     |

# Screens
The HMI design of our project consists of several screens. 
Main screen which is used for navigating through screens and dealing with user administration, namely login and logging out. 

![main](https://user-images.githubusercontent.com/52673837/105575359-81391480-5d84-11eb-9245-ec972ff2fc05.png)

The other page which shows the whole process is Tank Farm page. 

![tank_farm](https://user-images.githubusercontent.com/52673837/105575384-bba2b180-5d84-11eb-8888-b90877aab6c1.png)

Here we can see status of valves and pumps with colors, and the level of the tanks is illustrated. By clicking on the tank, we can navigate to separate tank pages. 

![separate_tank](https://user-images.githubusercontent.com/52673837/105575406-e7be3280-5d84-11eb-9ea0-b407d9dc68e6.png)

There is also an alarm page which shows the activated alarms.  

![alarm_page](https://user-images.githubusercontent.com/52673837/105575427-07555b00-5d85-11eb-8dad-208ef557035b.png)

And an trends page showing the trends of analog values such real level in the tanks. 

![trends_page](https://user-images.githubusercontent.com/52673837/105575460-39ff5380-5d85-11eb-837a-50a79c88ee5e.png)

There is also a pop-up screen - helpers to give additional info about alarms. 

![image](https://user-images.githubusercontent.com/52673837/105575493-86e32a00-5d85-11eb-90b2-d2b2a721fe0c.png)

To manage pump and valves we created faceplates for both, which shows status, tag number and buttons to control them. 

![faceplates](https://user-images.githubusercontent.com/52673837/105575484-6ca94c00-5d85-11eb-857f-97440544abec.png)



