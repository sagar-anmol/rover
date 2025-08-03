

# Autonomous Rover

🧭 Navigation System
-------------

The navigation system for the autonomous rover is designed to compute and follow a GPS-based route from the rover's current location to a user-defined destination. It integrates third-party routing APIs for initial path planning and performs in-house logic to manage GPS inaccuracies and route validation. The system is modular, enabling future replacement with a fully self-hosted OpenStreetMap (OSM)-based engine.
## Overview

🔹 Initial Localization
-------------

At time t=0, the rover continuously fetches its current geographic coordinates using a standard GPS module. This forms the base reference point for route computation.

🔹 User Interaction and Destination Input
-------------
The system exposes a local server endpoint where a user can input the desired destination. Upon receiving the request, the destination is geocoded into coordinates and paired with the rover’s current position to define a navigation query.

🔹 Third-Party Routing Integration
-------------
![](https://i.sstatic.net/uYedd.png)
>the img is not the write depiction of what we are doing

The paired coordinates are transmitted to a third-party navigation provider (currently testing with Google Maps and its competitors). The service returns a sequenced list of intermediate waypoints (coordinates) representing the recommended path.

🔹 Route Preprocessing and Turn Detection
-------------
Post-receipt, the returned coordinate sequence undergoes lightweight preprocessing. Every set of three consecutive points is analyzed to detect significant heading changes indicating a turn. Identified turning points are cached locally for decision-making during motion.

🔹 Checkpoint Handling and Error Mitigation
-------------
![](https://img.gta5-mods.com/q95/images/race-timer/4b1776-lapTimer3.jpg)
>checkpoints idea taken from games logic
Given that the onboard GPS module is not RTK-enabled and has a positional error margin of a few meters, the system employs geofenced coordinate ranges instead of exact positions. These act as checkpoints for route validation and deviation handling.

🔹 Visual Verification at Turns
-------------
As the rover approaches a predefined coordinate range with a turn, it activates the YOLOv8-based road segmentation model to visually verify road geometry and make precise turn decisions. (See [Driving Mechanism](https://github.com/sagar-anmol/rover/blob/main/DrivingMechanism/iindex.md "Heading link") section for full integration details.)
