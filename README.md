# Filament Runout Sensor
Simple roller switch based filament runout sensor. Used with Rostock Max v2 (upgraded to v3) with dual extruders.

# Description
The original mechanical housing and switch selection were sent to me as an STL file by email, I'm not sure who originally created this model (sorry for lack of attribution!). It is similar to [this one](https://www.thingiverse.com/thing:1134134). I modified the STL in Fusion 360 to improve printability (square profile prints better than round) and switch fit (including open back-end for easy connection). I have also added a wiring diagram for using this switch with the RAMBo 1.3L that is in my SeeMeCNC Rostock Max printer. I used [5A 125 250V SPDT 3 pin momentary hinge metal roller lever microswitches](https://www.amazon.com/gp/product/B07BL33XXT) to add the filament sensors.

I also modified a Teensy project to [adapt the HE280 end effector platform](https://github.com/FEsmondeWhite/HE280AccelerometerInterface) for use with the latest Repetier branch.

[Find more discussion of my Rostock Max setup on the Repetier forum](https://forum.repetier.com/discussion/8324/rostock-max-he280-accelerometer-z-probe-filament-runout-sensors).

# Assembly
One housing and switch are needed for each filament runout sensor. 3D print a housing, and press a switch into the housing, so that the roller ends up in the filament path. I used crimp-on automotive blade-style connectors to connect onto the switch, with tiny wires salvaged from an ethernet cable and dupont connectors to connect to the RAMBo board.

Switch pins 1 and 3 are connected to the RAMBo. I have connected filament sensor 1 to the X-min endstop port on the RAMBo, for use with extruder 0. Filament sensor 2 is connected to the Y-mnin endstop port on the RAMBo. The wires are connected to the ground and sensor pins, and the input is set with a pull-up in Repetier firmware. My Repetier 1.0.5 Configuration.h file is included for reference.
