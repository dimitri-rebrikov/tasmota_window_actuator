# tasmota_window_actuator
This project implements a [tasmota](https://tasmota.github.io) based windows actuator.
The implementation allows steer the window both directly using buttons and remotely over the functionalities provided by tasmota (MQTT, HTTT, Web UI).

## Circuit Diagram

### Relay 1
Powers the 12v power supply only if needed

### Relay 2
Switch on/off the motor. The Relay 1 is not enough as the remaining energy of the power supply continues to power the motor even if the power supply by itself is cut off the current. So Relay 2 ensures immediate stop of the motor.

### Relays 3 and 4 
Are the classic power polarity inverting circuit. Together they let the motor turn into the one or another direction.

### Push Buttons "OPEN" and "CLOSE"
The buttons are implemented with the pull-up resistor.

### 8 x RGB LED WS2512b
This is an optional/changeable component to visualize the current status of the window.
In the presented implementation it is a stripe of 8 RGB LEDs.

### Fuse and Varistor
Shall protect the circuit.

### Motor
I used a linear actuator for 12v

### WeMos D1 mini
Is the "Brain" of the circuit.


