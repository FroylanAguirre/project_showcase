# Soundboard Project Package Redo

The last project in my embedded systems class involved designing a product of our choosing. My lab partner and I
decided to make a sound board capable of recording and playing back three, 4s audio clips. The final product was a mess of
stiff wires, weakly attached to a breadboard (see photo in this file). 
Unsatisfied with this, I orderned the necessary parts from Digikey to redo the project, but this time on a stripboard instead
of a breadboard.

* 12-24-2017 : Seven segment display driver works. Selection buttons soldered and tested.
* 1-1-2018: Stripboard completed, testing began. Everything functions EXCEPT for data retrieval/writing for the EEPROMS ICs. Using
  the original EEPROMS reveals that they still function, but the new ones dont. Voltage readings of SDA and SCL lines reveal
  that SDA is pulled to Vdd, but SCL is at ~1V. Most likely a slave device issue.
* 7-7-2018: Fixed and functional. The problem was two extra pairs of resistors connecting the high rail to the SCL and SDA lines. Not sure how I overlooked that.
  * Future plans:
    * Improve layout.
    * Look into PCB design.
    * Replace 7-seg display with LEDs for selection and status.
  * Stretch goals:
    * Integrate a MCU IC on the board itself.
    
# Notes
I plan to publish a BOM and schematic when the project is complete.
