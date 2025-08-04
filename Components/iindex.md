1. Raspberrypi 4B
Specs:
Broadcom BCM2711 Quad-core Cortex-A72 (ARM v8) 64-bit SoC @ 1.5GHz,
RAM: 2GB/4GB/8GB LPDDR4-3200 (depending on your model),
Dual-band 802.11ac wireless, Bluetooth 5.0,
Gigabit Ethernet + 2 × USB 3.0 and 2 × USB ,2.0 ports
40 GPIO pins for sensor/motor interfacing,
HDMI support for debugging and display,
Operating System: Raspberry Pi OS / Linux-based OS.

2. GPS Module (Neo 6M / USB GPS Receiver u-blox 7)
Role: Provides real-time latitude and longitude for location tracking.
Specs:
Satellite systems: GPS, Galileo, GLONASS (u-blox 7),
Baud rate: 9600 by default,
Communication: UART (Neo 6M), USB (u-blox),
Accuracy: Up to 2.5m,
Supports NMEA protocol,
Compatible with gpsd, gpsmon, cgps, PythonGPS Module (Neo 6M / USB GPS Receiver u-blox 7),
Role: Provides real-time latitude and longitude for location tracking.
Specs:
Satellite systems: GPS, Galileo, GLONASS (u-blox 7),
Baud rate: 9600 by default,
Communication: UART (Neo 6M), USB (u-blox),
Accuracy: Up to 2.5m
Supports NMEA protocol,
Compatible with gpsd, gpsmon, cgps, Python.

3. Motor Specifications
Model: GF12-N20 Motor 12V200rpm Gearbox,
Rated voltage: 12V,
Rated current: 0.055A,
Locked rotor current: 0.45A,
Rated torque: 0.09kg.cm,
Locked rotor torque: 0.7kg.cm,
Rated output power: 1.5W,
No-load speed: 66±10%RPM,
Motor size: 34*12mm,
Output shaft size: 4*10mm.

4. Power Bank
(Power Supply for Raspberry Pi and Components)
Role: Portable energy source for Raspberry Pi and low-power peripherals.
Specs: Output: 5V 3A via USB-A or USB-C,
Capacity: 10,000mAh – 20,000mAh (recommended),
Rechargeable via micro-USB or Type-C,
Built-in protections (short-circuit, overcharging).

5. Yaw Movement of Wheels
(Direction Control of Vehicle - Turning Left/Right)
Role: Enables turning capability of the vehicle (steering).
Achieved By:
Differential Drive: Varying the speed of left/right wheels.
Eg: Left wheels move slower → vehicle turns left.
Servo-controlled steering (if implemented).
Specs:
Based on motor driver logic (L298N) and pulse width modulation (PWM),
Real-time control via Python or Arduino code,
Used In: Turning at intersections, path correction based on Google Maps route.

6. Raspberry Pi Camera
(For Road Detection, Obstacle Detection, or ML Input)
Role: Captures live video feed or images used in: Road line detection, Object detection (e.g., stop signs), ML-based decision-making
Specs:
Module: Pi Camera v2.1,
Resolution: 8MP,
Video: 1080p30 / 720p60 / 640x480p90,
Interface: CSI port on Raspberry Pi,
Compatible with OpenCV, TensorFlow, PyTorch
Optional: USB camera for flexibility in placement.

