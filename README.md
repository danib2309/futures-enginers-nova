# futures-enginers-nova
**Team:** Nova  
**School:** Colegio Adventista Bilingüe de David  
**Members:** Daniel Barría & Roque Samudio  

---

## 1. Team Information

* **Team Name:** Nova
* **Educational Institution:** Colegio Adventista Bilingüe de David
* **Category:** Future Engineers (WRO National)
* **Team Members:**
  * **Daniel Barría:** In charge of mechanical design, chassis assembly, and Ackerman steering management.
  * **Roque Samudio:** In charge of programming logic in LEGO MINDSTORMS EV3.

### Team Presentation
This is our first year participating in the Future Engineers category. We have prepared by analyzing the rules, overcoming design challenges, and iterating our prototype with the goal of learning as much as possible, applying real automotive engineering concepts, and doing our best on the track.

## 2. Mechanical Design and Chassis
Our autonomous vehicle is built using the LEGO MINDSTORMS EV3 platform, strictly complying with the regulatory limits.

* **Steering System:** We implemented an Ackerman steering system, which allows our robot to change direction using a single medium motor.
* **Drive System:** Traction is rear-wheel drive only; the large motor is directly coupled to the rear axle of the vehicle.
* **Wheel Design:** It features 4 wheels to evenly distribute the vehicle's weight and maximize grip on the track.

### Wiring Diagram
* **Port A:** Steering Motor (Medium Motor – Front Axle)
* **Port B / D:** Drive Motor (Large Motor – Rear Axle)
* **Port 3:** Ultrasonic Sensor
* **Port 4:** Color Sensor

### Sensor Placement
Sensors are mounted at the front of the robot for optimal obstacle detection. The ultrasonic sensor is placed 8 cm above the ground, and the color sensor is positioned 3 cm above the ground.

## 3. Strategy and Programming Logic
The vehicle's logic is programmed in a loop to repeat actions based on sensor inputs, using state switches to control steering.

* **No Obstacles:** The robot uses the ultrasonic sensor to avoid colliding with the track walls. Depending on the direction of travel (clockwise or counterclockwise):
  * *Counterclockwise:* Steering motor turns left (-25°), drive motor advances for 1 second, and steering motor returns to 25° to straighten up.
  * *Clockwise:* Steering motor turns right (25°), drive motor advances for 1 second, and steering motor returns to -25° to straighten up.
* **Open Road State:** When no obstacles are detected, the steering angle remains at 0° (straight) and the drive motor maintains constant power.
* **Green and Red Obstacle State:**
  * *Green Pillar:* Steering motor turns left (-25°), advances for 1 second, and turns right (25°) to straighten up.
  * *Red Pillar:* Steering motor turns right (25°), advances for 1 second, and turns left (-25°) to straighten up.

## 4. Bill of Materials (BOM)

| Component | Quantity | Main Function |
| :--- | :---: | :--- |
| LEGO EV3 Intelligent Brick | 1 | Vehicle brain and data processing. |
| LEGO EV3 Color Sensor | 1 | Traffic pillar detection (Red and Green). |
| LEGO EV3 Ultrasonic Sensor | 1 | Distance measuring and wall collision avoidance. |
| LEGO EV3 Large Motor | 1 | Rear-wheel drive system for propulsion. |
| LEGO EV3 Medium Motor | 1 | Steering angle control for Ackerman mechanism. |
| LEGO Technic Parts | Multiple | Beams, connectors, and axles for structural chassis. |
| Rubber Wheels | 4 | Standard tires for movement on the track. |

## 5. Engineering Journal

Our team is made up of two people, Daniel Barría and Roque Samudio. We built our vehicle from scratch, taking inspiration from different robots we saw to figure out the best shape and design for a solid build. To keep the workload balanced and avoid putting all the weight on one person, my teammate Roque handled the programming, and I (Daniel) took charge of building the vehicle.

During the first few days, we both reviewed the rules together to check the requirements. We researched steering systems and decided how it should work to get the first phase underway. Next, we brainstormed whether the shape should be elongated or compact. We ultimately chose an elongated design because a compact build would have been trickier—though not impossible—to assemble.

Once those decisions were made, I (Daniel) got to work building the vehicle using LEGO EV3, attaching the color sensors, ultrasonic sensors, and motors. I had to disassemble it several times after catching mistakes that violated the competition rules; specifically, I had installed two large motors instead of one. Fortunately, I realized the error and fixed it.

In the following days, after I finished the build, Roque started programming the vehicle. We ran into some trouble with the code when the robot kept crashing into obstacles. Finding a solution took us a while through trial and error, but we eventually solved it. We then ran test trials to see if any final tweaks were needed in the code or the physical design.

Now that the testing and adjustments are complete, all that is left is to wait for the competition and see how the vehicle performs—hoping for a great run.
