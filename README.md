# Remarkable2-recovery
This Repository is inspired by and heavly dependand on https://github.com/ddvk/remarkable2-recovery the have done a great job of Documenting the Process.

This Repository is just a Personal "Wiki" in whitch i document my expirients with recovering a Remarkabel 2 out of a Soft-Brick.
I will also be sharing my method of creating full disk backups in case of future misshaps.

**It is best to read the instructions fully befor starting tue to being under time pressure while in the midst of it.**

## Prerequisits
Like disgussed in ddvk´s guide you need a

- USB-C Breakout Board (It needs to have a full breakout, not just  VBUS, D+ ,D-, GND) ![Picture ofUSB-C Breakout](./images/USB-C_breakout.jpg)

- Micro USB to Pogo Pin adapter,
> Pogo pins are as follows, when viewed from the side, device facing up (VBUS is near the usb-c) ```GND,ID,D+,D-,VBUS```
![Micro USB Pogo](./images/Micro-USB_Pogo.jpg)

- [imx_usb_loader](https://github.com/boundarydevices/imx_usb_loader) I´ve included the version DDVK originaly gave out. It is in the imx_usb dirrectory, but can also be self-compiled.

## Guide

### Getting into Recovery mode
I recomend using tmux or multiple terminals due to needing to monitor multiple commands.

1. Run ```dmesg -w``` to get a continual output of the Kernel Logs
2. Power of the Rm2 (hold power button for 10 sec)
3. Plug in the USB-C breakout board with B8 pulled down to B12 / GND via a 10K resistor
4. Connect Pogo Pins (Watch out that you have a solid connection and no shorts (**MAKE SURE YOU USE THE PROPER ORIENTATION, YOU RISK FRYING YOUR DEVICE IF CONNECTED INCORECTLY** be warnd.))
5. Plug in micro USB cable into computer with a known good cable.
6. If the remarkable did not start on its own power it on with the Press of the Power Button.
7. Look at the dmesg output, there should be a line saying ```USB HID v1.10 Device [Freescale SemiConductor Inc SE Blank ULT1]```
8. **REMOVE Pulldown**, the next steps wont work with the pulldown still there
9. Run the imx_usb binary from the imx_usb directory (can be done with ```sudo ./imx_usb``` command)
10. You should see a dmesg with says ```USB Mass Storage device detected```

You can now mount the Mass Storage device if it were a normal USB Stick








