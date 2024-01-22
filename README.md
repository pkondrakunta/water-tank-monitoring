# water-tank-monitoring
Connected Devices project for water tanks monitoring (summarization repo). 

## Description
An automated version of the typical water tank. Using a water level sensor we can monitor the level of water in the tank. ANy any given instant we can take a look at the water level. We can also atuomatically create events that will turn on the motor to fill up the tank and turn off the motor to stop filling it once it is full.

## What - The Problem 
In India, the city's water department releases water supply on specific days of the week. Very limited communities receive 24 hours of water. The water that needs to be consumed by a house has to be accessed and stored during these timings. Each household has a water tank and corresponding motor that need to be manually turned on when there is supply (the supply timings and days are subject to change). 
While the water fills up the tank when the motors is turned on, there is no way a person can determine how measure the level of water without physically going to the tank and seeing the depth of water. The only indication of that the water is filled, is the sound of water overflow from the tank. If no one turns off the motor once the tank is full, the overflowing water is wasted turned turned off (in the household or from the city's supply).

## Why - Who Cares? 
Water shortage is real in India (and everywhere. Obviously we don't pay attention to this as much). It is extremely important to avoid any wastage of water resources. 
For the households, monitoring the water level in the tank and the schedule of the city's water supply is an important chore. If I missed consecutive water releases from the supply, I may not have water running from the taps until my water tank is filled! At the same time, it is a hassle to keep track of the water level in the tank (each time, I have to physically see the level or wait hear the overflowing sound of water from the tank's location). Tackling this problem statement, can significantly impact how we handle this important chore of water access in each household.

## How - Expected Technical Approach

Using a water level sensor and a servo motor to handle a valve to the water tank, we can automated the manual task of water tank filling. Not only can we monitor the water level without the need to physically access the tank, we can also trigger the turn off of the sensors remotely. Furthermore, we can automate the process using event triggers to turn off water supply after it touches 95% (for example).
![project_architecture](https://github.com/pkondrakunta/water-tank-monitoring/blob/main/project_architecture_final.png)

At the Edge Tier, the architecture diagram depicts constrained device’s measurement of water level in the tank. These sensor readings are passed to the gateway device for processing and transmission to the Cloud Tier.

When the city supply schedule is released, the person can trigger activating the servo motor to fill up the tank. For a future use case, we can also use a sensor in the pipe that releases city's water supply to indicate to the user that the supply is here! If the measured water level is above a threshold value, the gateway device instructs the constrained device to activate the servo motor to stop water flow into the tank.

All this data collected, can be referenced later to analyse the frequency of water fills, and using the time between turn on/off, we can measure water consumption of the house and analyse causes of more/less comsumption. Maybe we can even detect invisible leaks if my consumption has been a lot lately without any reason!

# My Java Components
https://github.com/pkondrakunta/connected-devices-gda

# My Python Components
https://github.com/pkondrakunta/connected-devices-cda

## Results - Expected Outcomes 

Here are some metrics to determine the success of the project.

* The ability to monitor the water level using a cloud dashboard (on the web/mobile) without the need to physically access the tank
* The ability to programmatically trigger the turn on/off of the servo motor (which is connected to the valve) remotely on demand
* THe ability to automate the turn on /off events using threshold triggers (like turn off motor when tank reaches 90% or 95%)


> Here is a Kanban breakdown of the tasks completed:
> [Programming the IoT Kanban Board](https://github.com/orgs/programming-the-iot/projects/1)
