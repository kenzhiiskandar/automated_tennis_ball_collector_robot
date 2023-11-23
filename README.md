# automated_tennis_ball_collector_robot

This project aims to design and build a compact autonomous robot to search, retrieve, and return tennis balls in a specific arena provided.

https://github.com/kenzhiiskandar/automated_tennis_ball_collector_robot/assets/120554498/7be5cba8-c8c6-4ee8-a126-41c91ef14f99

## Robot Overview

![Uploading image.png…]()


## Robot Mechanical Design
![image](https://github.com/kenzhiiskandar/automated_tennis_ball_collector_robot/assets/120554498/127cd687-277c-48cf-9114-68d4fab68182)

## Robot Drive Systems
The robot utilizes the Vex ARM Cortex-based Microcontroller for electrical control management. The robot implements a robust 2-wheel drive system, driven by Vex Continuous Rotation Motor, and a caster wheel at the front of the robot. Its energy requirements are efficiently met by the NiMH Battery Pack boasting a voltage rating of 7.2V and a capacity of 3000mAH.

## Robot Searching Systems
The robot employs two IR Sharp Distance Sensors placed at its front (left and right) to detect the ball, while relying on the Digital Compass 1490 for navigation.

When searching, the robot follows a sequence of movements: moves straight, then turns left and right. If it locates a ball, it collects the ball and proceeds to return it. If no ball is found, the robot persists in its search routine: moving straight, turning left, and then right. To ensure comprehensive coverage of the arena, the search algorithm utilizes the compass for guidance. The direction of search depends on the robot's orientation and boundary detection, following this pattern:
(a) Searches forward in the north direction until it hits the yellow boundary line,
(b) Searches to the west until it encounters another yellow boundary,
(c) Continues the search southward,
(d) Explores eastward before returning to (a).

![image](https://github.com/kenzhiiskandar/automated_tennis_ball_collector_robot/assets/120554498/3e32d3ac-0f4e-470a-9985-f3ac2f1e39f2)

## Robot Return Systems
During the return phase, the robot orients itself northward, using the digital compass, and reverses until it contacts the boundary of the box. The detection of this boundary is indicated by the activation of limit switches situated at the back of the robot (both left and right). After hitting this boundary, the gate at the back will open, then the robot resumes its search.

## Robot Boundary Line Detection Systems
The robot utilizes IR Line Tracking Module Sensors mounted at its four corners to detect the boundary lines. Whenever any of these sensors detect the boundary line, the robot triggers specific maneuvering mechanisms to re-adjust its position back within the arena boundaries. Additionally, these boundary line detection systems play a crucial role in guiding the navigation and execution of the searching algorithm.
