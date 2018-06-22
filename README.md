# smartkeyfinder
Helps find lost passive keyless entry car key fobs (i.e. [smart keys](https://en.wikipedia.org/wiki/Smart_key))

# Status
*At the moment, this is just an idea for a future project.* I'm just documenting interesting resources that I've come across in my research.

# Idea
This is a hardware device (perhaps standalone, or perhaps plugged in to a phone or computer), which records the signal that the car sends to wake-up the key fob and then replays that signal in other locations and displays the strength (and possibly direction) of the smart key's response.

It should cost substantially less than $100. Otherwise, it is probably cheaper to just get and program a new smart key

# Resources

## Background

https://eprint.iacr.org/2010/332.pdf - Paper describing the way these systems work and how a relay attack can be used against them.

https://conference.hitb.org/hitbsecconf2017ams/sessions/chasing-cars-keyless-entry-system-attacks/ - Presentation on system which uses relay attack to break-in to cars which use smart keys.

https://fccid.io/ - Lookup the frequency at which a a particular smart key operates.

## Recording and playing back the car's 125kHz wake-up signal

[AS3933 Development System](https://www.mouser.com/ProductDetail/ams/AS3933-DEV-SYSTEM?qs=abmNkq9no6CEexCfuZXvZQ%3D%3D&gclid=CjwKCAjwma3ZBRBwEiwA-CsblBmGowI5RJ5Bt3QB-EMN4k0N-29EVO9rrtOMMO3-p2BjhQMVCeOpZBoCFXMQAvD_BwE) - $260 plug-and-play system for working with the 125kHz wake-up system used in at least some of the smart key systems. Expensive but could be used to prove the feasibility of the concept.

[Espotek Labrador](http://espotek.com/labrador/product/espotek-labrador-board/) - $29 USB board with both oscilloscope and signal generator functionality. Probably not enough bandwidth for the 125kHz wake-up signal but might be worth a try. Would presumably also need an amp and antenna.

https://digibird1.wordpress.com/arduino-as-a-5m-sample-osciloscope/ - A fast oscilloscope based on an Arduino and an external ADC.

## Listening for the smart key's response

https://www.adafruit.com/product/1497?gclid=CjwKCAjw9qfZBRA5EiwAiq0AbcbSHQ5MJVPVm0SsUiqtuzBhm_KNN7Ewk-B6O7MjhVj9NyhHP3-BLxoCN1YQAvD_BwE - $23 Software Defined Radio that should be able to tune in to the frequency that the smart key responds with.

