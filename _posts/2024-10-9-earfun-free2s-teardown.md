---
layout: post
title: "EarFun Free 2S Teardown"
categories:
- Blog
tags:
- hardware
- teardown
---

One day a few months ago, as I was biking in Cambridge, my earbuds fell out of my pocket onto the road. I pulled over but before I could grab them, a car had run them over. And so I decided to pick up the pieces and take them apart to see what's going on inside.

I have the EarFun Free 2S earbuds. You can read all their ad copy about how they're wireless Bluetooth earbuds that have ~30 hours of playtime here. If memory serves, these were recommended on Wirecutter as good-enough earbuds if you were looking for something cheap but decent. I think I paid around $30 for them.

These were built to be difficult to repair. Since I bike with at most one earbud in, one of the earbuds was in the case that got run over by the car. Shout out to the car for destroying the plastic case for me! It would have been way harder to do by myself. You can't take the case or earbud apart nondestructively because of glue.

# The Case

There are two earbuds, left and right, that slot into an oval case with a satisfying click. The earbuds themselves have two exposed conductive pads that contact two pogo pins inside the case, which I imagine is for charging. The case itself is charged over a USB-C connector, and there's a button on the side.
![Earbuds in their case](/assets/images/teardown/earbuds_incase.jpg)
![Earbuds out of case](/assets/images/teardown/earbuds_outofcase.jpg)

Rather than spend money on a connector, the designers chose to solder tiny wires from one PCB to the next. There's one tiny PCB towards the top of the case, and one main PCB. All the PCBs seem to be 2 layers, which makes sense for costing down.
![PCB in case, top view](/assets/images/teardown/earbuds_mainpcb.jpg)

The bottom of the case has a big coil for supporting wireless charging.
![PCB Assembly out of case](/assets/images/teardown/earbuds_pcboutofcase.jpg)

I removed the tiny screws to take the main PCB out of the enclosure. The main PCB has the pogo pins that contact the earbuds. 
![Main PCB Front](/assets/images/teardown/earbuds_mainpcbfront.jpg)
![Main PCB Back](/assets/images/teardown/earbuds_mainpcbback.jpg)

The battery is glued to the bottom of this PCB. It's a pretty standard 400mAh battery (I think I've bought similar ones from SparkFun). It has an NTC pin - an NTC is a thermal sensor that detects battery temperature, so that the circuit can shut down if needed for safety.
![PCB Assembly](/assets/images/teardown/earbuds_pcbassembly.jpg)

The tiny PCB contains a hall effect sensor, to detect when the case is open vs closed. I think the magnet that holds the case closed also functions to activate the sensor here. The hall effect signal wire is shielded, but not insulated - I imagine this is to further save on cost.
![Hall Effect Sensor](/assets/images/teardown/earbuds_hallsensor.jpg)
![Hall Effect Sensor Wires](/assets/images/teardown/earbuds_hallwires.jpg)

The top of the PCB has the red and green LEDs for charge indication, surrounded by a black mask.
![LEDs on PCB](/assets/images/teardown/earbuds_leds.jpg)

The SS809 seems to be the main chip on this board. It seems to be "an AD MCU integrated with charge and discharge management" from Sinhmicro (this is from the Google description - the datasheet itself wouldn't load for me), which has a pretty low clocking rate (12MHz) that I don't think would support Bluetooth. My hypothesis is that the case is purely for providing power to the earbuds, and the actual music playing / Bluetooth commands are sent directly to the earbuds.

Onto the power scheme! I'm curious if they implemented USB-PD given that they used a 6 pin power-only USB-C connector. They didn't have to, given that the nominal current draw is 1A (USB-PD is only required at 3A and above), and it would have certainly added cost and development time. There is a P14C1N chip directly under the USB connector for overvoltage protection. This is especially useful since USB-C is a form factor for a connector, so there's no guarantees that a USB-C source provides 5V (see: my 19V laptop charger). I would wager that there is no PD happening here.
![USB-C Connector](/assets/images/teardown/earbuds_usbc.jpg)

On the right side of the board, there appears to be a chip that provides power to the battery. I think this is a DC/DC converter given that there are power planes and a large inductor.

# Earbud

The earbud is also wired together rather than using connectors. In addition to cost constraints, this also makes sense for space - using wires allows you to cram a lot of stuff into one earbud. The earbud has a battery, and connects to the case through pogo pins for charging and to the speaker.
![Earbud Disassembled](/assets/images/teardown/earbud_disassembled.jpg)

The battery is a LIR1045 40mAh button battery.
![Earbud Battery](/assets/images/teardown/earbud_battery.jpg)

There is an MCU that seems more substantial than the one on the case - I couldn't get the part number because it was covered by a potting solution and I couldn't get it off (which is probably for waterproofing). It must be Bluetooth-capable though. One thing that's challenging with Bluetooth is that you're only supposed to have one controller device - so how do you handle two earbuds? There are chipsets out there that share controller responsibilities by switching roles rapidly. The answer is to either use those chipsets or designate one earbud to be the controller and the other the peripheral. Using the former is probably better to avoid consistent latency between ears, but it could also be that the latency is so small it's imperceptible. These earbuds also have a "game mode" that drops latency from 200ms to 60ms.
![Earbud PCB Front](/assets/images/teardown/earbud_pcbfront.jpg)
![Earbud PCB Back](/assets/images/teardown/earbud_pcbrear.jpg)

There are a few other smaller unmarked ICs on the board. One is definitely for touch sensing, since the earbuds can be controlled by tapping the outside (pause, skip, etc), and another is likely the microphone (since it's placed so close to the LEDs & case opening).

This earbud also has the LEDs for status indication (connected, trying to connect, error) surrounded by a black mask.

# Conclusion

Overall, this is a good example of a mass-manufactured and cheap consumer product. You know exactly what you're getting - good audio quality and battery life, but it's not a luxury product. I think these earbuds do that very well and I've been happy with them from a functionality standpoint.

I do wish sustainability was more encouraged and incentivized, though. If any one of the parts of this assembly broke, I'd have to reorder the whole package (rather than one earbud, or just the case). Products that are more sustainable generally cost more because of the thought that goes into them and the less-standard design, which are not compatible with the breakneck pace of consumer electronics.

After these broke, I ended up not replacing them. I have wired earbuds at work for calls and a speaker at home for listening to music, and I decided to not create more e-waste. These earbuds served me well, and they'll be recycled in my office's e-waste bin.