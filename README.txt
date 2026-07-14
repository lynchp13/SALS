# SALS

## Purpose
This LabView VI controls and automates testing of tissue samples on the SALS testing rig in the basement of the Parsons Building Trinity College Dublin.

At a very high level it controls the precise position a laser interacts with a test sample and captures an associated images, which can be used to determine useful characteristics of the test sample.

## Hardware Requirements
- Camera: USB Webcam
- NI DAQ device: NI USB 6501
- Other hardware: Laser

## Software Requirements
- LabVIEW version:2024 Q1

## How to Run
1. Open SALS.lvproj
2. Open SALS.vi
3. Configure...
4. Run...

## Project Architecture
Brief explanation of the overall program:
- State machine
	- Setup - Start tasks to operate NI USB 6501 & Webcam
	- Configure - Take configuration params and prepare array for test
	- Jog - Pretest equipment control for the purpose of preparation
	- Move - Mid test move sample state
	- Capture - Mid test capture image state
	- Idle - State to allow for checking the state of buttons and to linger in when not actively doing something else
	- Finish - Close open files, shut down created tasks, etc

## Known Issues
...

## To do
-  Add additional documentation
-  Add button to allow you to reconfigure for the next test without shutting down.
-  Add button to allow an image capture without starting a test
-  Run performance tests on the code
-  Run VI Analyzer

## Version History
See Git/GitHub commit history.