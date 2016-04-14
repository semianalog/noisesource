Noise source, rev 1
===

Noise source for filter/amplifier testing, 1 MHz to 1 GHz. CC0/Public domain.

[![3D render](renders/3d-small.png)](renders/3d.png)


Plots
-----

![Wideband output](images/wideband-grey.jpg)

Output: -30 dBm ± 2 dBm from 200 MHz to 1.2 GHz

![Low frequency output](images/low-grey.jpg)

Output: -25 dBm to -29 dBm from 1 MHz to 100 MHz

Getting it
----------

You probably don't want this revision. It has a bug: it oscillates around 1.6 GHz. A ferrite bead in the signal path damped this to the point where it's just a slight hump in the output spectrum (as seen above). I'm saving the existing Rev 1 PCBs, which require this modification, for distribution among friends on IRC. Rev 2 will have footprints for a few types of matching/damping circuits I plan to try between the noise diode and the first amplifier.

The PCB is designed to allow experimentation with different noise diodes. I built two variants. One shoves a lot of current through a [http://www.semicon.panasonic.co.jp/ds4/DZ24100_E.pdf](Panasonic DZ2410000L) 10V Zener diode, roughly along the lines of a Maxim application note presenting a similar circuit. Performance was quite poor. The second uses the emitter-base junction of an [https://www.fairchildsemi.com/datasheets/MM/MMBTH10.pdf](MMBTH10) RF transistor in reverse bias with a 1k source resistor, with much better performance. I recommend the latter.
