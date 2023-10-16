# ESP-Home IR Light Integration
Control your lights with an IR blaster. The remotes are commonly used in cheap light bulbs or LED strips. With this ESP-Home integration you can set colors, brightness and turn the light on or off.

I've set this up in my bedroom with 2 nightstand lights. These are setup as left and right transmitter in the code. 

## Installation:
- `on_boot` in `esphome` is required as it turns on the lights, sets it to white, and turns it back off for initialization as there is no way to track the current state of the light(s). (You could add additional commands to turn the brightness all the way up/down).
- Add you encryption key and ota password and change your board type (or you can just copy the code below `captive_portal` and `on_boot` on your original code, which I suggest you do).
- Make sure to edit the GPIO pins on line `59` and `62`
- Now change all the `addresses` and `commands` to the one from your remote. You can log this data with a IR receiver.
- Also change all the `entity ID's` to your needs

I know this is maybe not the way to go, but this worked for me. You can create a PR to improve the code. It will be highly appreciated (credits will be added). If you run into any issues, please open a issue and I will take a look at it when possible.

## Credits
BreadJS

## Screenshots
*All entities (I changed the `switch` to a `light` in Home Assistant)*

![f](https://raw.githubusercontent.com/BreadJS/esphome-ir-light-integration/main/ESPHomeIR.png)
