# Remarkable2-recovery
This Repository is inspired by and heavly dependand on https://github.com/ddvk/remarkable2-recovery the have done a great job of Documenting the Process.

This Repository is just a Personal "Wiki" in whitch i document my expirients with recovering a Remarkabel 2 out of a Soft-Brick.
I will also be sharing my method of creating full disk backups in case of future misshaps.

## Prerequisits
Like disgussed in ddvk´s guide you need a

- USB-C Breakout Board (It needs to have a full breakout, not just  VBUS, D+ ,D-, GND) ![Picture ofUSB-C Breakout](./images/USB-C_breakout.jpg)

- Micro USB to Pogo Pin adapter,
> Pogo pins are as follows, when viewed from the side, device facing up (VBUS is near the usb-c) ```GND,ID,D+,D-,VBUS```
![Micro USB Pogo](./images/Micro-USB_Pogo.jpg)

- [imx_usb_loader](https://github.com/boundarydevices/imx_usb_loader) ive included the version DDVK originaly gave out. It is in the imx_usb dirrectory, but can also be self-compiled.

