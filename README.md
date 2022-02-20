# WallSwitchRemote
Contains the ESPHome .yaml that allows you to modify your ESP controlled wall switch such that a button press can trigger a Home Assistant automation without toggling the relay state. This is useful when you have smart bulb installed and want to avoid accidentally cutting power to the smart lights.

## Problem Definition
After installing smart bulbs (e.g. HUE or IKEA smart bulbs) which are controlled by a mechanical wall switch, the usual problems that arise are:
- power to the bulbs is cut by accidentaly toggling the wall switch
- an additional remote is mounted around the location of the mechanical switch to control the smart bulbs
- need to inform all visitors to not toggle the mechanical switch
- bypass the switch by physically connecting the switched wires behind the switch

## Proposed Solution
Use a smart switch where the button press action is not linked to the the relay control.

