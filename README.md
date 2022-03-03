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

## Solution implementation
This project contains the .yaml file for ESPHome for a Gosund-SW9 smart switch that supports the following functionalities:
- Switch-1 and Switch-2 to control each relay _(exposed to home asssistant)_
- Switch-Cngf used as a configuration to enable/disable the control of relay-2 by a short press on the mechanical button-2 _(exposed to home asssistant)_
- Short Press, Long Press, Double Press and Press and Hold actions for both mechanical switches
- The "Press and Hold" action on the mechanical button-1 will toggle the Switch-Cnfg and flash the Button-2 LED for confiramtion
- Turn on both buttons' LEDs on boot
- Close relay-2 on boot
- Set Switch-Cnfg to the ON state on boot

## Home Assistant exposed entities
<img src="https://user-images.githubusercontent.com/93916516/154858345-004481cc-db22-41d6-b712-bb2e7347887e.png" width="300">
