# Temperature Control for TGI
This is a tutorial for temperature control of Peltier elements for Thermal Grill Illusion intensity control

# Features
In thermal grill illusion (TGI) generation using warm and cold stimuli, continuous cooling of the cold stimulus enables the control of perceived pain intensity. 
This tutorial will guide you through the temperature control methods for Peltier elements to achieve TGI intensity control and briefly discuss its application to VR environments 

 
# Requirement
Peltier elements × 6

Raspberry Pi 4 Model B

The following circuits for temperature measurement circuits for the Peltier elements (× 6)
![Image](https://github.com/user-attachments/assets/0e84643c-10f6-4672-8f42-789a341d92fb)

# Usage
By using "Experiment1.py", the Peltier elements used for cold stimulation can be continuously cooled from 25°C to 20°C over a specified duration. Among the six Peltier elements,
two are maintained at a constant 41°C, while the other four are initially held at a constant 25°C before commencing cooling to 20°C. 
In the code, X, Y, Z, L, M, and N distinguish the six Peltier elements, which are arranged as shown in the figure below.


![Image](https://github.com/user-attachments/assets/c079b54a-216a-45f1-9938-fc2c201fed83)

"Experiment2.py" is a tool for synchronizing the temperature changes of the Peltier elements with changes in the VR environment. 
This code is designed to transmit the elapsed time since the start of the Peltier element temperature control to Unity using socket communication, 
thereby enabling synchronization with the VR application running within Unity.

SocketManager.cs" is the code Unity uses to receive elapsed time data from the Raspberry Pi.
"colorsocket.cs" and "scalesocket.cs" are the codes that modify objects within the VR environment based on the elapsed time data.
TGI_Display_Peltier_Bracket is the CAD/STL file for the bracket designed to secure the Peltier element in the TGI display.

# Note
Please ensure that the temperature of the Peltier elements does not overshoot and reach temperatures harmful to the human body.

To prevent damage to the Peltier elements, it is recommended to specify a cooling time of 5 seconds or longer for cooling from 25°C to 20°C.
 
# Author
 Shinnosuke Hori
 
 Department of Pure and Applied Physics, Graduate School of Advanced Science and engineering, Waseda University
 
 noether@toki.waseda.jp
 
# License
 
This is under [MIT license](https://en.wikipedia.org/wiki/MIT_License).


