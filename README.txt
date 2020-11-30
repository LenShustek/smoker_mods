This is a repository that documents my modifications to the 
Masterbuilt MES130B food smoker. 

It's a serviceable appliance, and we've made some great meals with it, 
but it suffers from a number of defects. You can read my posting to 
www.smokingmeatforums.com about them in the file forum_posting.txt. 

The first modification I made is to keep the smoke production going 
when the main (and only) heating element turns off to allow the 
temperature to come down. I put some heating elements in the bottom of 
the wood chip tray, and turn them on periodically whenever the main 
heater is off. 

The details are in the chipheater directory. There are two 100W heating 
elements wired in series, so 50W power dissipation. To control them I 
tapped into the 4-wire cable (ground, 5VDC power, heater on, and 
temperature sense) that goes to Masterbuilt's controller, and connected 
a little circuit that switches a small solid-state relay. A knob adjusts 
the duty cycle: it's on for 10 seconds and off for 2 to 18 seconds. It 
seems to be working fine. 

The second modification was to replace the Masterbuilt controller with
one based on an inexpensive PID (proportional-integral-differential) 
controller, interfaced to the smoker with a small circuit. This keeps
the temperature at the set point within a degree or two, rather than
having huge overshoot and undershoot by 10-15 degrees in each direction, 
with a cycle time of about 15 minutes. 

The details are in the PID_interface directory. In particular, see
the PID_addition_instructions file for instructions and photos.
This modification doesn't require the smoker unit itself to be
taken apart, or any of its 120V AC wiring changed.

Len Shustek 13 November 2020 
updated 29 November 2020
