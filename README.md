# Human Infected Zombie

An entry to the [Square Inch Project](https://hackaday.io/project/7813) contest on Hackaday.io

![PCB](https://raw.github.com/SmallRoomLabs/HIZ/master/Images/HIZ-Top.png)

## Hardware
The board is a small (25 mm square) PCB with an IR transmitter and receiver for communications with other players and three colored LEDs that indicate the current state of the player.

The board is powered by a CR2032 coin cell mounted at the back of the PCB and it will hopefully last long enough for a full day of playing.

There's also an on/off slider switch and a tactile button for configuration changes on the PCB.

The game is running on a PIC12LF???? having 1.5K flash and 64 bytes of RAM.

## Gameplay 
#### States
A player can be in three different states:

1. Human - Green LED
2. Infected - Yellow LED
3. Zombie - Red LED

#### State changes

* A *Zombie* will turn a *Human* into an *Infected*
* A (multiple?) *Human* will heal an *Infected* into a *Human* again.
* An *Infected* will after some time automatically become a *Zombie*
* A *Zombie* could possibly be treated into a *Human* or *Infected* by visiting (multiple?) *Hospital* (fixed locations with transmit-ony boards)


## IR Protocol
In order to prevent cheating (or at least make it harder) there should be a two-way communications between the nodes in order for a state change to take place. Or else one can simply avoid getting infected by just covering the IR receiver.

