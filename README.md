# quadcopter-v1

[Image]

# Introduction

A Quadcopter is a helicopter with four rotors. A rotor is the main rotating part of an electrical machine such as a propeller blade. The rotors provide lift and propulsion for the quadcopter via electromechanical energy conversion. 

There are three dimensions in which a flying object can move through: pitch, yaw, and roll.

<p align="center">
<img src="axis.png" width="500px" height="500px" align="center">
</p>


<ul>
  <li><strong>Pitch</strong> refers to moving the nose of an aircraft up and down.</li>
  <li><strong>Yaw</strong> refers to moving the nose of an aircraft left and right.</li>
  <li><strong>Roll</strong> refers to tilting (rolling) an aircraft side to side.</li>
</ul>


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

<ul>
  <li>The centre plate is where all of the electrical components are placed.</li>
  <li>The four arms connect to the centre plate (some components can be placed here too).</li>
  <li>The four motor brackets hold the motors on the arms.</li> 
</ul>

Common materials used for frames:

<ul>
<li> Wood - The prominent benefit of using wood is the fact that it is very inexpensive and easy to replace. It will reduce build time. Also fairly rigid. However, it can be aesthetically unappealing </li>
<li> Carbon Fiber - Very tough and extremely lightweight material, this will allow for better flight dynamics and less needed thrust. Expensive option. Best option. </li>
<li> Plastic - Not as ideal since it tends to bend. 3D printing a frame can be useful for small builds. </li>  
</ul>

The size of a frame is usually measured as the longest distance from motor to motor in mm. Frames less than 150 mm are micro frames. 



# Motors

<p align="center">
<img src="motor.gif" width="250px" height="250px">
</p>

In a DC motor, a spinning armature called the rotor is surrounded by stationary permanent magnets called the stator. The armature (rotor) contains an electromagnet, which creates a magnetic field when electricity is run through it. The generated magnetic field attracts and repels the magnets in the stator causing the armature to spin. In order to keep the armature spinning, the poles of the electromagnet must be changed, which is what the brushes are responsible for. Unfortunately, brushes create a number of inefficiencies such as wear and tear and speed reduction. 

In a brushless DC motor, the permanent magnets are on the rotor and the electromagnets (called poles) are on the stator. A computer is then used to charge up the electromagnets as the shaft turns. The greater the number of poles the more precisely the motor can be controlled. Brushless motors have three wires and depending on their connections, can change the motor spin direction. Quadcopter motors have KV ratings which depicts the RPM per 1 volt applied to the motor. The larger the weight of the quadcopter, the lower the KV rating for the motors. For a lightweight and fast quadcopter, you would use a high KV motor for high rpm. For a heavier quadcopter, you would use a low KV motor for low rpm and more torque. Motor and propeller combinations should be able to generate twice the weight of the craft in thrust. The motor shaft diameter will determine the type and size of propellers.

An identifying feature of a brushless motor is if you see three wires coming out.

The size of a brushless motor is identified by a four-digit code that describes the dimensions of the stator in mm. 

<p align="center">
<img src="brushless-motor.png" width="600px" height="300px">
</p>



# Propellers

Lightweight and fast quadcopters should have high Kv motors with small propellers. Heavyweight quadcopters should have low Kv motors with large propellers. The higher the Kv rating, the smaller the propeller diameter. 

Smaller propellers allow for quicker flight but reduces efficiency. Large propellers allow for steadier flight, lifts more weight, and uses more power.

Propellers are usually defined by two sizes “500 x 200 mm”, the first size indicates the diameter of the propeller and the second size (called pitch) indicates the linear travel distance in a single rotation.

Higher pitch means a slower rotation which increases speed and uses more power.

Lower pitch propellers can generate more torque and your motors will consume less current.

Propeller size is linked to thrust, responsiveness, and the amount of control the quadcopter will have in the air.



# Electronic Speed Controller Circuits (ESCs)

These are circuits that control a motors speed, direction, and braking. The circuits offer high AC power to the motors.

These are needed for each motor.

ESCs interpret signals and regulate the variation of motor speed.

ESCs regulate the amount of power that goes to the motor. ESC’s apply voltage to a motor. They turn the motor on and off to create a ratio of on and off time. This varies the average voltage induced onto the motor. The switching is controlled by a microprocessor and carried out by transistors called MOSFETs or FETs.

A brushless ESC is used to connect to a brushless motor, they provide superior performance to the brushed ESCs.

ESC’s have three wires that connect to the three wires on the brushless motor. Two other wires connect to the power distribution board. Three smaller wires connect to the flight controller. The ESC should be able to handle the maximum current that your motors use.

Some features:
<ul>
  <li>Brake - Used to force the motor to stop turning once ESC stops delivering power</li>
  <li>Soft Start - Indicates that the control will go from off to full throttle slowly and not instantaneously</li>
  <li>Automatic Cut-off - Power is cut from the motors when battery is low and is reserved for radio signals</li>
</ul>

Most ESC’s are controlled by onboard 32-bit processors running firmware called BLHeli_32 or KISS. 32 bit ESC’s can communicate with faster digital protocols and are capable of things like controlling LEDs, changing motor direction, and telemetry data.

<p align="center">
<img src="ESC.PNG" width="500px" height="250px">
</p>
