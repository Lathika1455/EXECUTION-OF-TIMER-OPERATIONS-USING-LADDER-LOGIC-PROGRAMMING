# EXECUTION-OF-TIMER-OPERATIONS-USING-LADDER-LOGIC-PROGRAMMING


 #### NAME : Lathika Sree R
 #### REGISTER NUMBER : 212224040169
 #### DEPARTMENT : CSE
 #### YEAR : 1

 
# Aim:
To understand and implement timer operations in a PLC using ladder logic and verify the output for different types of timers (ON-delay, OFF-delay, and Retentive timers).

# Apparatus Required:
Programmable Logic Controller (PLC) - A PLC that supports timer functions.
PLC Programming Software - Software such as RSLogix, TIA Portal, or CX-Programmer.
Computer System - For programming and simulating the PLC ladder logic.
Input Devices - Push buttons or switches for triggering the timer operations.
Output Devices - LEDs or any other indicators to visualize the timer output.
Wires and Connectors - For interfacing input/output devices with the PLC.
Power Supply - Appropriate power supply for the PLC and peripherals.
# Theory:
Timers in PLCs are used to introduce delays in control processes. They are fundamental in operations where the timing of events is crucial, 
such as starting a motor after a delay, turning off a light after a specified time, or maintaining a state for a fixed duration.

# Types of Timers:
 1. ON-Delay Timer (TON)
Functionality:

The ON-delay timer starts timing when the input condition becomes TRUE (ON).
After the preset time has elapsed, the timer output becomes TRUE (ON).
If the input condition turns FALSE (OFF) before the timer completes, the timer resets, and the output remains FALSE.
2. OFF-Delay Timer (TOF)
Functionality:

The OFF-delay timer starts timing when the input condition turns FALSE (OFF).
The timer output remains TRUE (ON) during the preset delay time and then turns FALSE (OFF) after the time has elapsed.
If the input condition becomes TRUE (ON) during the timing process, the timer resets.
3. Retentive ON-Delay Timer (RTO)
Functionality:

The Retentive ON-delay timer accumulates time as long as the input condition is TRUE (ON).
The accumulated time is retained even if the input condition turns FALSE (OFF).
The timer continues from the accumulated time when the input condition becomes TRUE again.
A separate reset input is usually provided to clear the accumulated time.
4. Pulse Timer (TP or TONR)
Functionality:

The Pulse Timer generates an output pulse of a specific duration when the input condition becomes TRUE (ON).
The output remains TRUE for the preset duration, regardless of the input state.
5. Timer-On Interval (TONI)
Functionality:

The Timer-On Interval is a variation of the ON-delay timer but is used to measure the time interval while the input is TRUE (ON).
The timer counts up as long as the input is TRUE and resets when the input turns FALSE.

 
# Procedure:
Setup the PLC Programming Environment:

Connect the PLC to the computer and launch the PLC programming software.
Ensure all input and output devices are connected to the PLC’s I/O modules.
Create Ladder Logic for Timers:

Implement the ON-delay timer (TON) by creating a rung with an input (e.g., a push button) linked to a TON instruction. Set the preset time (e.g., 5 seconds).
Implement the OFF-delay timer (TOF) by creating a rung with an input linked to a TOF instruction. Set the preset time (e.g., 5 seconds).
Implement the Retentive Timer (RTO) by creating a rung with an input linked to an RTO instruction. Set the preset time and enable an additional rung to reset the timer when required.
Simulate the Ladder Logic:

Run the simulation in the PLC software.
Test the ON-delay timer by pressing the input button and observing the delay before the output is activated.
Test the OFF-delay timer by deactivating the input and observing the delay before the output turns off.
Test the Retentive Timer by toggling the input on and off, observing how the accumulated time is retained.
Download and Execute:

Download the ladder logic program to the PLC if available and run it.
Test the timers with the physical push buttons and observe the LEDs or other output devices.
#   Outputs:
ON-Delay Timer: The output LED or indicator should turn on after a specified delay (e.g., 5 seconds) once the input is activated.
OFF-Delay Timer: The output should remain on for the specified delay after the input is deactivated, and then it should turn off.
Retentive Timer: The output should turn on after the accumulated time reaches the preset value, and it should retain the accumulated time even if the input is turned off.


# Simulation Screenshots 

ON DELAY:

![WhatsApp Image 2025-02-28 at 16 13 14_379c23fd](https://github.com/user-attachments/assets/873a39cd-ee1e-4c54-a3d5-25f3a89d4364)

![WhatsApp Image 2025-02-28 at 16 11 09_f6fe32cc](https://github.com/user-attachments/assets/725fa535-f720-4a8e-b1f1-47786b64f827)

![WhatsApp Image 2025-02-28 at 16 13 50_db80db60](https://github.com/user-attachments/assets/9a83715a-ab07-43a9-9674-75da6ca2d91d)

![WhatsApp Image 2025-02-28 at 16 14 07_30205dc5](https://github.com/user-attachments/assets/e8d2b31e-6f28-4b8b-97c0-32fcf0f7a148)

REAL_LIFE EXAMPLES:

1.Develop a logic ladder that reads sensory data from 2 sensors and initialize the timer and switch on a output after 5 secs of delay

# Simulation Screenshots

![ex 2 ss1](https://github.com/user-attachments/assets/24059e79-d0f4-4d21-9604-127e896c19b2)

![ex 2 ss2](https://github.com/user-attachments/assets/ac8964f8-a9d2-4d24-8c82-3589864d26d7)

2.Develop a ladder logic using timer blocks to initialize the process of stamping where the operator uses its two hands to switch on the machine,the stamping duration starts after 5 seconds, select appropriate time block.

# Simulation Screenshots

![ex 2 ss3](https://github.com/user-attachments/assets/ab0c3690-eb7a-473d-934c-a2c35bd5b387)

![ex 2 ss4](https://github.com/user-attachments/assets/5aecd21e-c7ef-4135-abfa-11f527e88dbb)

# Results:
The ladder logic programs for ON-delay, OFF-delay, and Retentive timers were successfully implemented and tested.
The observed outputs matched the expected behavior of each type of timer, demonstrating the correct functioning of timer operations in PLC ladder logic.
The experiment confirms the practical application of timers in controlling process sequences and managing time-dependent operations in industrial automation.
