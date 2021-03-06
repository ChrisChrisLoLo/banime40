# PCB
This section contains information about making your own assembled PCB

## Acknowledgements
Thank you to [PCBWay](https://www.pcbway.com/) for sponsoring research and development for the banime40. Because of them, I can further iterate on this board, as well as do some experimentation with SLA printed cases. I found their service to be fast and easy to use, so I do endorse using them for your PCB printing needs.

## Gerbers
A zipped file containing the Gerbers you need should be already provided for certain PCB print services. You may need to re-generate the Gerbers if you go with a different PCB service.

When ordering from PCBWay or the like, the standard print settings should be fine, though I do recommend the Lead free HASL surface finish, mostly out of concern for long term health. If you think having a leaded surface is fine, feel free to go with that option.

Follow this guide to learn more about uploading Gerbers to services like PCBWay: 
https://www.pcbway.com/helpcenter/Findproducts/How_do_I_place_an_order_.html

## Bill of Materials
Here is the list of materials you will need:
- 1 pro-micro. I highly recommend using the USB-C pro-micros, as I build the PCB with the size of that microcontroller in mind. Other pro-micro compatible boards should also be fine.
- Appropriate header
- 43x Kailh hotswap sockets
- 40x Diodes
  - PCB supports either through-hole or SMD
  - I found that through-hole is more commonly found, but leave "pokey" bits on the pcb, while SMD diodes are a tad bit harder to get, while leading to a cleaner PCB
  - If going down the SMD route, I personally prefer the black diodes over the glass ones
- [Optional] 1x reset button
  - A 3x4mm SMD buttom should do it (haven't confirmed)
  - I recommend just shorting the micro-controller pins or using bootmagic instead to reset the board though.
  - Note that the cases currently do not have holes to support this button
  - Note that I plan to swap out this button with a more standard size

## Assembly
Once you have all the parts, you will want to do the following steps. Following similar build guides, like the CRKBD or REVIUNG41 build guides should give you a rough idea of the build, if this is your first time assembling a board.
- Solder on the diodes first, as they are the smallest parts.
    - Remember that diode polarity does matter, so refer to diode reference guides if needed.
    - Note that all diodes point the same way vertically and horizontally
- Solder on the hot swap sockets
    - Everyone has their own grove, but what I like doing is placing a _very_ small amount of solder onto one pad, placing the socket onto the board, and then using the soldering iron to re-heat the solder pillow while gently pressing down on the socket with tweezers.
- Flash the firmware onto the pro-micro
    - There is a hex file available for you to flash in the `firmware` folder of this repo.
    - You should confirm that flashing is successful before doing any kind of solder work with your microcontroller, to at least have some confidence that the board works.
    - QMK PR in progress
- Solder on the pro-micro
    - Ensure that the components under the pro-micro footprint have a solid solder connection before soldering the header pins.
    - The pro-micro **must** be on the same side as the other components, with the pro-micro facing up.
    - Low profile female sockets should work, though I do think it might be cutting it close hight wise.
