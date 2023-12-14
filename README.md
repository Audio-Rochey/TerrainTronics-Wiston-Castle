
# Wiston Castle Magnetic Switch LED Driver
## Introduction

Wiston Castle includes a Hall Effect Sensor that can detect magnets, a small battery and a 2 pin LED output. Smaller than 25mm x 25mm, Wiston Castle can fit under a small 32mm circular base, or within a single 1 inch square.

<img src="/pictures/IMG_1923.jpg" width="250"><img src="/pictures/IMG_1924.jpg" width="250"><img src="/pictures/IMG_1925.jpg" width="250">

Please take a minute to read through the uses - there's usability hints throughout that will inspire creative usage!

## Uses
Wiston Castle can be used over the surface of the table, within the base of a piece of scatter terrain piece or the case of a player character etc.
### Example 1 - Fire Pits, Tall Candles etc
<img src="/pictures/pentagram.jpg" width="350"><img src="/pictures/wistoninbase.jpg" width="500">

Here the Wiston Castle has been designed to fit in a base, battery pointing down, so that it can be changed easily. Magnets have been placed beneath the foam floor of the terrain, so that it lights up ONLY when the scatter terrain is above the exact spot. This makes an excellent "X Marks the Spot" type experience.
In this image, the LED has been wire wrapped to the LED, touch of solder on those joints to hold them in place, and then the other ends directly soldered to the + and - LED pins on the Wiston Castle PCB. + connects to the longer pin on a traditional LED and the - to the shorter pin.

### Example 2 - X Marks the spot for player models.
INSERT PICTURE
By placing the Wiston boards BENEATH the playfield/floor, LED's can be triggered, and powered by a player position, providing the player mini's have a magnet placed in their bases. The polarity of the magnets is not important, Wiston Castle will respond whether you see a North or South facing magnet.
In a puzzle room, each LED can be wired directly to the Wistron Castle. Nice and Easy.

### Example 3 - A sensor for a larger system (e.g. Arduino or Wemos D1 Mini)
INSERT BLOCK DIAGRAM

Wiston Castle boards can drive more than a simple LED. 

The **LED-** pin is a simple 3V / 0V output with **inverted** logic that can be used to drive the input pins of a microcontroller such as an Arduino or Wemos D1.
**LED+** remains at VCC (3V for battery usage) regardless of magnet presence.

If you have multiple Wistron Castles, you may not want to use a battery in each one. In which case, the battery can be bypassed by soldering your power supply (e.g. 3.3V or 5V) to the positive battery terminal.
** IF YOU DO THIS - MAKE SURE TO ADD A RESISTOR INLINE WITH YOUR LED**

## How does it work?
Wiston Castle is a simple design. The schematic is painfully simple. The SL1603SL Hall Effect sensor does most of the heavy lifting.

The CR1616 battery powers the SL1603SL Hall effect sensor. The output of the Hall Effect sensor is connected to LED- Pin on the output.

Simple Stuff Really! PG1.0 used a reed switch, but I found the reed switches not to react when a magnet was immediately below it. Reed switches need to be at a common angle to the magnetic fields, forcing most magnets to be on their side, or off to one side.
The SL1603SL is designed to be directly above a N or S face of a Magnet. Perfect.

<img src="/pictures/WistonPG2p0Schem.png" width="500">

Key components:
  
SL1603SL

> Written with [StackEdit](https://stackedit.io/).
