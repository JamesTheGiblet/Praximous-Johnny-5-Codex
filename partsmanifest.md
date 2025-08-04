# Johnny 5 "Number 3" - Parts Manifest

This document is the complete and annotated blueprint for all physical components required to build Johnny 5 "Number 3." Each component is part of a larger subsystem, carefully selected for its role in the ritual of construction.

---

## **Table of Contents**
* [1. Chassis & Motion Foundation](#chassis-motion)
* [2. Core Electronics ("The Brains")](#core-electronics)
* [3. Power Management](#power-management)
* [4. Audio & Communication](#audio-communication)
* [5. Actuators & Movement](#actuators-movement)
* [6. Sensors & Visuals](#sensors-visuals)

---

### <a name="chassis-motion"></a> 1. Chassis & Motion Foundation
* **chassis.kit**: Echwave RC Tank Smart Robot Tank Car Kit (with rubber tracks & dual 130 DC motors)
* **motor.driver**: L298N Motor Driver Module or equivalent
    * *Note*: Controlled by the Base Pi for motor speed and direction.
* **power.protection**: PPTC Polyfuses (x3)
    * *Note*: One per voltage rail (5V, 3.3V, motor power) for overcurrent protection.

---

### <a name="core-electronics"></a> 2. Core Electronics ("The Brains")
* **brain.body**: Raspberry Pi 5 (4GB or 8GB)
    * *Note*: The central command hub for high-level tasks.
* **brain.base**: Raspberry Pi Zero 2 W
    * *Note*: Dedicated to low-level motor control for the chassis.
* **brain.head**: ESP32-CAM Module
    * *Note*: Handles computer vision, sensors, and expressive lights.
* **inter-brain.comms**: SPI Bridge (e.g., HyperSPI topology)
    * *Note*: Provides high-speed, reliable communication between the three brains.
* **heartbeat.module**: Chassis-mounted LED
    * *Note*: A visual diagnostic tool, synced to uptime or CPU load.
* **cooling.kit**: Official Raspberry Pi 5 Active Cooler
    * *Note*: Essential for thermal management during intensive tasks.
* **storage**: microSD cards (x3)
    * *Note*: One for each brain.

---

### <a name="power-management"></a> 3. Power Management
* **battery**: High-capacity 2S or 3S LiPo
    * *Note*: The primary power source, mounted in the chassis.
* **distro.board**: Evemodel PCB007
    * *Note*: For clean and organized power distribution.
* **power.converters**: Buck Converters (x3 or more)
    * *Note*: To create stable 5V, 3.3V, and 3–7V power lines.
* **fuse.layering**: Inline PPTC polyfuses on all voltage rails
    * *Note*: Provides redundant protection for all components.

---

### <a name="audio-communication"></a> 4. Audio & Communication
* **speaker**: 8-ohm, 3W mini speaker
* **amplifier**: Adafruit MAX98357A I2S Class D Amp
    * *Note*: Ensures crisp, clear voice output.
* **microphone**: MAX9814 Electret Mic Breakout (with auto gain control)
    * *Note*: Provides a consistent audio input signal for speech-to-text.
* **voice.synthesis**: (Choice A) Gravity TTS Board or Emic 2 Voice Module (for hardware-based TTS)
    * *OR*: (Choice B) Software-based TTS (e.g., Pico TTS)
* **connectors**: Assorted JSTs (color-coded, a "glyph system" for connections)
* **jumper.wires**: Male-to-male and male-to-female sets

---

### <a name="actuators-movement"></a> 5. Actuators & Movement
* **shoulders**: 2× High-torque metal gear servos (20–25kg.cm)
* **elbows**: 2× Medium-torque servos (10–15kg.cm)
* **wrist**: 1× Standard servo (5–10kg.cm)
* **claws**: 2× Micro servos (2–5kg.cm)
* **neck**: 3× Feedback-enabled Linear Actuators (with potentiometer or Hall sensor)
    * *Note*: A crucial detail for precise neck positioning.
* **motion.dampening**: Springs, rubber bushings for joints
    * *Note*: Reduces servo strain and creates smoother movement.

---

### <a name="sensors-visuals"></a> 6. Sensors & Visuals
* **eyes.mouth**: LED Strip/individual LEDs (mouth), OLED screens/LEDs (eyes)
* **navigation**: HC-SR04 Ultrasonic Sensors (×2–3)
* **balance.gesture**: MPU6050 IMU sensor
    * *Note*: Allows for gesture-based control and awareness of the robot's orientation.
* **vision.tracking**: ESP32-CAM (on a pan-tilt mount) with ESP-WHO or OpenCV
    * *Note*: Provides the ability for object and motion tracking.

---
