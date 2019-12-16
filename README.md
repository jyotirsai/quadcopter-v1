# quadcopter-v1

[Image]

# Introduction

A Quadcopter is a helicopter with four rotors. A rotor is the main rotating part of an electrical machine such as a propeller blade. The rotors provide lift and propulsion for the quadcopter via electromechanical energy conversion. 

There are three dimensions in which a flying object can move through: pitch, yaw, and roll.

<p align="center">
<img src="axis.png" width="500px" height="500px" align="center">
</p>

Pitch refers to moving the nose of an aircraft up and down.
Yaw refers to moving the nose of an aircraft left and right.
Roll refers to tilting (rolling) an aircraft side to side.

In order to produce lift and propulsion, a rotor must produce thrust and torque about its (the individual rotors) center of rotation. Gravity as well as a drag force will act upon the quadcopter and will have to be overcome by the rotors in order to propel the machine. 

<p align="center">
<img src="rotors.png" width="250px" height="250px">
</p>

The above figure shows the direction of rotation of the four rotors. In a quadcopter, pairs of rotors will rotate in opposing directions in order to cancel out any unwanted rotational force. If all four rotors were to spin in one direction, let’s say the clockwise direction, then this would generate a non zero rotational force and would thus cause the quadcopter to spin clockwise about its yaw axis. 

To make a quadcopter hover, its rotors must be spinning at the same angular speed. Two of the rotors will spin clockwise, and the other two will spin counter-clockwise. The forces created by the rotors will cancel each other out and create a hovering effect. 

To adjust the yaw (move aircraft left and right), more thrust would be applied to the rotors rotating in the desired direction.

In order to create a pitch or roll adjustment, more thrust must be applied to a single rotor while simultaneously reducing the amount of thrust sent to the rotor that is diametrically opposite. The quadcopter will dive or tilt in the direction of the rotor that receives less thrust. 

<p align="center">
<img src="quadrotor-pitch.png" width="250px" height="250px">
</p>

# Mechanical Components

In a quadcopter, the main mechanical component is the frame. The frame is responsible for mounting and connecting all the components together. Frames differ in shapes, dimensions, and materials. A stiff frame is ideal for flight since this reduces warping and bending. The stiff material must not be too brittle since this can cause easier breakages during crashes. The frame must also be light in order to reduce the needed thrust. Heavier frames will need stronger motors. The material should also be able to minimize vibrations as this can damage electrical components. The frame can be broken down into the following: Centre plate, four arms, four motor brackets.

The centre plate is where all of the electrical components are placed.
The four arms connect to the centre plate (some components can be placed here too).
The four motor brackets hold the motors on the arms. 
