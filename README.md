# Digicus (In-Progress)
A digital abacus trainer modeled after the Japanese Soroban.  The columns of beads are represented
by eight columns of five LEDs, with a toggleable OLED display showing in real time the numerical
number represented by the columns.  Beads can be "pushed up or down" by the use of pushbuttons
placed next to each column of LEDs, with a powered LED acting as a pushed-up bead for the four
lower "Earth Beads" of each column, representing 1s, and a pushed-down bead for the upper "Heaven Bead",
representing a 5.

The OLED display, alongside its toggle switch, allows the Digicus to be used as a trainer.  When
toggled on, the display allows for the user to continuously see the numerical representation of
the beads, enabling direct visual feedback of the current state of the abacus.  The display may
also be turned off, allowing the user to practice inputting a number or performing an arithmetic
operation on their own, and then turning the display back on to check their work.

********************************

## Project Progress

* Design Requirements \[**Completed**\]
* Design Specifications \[**Completed**\]
* Component Selection \[**Completed**\]
* Schematic Design \[**Completed**\]
* Functional Prototype \[**In-Progress**\]
* Firmware \[**In-Progress**\]
* Board Layout \[**To-Do**\]
* Board Manufacturing and Testing \[**To-Do**\]

********************************

## Sections

* [Design Requirements](#design-requirements)
* [Design Specifications](#design-specifications)
* [Component Selection](#component-selection)
* [Schematic Design](#schematic-design)
* [Functional Prototype](#functional-prototype)
* [Firmware](#firmware)

## Design Requirements

The following are my determined requirements for this design:

1. The Digicus must have enough columns of "beads" to perform useful calculations.
1. The Digicus must have an intuitive input method for interacting with the "beads".
1. The Digicus should be highly responsive to all inputs, reacting immediately.
1. The Digicus must be able to be operated portably, i.e. not have to be tethered to an
   outlet or cumbersome power supply for it to function.
1. The Digicus must be small enough to be portable, but large enough to be used
   comfortably.
1. The Digicus must feature a display that consumes relatively low power and is legible
   in well-lit environments.

## Design Specifications

The following are the design specifications along with the number of the design requirement, if any,
that they address in brackets:

* The Digicus will have 8 columns of 5 LEDs, for a total of 40 bead LEDs. \[1\]
    - The lower 4 LEDs will be red, with the upper LED being amber.  This adds an additional
        visual differentiatior between the heaven bead and the earth beads.
* The Digicus will use three pushbuttons per column of LEDs for interacting with the "beads",
  as well as a button for resetting the abacus to zero, for a total of 25 pushbuttons. \[2\]
    - Two of the pushbuttons for each column will be used for "pushing up" and "pushing down"
      earth beads with the third bead toggling the heaven bead.
* The Digicus will be powered by three NiMH AAA batteries in series or an external source, fed to a
  switching voltage regulator for a 3.3V supply voltage. \[4\], \[5\]
    - Using AAA batteries allows for an easily available, rechargeable, and relatively compact
      power source, close to the desired 3.3V supply voltage.
    - Employing a switching regulator instead of a linear regulator will allow for higher efficiency
      since the difference between the 3.6V provided by the series batteries and the 3.3V supply
      voltage output by a linear regulator will be lost as heat.  Any high frequency switching noise
      of the switching regulator will not be an issue since there are no high frequency data signals
      present in this design.
* The Digicus will use the Microchip ATmega328PB microcontroller to run the device. \[3\]
    - The ATmega328PB is cost-effective, easy to program, and can clock up to 10MHz at the
      desired 3.3V supply voltage, which is plenty fast enough for this application.
    - The ATmega328PB provides two independent I2C buses as well as two independent SPI buses,
      allowing for communication to the display, programming interface, and any other IC needed.
    - The ATmega328PB is available as a VQFN package, allowing for a small vertical footprint.
* The Digicus will employ the use of shift registers to expand the effective I/O of the MCU in order
  to interface with the large number of LEDs and pushbuttons.
* The Digicus will use a small OLED as its primary display. \[6\]
    - An OLED display will consume less power than a comparable LCD or seven segment display array, and
      provides a very high contrast ratio for easy viewing.


## Component Selection

## Schematic Design

The Digicus schematic can be broken down into five major blocks:

* [Power Supply and Programming Interface](#power-supply-and-programming-interface)
* [Display](#display)
* [Shift Register Bank](#shift-register-bank)
* [Shift Register Outputs](#shift-register-outputs)
* [Microcontroller Connections](#microcontroller-connections)

Each will be described briefly in this section alongside an image of its section in the schematic.
The full schematic of the design can be viewed as a PDF in
[schematics/digicus-schematic.pdf](schematics/digicus-schematic.pdf).

### Power Supply and Programming Interface

### Display

### Shift Register Bank

### Shift Register Outputs

### Microcontroller Connections

## Functional Prototype

## Firmware
