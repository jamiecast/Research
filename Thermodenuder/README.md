# Low Cost Thermodenuder

This repository covers the work I did in developing a low cost thermodenuder as part of my research experience at Colorado State University's Lab for Air Quality Research (LAQR). The goal was to redesign a common aerosol instrument with as low of cost components as possible, with the idea of making it easier for other to build and maintain what is normally a very expensive piece of equipment.

## What is a thermodenuder?
A thermodenuder is an instrument which helps determine the volatility of an organic aerosol. By passing the aerosol through a heated tube, a portion of the aerosol will change from the particle to vapor phase. These vapors can then be absorbed by activated charcoal cloth, removing a fraction of the original aerosol. The concentration of the aersol can be measured using an external instrument both before and after it is run through the thermodenuder. As the temperature of the heated tube is changed, the portion of the aerosol that is removed will also change. This can be plotted on a graph called a thermogram, where the x axis is the temperature of the heated line, and the y axis is the mass fraction remaining.

## How does this particular one function?
Since the goal for this project was to make this device as cheaply as possible (while still being reliable), a variety of consumer electronics were used. The main computations is done using an ESP32 microcontroller, which controls a pair of solenoid valves that control the flow of air between a heated tube and a control (unheated) tube. The heated tube is heated using an AC heating strip that can be controlled through a relay. By changing the pulse width of the signal connected to the relay, the output of the heating strip can be adjusted. Using a pair of thermocouples located roughly 1/3 and 2/3 down the heated portion of the tube, a PID loop is able to control the heating automatically.

Additionally, the device is able to be controlled and monitored remotely through an IoT connection. This allows for even easier operation than many commercial thermodenuders.
