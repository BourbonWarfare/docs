# Binocular Ranging

Not every position gets a laser range finder, but you’ve got a great analog tool that serves the same purpose. The binoculars you’re equipped with by default are broken up into a series of hash lines and numbers; these follow the milliradian system of ranging. Every number represents 10 milliradians (1 = 10 mils, 2 = 20 mils, and so on) while each hash line between the numbers represents 5 milliradians.&#x20;

The formula to calculate range is (1000 \* target height)/miliradians.&#x20;

In Arma, every player model is 1.8 meters tall. Put the bottom line of the binoculars at their feet, estimate how many miliradians they take up, and divide 1800 by that number. The end result is their range away from you.

\
