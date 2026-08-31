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
