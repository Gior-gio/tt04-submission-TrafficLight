![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg)

# Traffic Light - UIS

## How it works

This is a Finite State Machine (FSM) that utilizes an instantiated module of the “CLK
Frequency Divider” by Ramón Sarmiento to perform internal counting for a traffic light
control system. Its state diagram is as follows:

![image](https://github.com/Gior-gio/tt04-submission-TrafficLight/assets/68038923/7c1f6fd9-e620-4884-8589-ee59f7ba9be5)

In the provided source code from this 
[tinytapeout submission](https://github.com/RamonSsc/tt04-submission-Vfreq), 
you can find a signal called "count," which increments every second due to frequency division using a module. 
Additionally, in the "src" folder, there is a testbench for the circuit. When running this testbench, 
the following results are obtained in the console:

![image](https://github.com/Gior-gio/tt04-submission-TrafficLight/assets/68038923/b41a2c0e-3a34-4d83-8a27-f51e6f75ec70)

## How to test?

Set the first input to “1” and await the activation of the Red light. It will remain active
for 30 seconds, provided the correct frequency is employed. Afterward, it will transition
to the Green state within 3 seconds, remaining in this state for an additional 20 seconds.
Finally, it will transition back to the Red state over the course of 3 seconds.
