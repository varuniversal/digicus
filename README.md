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

## Design Specifications

The following are the design specifications along with the number of the design requirement that
they address in brackets:

* The Digicus will have 8 columns of 5 LEDs, for a total of 40 bead LEDs. \[1\]
    - The lower 4 LEDs will be red, with the upper LED being amber.  This adds an additional
        visual differentiatior between the heaven bead and the earth beads.
* The Digicus will use three pushbuttons per column of LEDs for interacting with the "beads". \[2\]
    - Two of the pushbuttons will be used for "pushing up" and "pushing down" earth beads with
      the third bead toggling the heaven bead.

## Component Selection

## Schematic Design

## Functional Prototype

## Firmware
