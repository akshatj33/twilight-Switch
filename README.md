# twilight-Switch
This is the embedded C code and the schematic and board layout for my project on twilight switch.

The timely operation of street lights, porch lights and other forms of outdoor illumination is required for the twin
concerns of safety and environment protection; lights operated too late are a safety hazard, while lights operated
too early are a waste of power. The switching on and off of external lightings can be set with the help of the device
called Twilight Switch.
Traditionally switching has been controlled via a human operator or the automatic control is accomplished
using a light sensor like LDR, photosensitive cells etc. However the use of sensors is accompanied by
wastage of power deterioration over time due to incessant exposure to atmosphere and environmental
changes leading to regular maintenance.
A Twilight switch provides a mechanism by which a light bulb can be turned ON and OFF automatically
without human interference. This project is a time based solution. This mechanism works on civil twilight
time. Component used for human interface is LCD where data such as date, month, year, city and the
present time (hh:mm:ss) are entered. From the algorithm, twilight time i.e. civil-dusk and civil-dawn time of
that place is calculated.
RTC (PCF8563) is used to maintain time. As an when the civil dusk time matches with RTC, the light (here
bulb) is switched ON and remains in this state till civil-dawn time where it is toggled.
We have fabricated 2 boards. First (4*3) is the DC Circuit board which has our microcontroller
(MSP430G2553) and LCD (HD44780U). Second (3*1) is the AC circuit board which has a triac (BT136)
whose 2 of the 3 gate requires AC. We are using triac instead of a relay because SSD switches are better
than mechanical ones. To isolate the AC portion of the circuit from the DC one we have used an optoisolator
(MOC 3041).
