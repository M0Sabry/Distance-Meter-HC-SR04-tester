***********************************
# Distance Meter/HC-SR04 tester
***********************************
## this circuit is designed to mesure distance or test hc-sr04 ultrasonic distance sensor without the need of any microcontroller.

* its function is based on 556 timer (dual 555 timers).

* first 555 timer is operationg in monostable mode and used to generate a 10us high pulse to triger the ultrasonic distance sensor once the push button is hit.

* the 10us high pulse is also used to reset all counters in the circuit.

* second 555 timer is operating in Astable mode to generate square wave (lets call it clock) with time period equivalent to 1cm indicated by the ultrasonic distance sensor.

* after the ultrasonic distance sensor is triggered it echo a high pulse output, the time of high output IO duration is the time from sending ultrasonic to returning. 

* the echo signal is anded with the clock generated by 555 timer allowing only the number of clock cycles indicating the distance measured by the sensor.

* these clock cycles are passed to three consecutive 4026 counters with 7-segment display driver to display the distance as 3-digt number.
