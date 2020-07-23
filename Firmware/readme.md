[ The FR4 Machine Shield uses Open Source GRBL control software running
on the Arduino UNO 328p to interpret machine code or G code commands.
The following is a list of settings that must be changed for Grbl V.9 to
run correctly with any given FR4 Machine Shield. Users can also upload
the grbl.zip file, from the Pocket NC web page. Using the second method,
users may need to send the following command to the arduino after
flashing. \$RST=\* This enables a correct settings change. To upload
grbl.zip into the Arduino IDE, select Sketch \> Include Library \> Add
.zip Library. To open the GRBL library, select file \> examples \>
grbl.]{dir="ltr"}

[]{dir="ltr"}

**[CONFIG.h]{dir="ltr"}**

[(Line \# 137) \#define ENABLE\_SAFETY\_DOOR\_INPUT\_PIN
(enable)]{dir="ltr"}

> [This option causes the feed hold input to act as a safety door
> switch.]{dir="ltr"}

[]{dir="ltr"}

[(Line \# 142) \#define SAFETY\_DOOR\_SPINDLE\_DELAY 8000]{dir="ltr"}

[Pauses machine for 8 seconds after pause for spindle to warm
up]{dir="ltr"}

> []{dir="ltr"}

[(Line \# 173) \#Invert spindle enable pin]{dir="ltr"}

[(Uncomment to enable feature)]{dir="ltr"}

[]{dir="ltr"}

[(LINE \# 234) \#define DISABLE\_LIMIT\_PIN\_PULL\_UP]{dir="ltr"}

[(Uncomment to enable feature)]{dir="ltr"}

[]{dir="ltr"}

[]{dir="ltr"}

[]{dir="ltr"}

**[CPU\_map\_atmega328p.h]{dir="ltr"}**

[(Line \# 63 & 64) \#define X\_LIMIT\_BIT 2 // Uno Digital Pin
10]{dir="ltr"}

> [\#define Y\_LIMIT\_BIT 1 // Uno Digital Pin 9]{dir="ltr"}
>
> [(Changed from x bit 1 and y bit 2 to accommodate backwards board
> pinout)]{dir="ltr"}

[]{dir="ltr"}

[]{dir="ltr"}

[**\$\$ Settings**]{dir="ltr"}

[\$0=10 (step pulse, usec)\
\$1=250 (step idle delay, msec)\
\$2=0 (step port invert mask:00000000)\
\$3=0 (dir port invert mask:00000110)\
\$4=1 (step enable invert, bool)\
\$5=0 (limit pins invert, bool)\
\$6=0 (probe pin invert, bool)\
\$10=3 (status report mask:00000011)\
\$11=0.010 (junction deviation, mm)\
\$12=0.002 (arc tolerance, mm)\
\$13=0 (report inches, bool)\
\$20=0 (soft limits, bool)\
\$21=0 (hard limits, bool)\
\$22=1 (homing cycle, bool)\
\$23=3 (homing dir invert mask:00000001)\
\$24=100 (homing feed, mm/min)\
\$25=300 (homing seek, mm/min)\
\$26=250 (homing debounce, msec)\
\$27=3.000 (homing pull-off, mm)\
\$100=800 (x, step/mm)\
\$101=800 (y, step/mm)\
\$102=800 (z, step/mm)\
\$110=300.000 (x max rate, mm/min)\
\$111=300.000 (y max rate, mm/min)\
\$112=300.000 (z max rate, mm/min)\
\$120=30.000 (x accel, mm/sec\^2)\
\$121=30.000 (y accel, mm/sec\^2)\
\$122=30.000 (z accel, mm/sec\^2)\
\$130=225.000 (x max travel, mm)\
\$131=125.000 (y max travel, mm)\
\$132=170.000 (z max travel, mm)]{dir="ltr"}

[]{dir="ltr"}
