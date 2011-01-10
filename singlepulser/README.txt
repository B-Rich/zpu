Test f�r die neue Version des Singlepulsers


Funktionsbeschreibung:

Es wird eine Impulsfolge mit einem definierten Takt-Pause-Verh�ltnis erzeugt.
Das Design arbeitet mit einem eigenen Taktgeber/Taktdom�ne f�r die Bestimmung der Impulsdauer/L�nge (50 MHz).

Auf dem Pulse_In-Eingang (13 MHz) wird eine Taktflankenerkennung durchgef�hrt.
Der Ausgang wird wieder mit dem 13-MHz Takt synchronisiert.


Hardwareplatform zum Testen: CPLD, Xilinx XC9536XL

Hardware lief mit Testsignalen (Clk) bis ca. 200 MHz.
Um die Taktflanke sicher zu detektieren, mu� die On-Dauer des Pulssignals 
�ber 100% der Taktperiodendauer betragen.


Detektion geht:

Clk     __--__--__--__--__--__--__--__--__--__--__--_
Pulse   _____-----_____-----_____-----_____-----_____
erkannt       |           |       |           |      


Detektion geht nicht:

Clk     _____-----_____-----_____-----_____-----_____
Pulse   ______--______--______--______--______--_____
erkannt                |                   
fehlt         |               |       |       |
