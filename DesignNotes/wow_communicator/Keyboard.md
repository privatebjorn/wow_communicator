# Overview
The full QWERTY keyboard will use a series of tactile switches along with a microcontroller to read out keys and relay them along an i2c bus.

## MCU Selection 
The selected microcontroller is the [[stm32c011f6.pdf#page=1&selection=176,0,176,11&color=yellow|STM32C011F6]]. This selection was made as the controller has a sufficient number of pins to provide all required functionality. 
* [[stm32c011f6.pdf#page=1&selection=101,0,107,16&color=yellow|Up to 18 fast I/Os – All mappable on external interrupt vectors – All 5 V-tolerant]]
* [[stm32c011f6.pdf#page=1&selection=158,0,158,44|Development support: serial wire debug (SWD)]]
* [[stm32c011f6.pdf#page=1&selection=135,0,142,22&color=yellow|One I 2 C-bus interface supporting Fastmode Plus (1 Mbit/s) with extra current sink; supporting SMBus/PMBus™ and wake-up from Stop mode]]

The package selected is the TSSOP20 version shown below:
![[stm32c011f6.pdf#page=27&rect=118,561,534,757&color=yellow]]

### Power Supply Scheme
The power supply scheme implemented was as follows 
![[stm32c011f6.pdf#page=34&rect=62,352,545,755&color=yellow]]

### Suggested NRST Pin 
The NRST pin was pinned out as suggested below: 
![[stm32c011f6.pdf#page=64&rect=115,513,537,758&color=yellow]]

## Switch Selection
The switches selected were the [[pts636.pdf#page=1&selection=13,0,13,13&color=yellow|PTS636 Series]]

## Keyboard Matrix 
The keyboard matrix was arranged as a 7x6 matrix for maximum keycount whilst maintaining debug interfaces and communication interfaces for the host microcontroller. 

