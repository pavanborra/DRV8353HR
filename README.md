# DRV8353HR
This design is meant to test 1xPWM mode of DRV8353 from Texas Instruments. Uses STM32F103c8t6 host controller. 

Target was to run BLDC Motor 205-35 (48v 1000w rated).  
IRFB4110 mosfets are chosen with very low ON state resistance. This leads to lower conduction losses.
TO-220 Mosfet Stage is planned that adds flexibility to add heatsink. 

STM32F103c8t6 pin planning is done using STM32CUBEMX tool. 
Project edited using STM32CUBE IDE.

DRV8353HRTAT version is selected for development. this version does not have integrated BUCK. This does not support SPI and is hardware controlled. NOTE, SPI variants offer more flexibility in modes and fault identifications. i may explore them i future. 

This project/design is developed to test 1 x PWM mode of DRV8353 SMART DRIVER SERIES. This Design expects hall inputs (from motor) for state control.

-- Features of Design --
One PWM signal for motor control from host controller.
Direction reversal through one GPIO state toggling.
BRAKING through one GPIO state toggling.
BUS Voltage and BUS current sensing.
All Phase Current sensing.


I have not incorporated Phase voltage sensing. you can download and re-use (edit) the design for your needs ( sensorless motors or motors with encoders/resolvers ). 

DRV8353 series simplifies design and control, helps us focus on BIG Picture. 
few DRV8353 variants has integrated BUCK conveter that can simplify drive design further. i have decoupled buck function (to derive 12v) for reasons. 
