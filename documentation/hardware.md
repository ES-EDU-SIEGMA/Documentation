# Hardware

The Drink Mixing Machine consists of several hardware parts.
There can be grouped into three categories, namely:

- [Frame](#frame)
- [Dispenser Components](#dispenser-components)
- [Controlling Components](#controlling-components)

## Frame

The frame is build from aluminium bases system profiles.

![system profile](images/alu-profile.png)

## Dispenser Components

The disepenser group consists of multiple components arranged around a standard bar dispenser as seen in image.

![dispenser](images/dispenser.jpg)

The dispenser is triggered by a 3D-printed arm which is lifted with a construction of ropes and deflection spool powerd by a stepper motot as the winch.

## Controlling Components

The group of controlling components consits of a Raspberry Pi as the main controller of the machine combined with a custom PCB that has a sub controller (Tiny2040) which controlls up to 4 stepper driver.

### PCB

The PCB is custom made for the purpose of providing a controller that combines sensors and stepper drivers.

**PCB:**
![PCB](images/pcb-layout.png)

> Rondell (only partly stacked)
>
> - TINY2040 -> Tiny2040
> - POWER_CON -> Power connection for the components
> - U1 -> Dispenser
> - U3 -> Rondell
> - LS4 -> Dispenser switch
> - LS3 -> light dependent resisotr (LDR) of the rondell
> - LED -> LED for LDR sensor of the rondell

> Left/Right:  
> The TMC2209 and sensors are connected regarding the number and the labels on the machine

> Datasheets:
>
> - [TMC2209](../datasheets/TMC2209_datasheet_rev1.09.pdf)
> - [TMC2209 SilentStepKick Board](../datasheets/TMC2209_SilentStepStick_Rev110.pdf)
> - [Tiny2040](https://shop.pimoroni.com/products/tiny-2040)
> - [RP2040 MCU](../datasheets/rp2040-datasheet.pdf)

### Raspberry Pi

The Raspberry Pi provides the GUI for the user and holds the required database for the drinks.
The Tiny2040 on the PCBs are connected via a serial port which where mapped dynmically during runtime.
The scale under the jar is directly connected to the Raspberry Pi.
