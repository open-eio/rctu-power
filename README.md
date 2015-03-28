# rctu-power

<img src="https://raw.githubusercontent.com/open-eio/rctu-power/master/rctu-power.png">

Microcontroller board for controlling power output to an embedded Linux system.

The board has several options for voltage input (VIN), and several options for voltage output (VOUT).  The on-board microcontroller controls mosfets which switch the VIN -- VOUT connections.  

The microcontroller can be programmed to switch in any arbitrary sequence, and sleep in between actions.  There is also an on-board set of physical switches so that, if desired, the user can dial in a particular sleep / wake timing sequence without having to reprogram the board.

### Typical use-case

A typical application of the board:


The board is programmed via the uUSB cable and a laptop to do the following, repeated sequence:

- Turn VOUT off
- Place the on-board microcontroller into sleep mode for X minutes
- Wake from sleep mode and Turn VOUT on
- Wait for X minutes, or until receive a 'sleep / done' signal from the device being powered by VOUT

### Connections

The board has three options for power input:

- Screw terminal
- JST connector (to e.g. battery or UBEC)
- USB-micro (which also doubles as microcontroller programmer)

The board has two options for power output:

- USB-A
- Screw terminal


