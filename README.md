## QUICK START INSTRUCTIONS
As Arduino UNO Q have the easiest way to make a python and C++ project, all you need is just download the zip file on the code foland import him on the Arduino APPLAB and you can enjoy your project the fastest way to start.

![Mimicry](/img/p1.JPG)
![Mimicry](/img/robot-image.png)
![Mimicry](/img/robot1.JPG)
## What is going on ?

Generally, when coding an algorithm for a robot, it is deterministic and predictable; in a sense, the robot's reaction to a specific situation is known in advance. While this characteristic offers a significant advantage, it can prove to be a double-edged sword if the robot encounters an unforeseen situation. To solve this problem, scientists have created Machines Learning Algorithms.

## What is Mimicry ?
Mimicry is an Open source Supervised Machine Learning mobile robot based on Arduino UNO-Q board. 
It use four STS3215 motors for movement, three ultrasonic sensors for obstacle detection, and an Arduino UNO-Q board as the onboard computer.

 During the data collection phase, the robot is manually controlled while sensor measurements and corresponding movement commands are recorded in a CSV dataset. This dataset is then used to train a KNN model capable of predicting the appropriate movement based on the current sensor readings. A Streamlit web interface provides manual control, dataset collection, autonomous operation, sensor monitoring, and dataset visualization, making the system accessible and easy to experiment with. The project aims to demonstrate a simple and reproducible approach to embedded machine learning and autonomous navigation using low-cost hardware.

![Mimicry](/img/robot%20description.png)

Mimicry have overall dimensions of 212 × 159 × 83 mm (L × W × H).

![Mimicry](/img/robot-image_plan.png)

## System Overview

The system is composed of three main layers: the hardware, the embedded software, and the web application. The Arduino UNO Q manages the ultrasonic sensors and STS3215 servomotors, while communicating with the Streamlit application through the Arduino Router Bridge. The web interface allows the user to manually control the robot, collect sensor and movement data, train and run the KNN model, and visualize the collected dataset. During autonomous operation, the three ultrasonic measurements are provided as inputs to the KNN model, which predicts the movement command to be executed by the robot. A watchdog mechanism is also implemented to improve safety by automatically stopping the robot when communication with the control application is interrupted.


![Mimicry](/img/chart.png)


## Hardware

Hardware Architecture

it composed with an Arduino UNO Q, three HC-SR04 ultrasonic sensors, four STS3215 servomotors, and a Waveshare serial bus servo driver. The three ultrasonic sensors are connected to the Arduino and provide distance measurements from the left, center, and right sides of the robot. The Arduino communicates with the Waveshare driver, which controls the four STS3215 motors for the robot's four-wheel drive. The motors and the electronics are supplied by an external power source.

Note: The schematic uses an Arduino UNO image instead of the Arduino UNO Q, as an appropriate UNO Q image was not available when the diagram was created. The wiring and functional connections represented in the diagram correspond to the project architecture.

![Mimicry](/img/circuit.png)

