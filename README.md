Traffic Light System Specification for Gishushu Junction
1. Purpose
The Traffic Light System at Gishushu Junction aims to control traffic flow by managing light signals in a multi-lane, two-direction intersection. This system ensures the safe movement of vehicles along both the Main Road and the Cross Road, minimizing the risk of accidents and optimizing the traffic flow.

2. Scope
This specification covers the requirements, behavior, and states of the traffic light system for the Gishushu Junction, assuming two main directions: Main Road and Cross Road. Each direction has three light signals (Red, Yellow, Green).

3. System Requirements
3.1 Functional Requirements
Traffic Light Control: The system should control lights for two directions:

Main Road
Cross Road
Traffic Light Phases:

Each direction has the following phases:
Green: Vehicles can proceed.
Yellow: A warning phase indicating the light will turn red.
Red: Vehicles must stop.
State Transitions:

The system cycles through the following states:
Main_Red_Cross_Green: Main Road is Red, Cross Road is Green.
Main_Red_Cross_Yellow: Main Road is Red, Cross Road is Yellow.
Main_Green_Cross_Red: Main Road is Green, Cross Road is Red.
Main_Yellow_Cross_Red: Main Road is Yellow, Cross Road is Red.
Timer-Based Transitions:

Each state has a specific duration, after which it transitions to the next state. Timers are set as follows (example timings):
Green Phase: 60 seconds
Yellow Phase: 5 seconds
Red Phase: Varies based on other road's green and yellow phases
Synchronization:

Transitions between states are synchronized to prevent both directions from having green lights simultaneously, avoiding collisions.
