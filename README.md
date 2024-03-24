# Formula_Student_Transponder
This repository contains the Arduino sketch for a transponder system designed for Formula Student vehicles. The system utilizes an HC-SR04 ultrasonic sensor to record lap times as vehicles pass a designated point on the track.

Features:
Ultrasonic Sensor Integration: Utilizes the HC-SR04 ultrasonic sensor to detect vehicles passing by.
Real-time Lap Timing: Measures the time taken by vehicles to complete a lap accurately.
Serial Communication: Sends lap number and lap time data to the Serial Monitor for monitoring and logging.

Components:
HC-SR04 Ultrasonic Sensor: Used for distance measurement and vehicle detection.
Arduino Board: Executes the transponder logic and controls the sensor.
Serial Monitor: Displays lap number and lap time information for monitoring.

How It Works:
The ultrasonic sensor emits ultrasonic pulses and measures the time taken for the pulses to bounce back after hitting an object.
When a vehicle passes within range of the sensor, it triggers the sensor, and the Arduino calculates the time taken for the pulses to return, determining the distance of the vehicle.
If the detected distance is below a certain threshold (300 units), the Arduino registers a lap. It calculates the lap time based on the difference in time since the last lap.
Lap number and lap time information are sent to the Serial Monitor for real-time monitoring or logging.

Usage:
Connect the HC-SR04 sensor to the specified pins (trigPin and echoPin) on the Arduino board.
Upload the provided sketch to the Arduino board using the Arduino IDE or compatible software.
Open the Serial Monitor to view lap number and lap time data as vehicles pass the designated point.

Note:
Adjust the threshold distance (300 units) and any other parameters as needed to suit the track and vehicle requirements.
