# Raspberry Pi FM Transmitter

## Project Overview
This project demonstrates how a Raspberry Pi can transmit an FM signal using its GPIO pin.

## Hardware
- Raspberry Pi
- Wire antenna (connected to GPIO pin 4)

## Software
- Raspberry Pi OS
- fm_transmitter
- SoX (Sound eXchange)

## Setup Steps

sudo apt update  
sudo apt install sox  

git clone https://github.com/markondej/fm_transmitter  
cd fm_transmitter  
make  

## Generate Test Wave

sox -n -r 22050 -c 1 -b 16 test.wav synth 10 sine 1000

This command generates a 10-second sine wave audio file for testing.

## Running the FM Transmitter

sudo ./fm_transmitter -f 100.0 test.wav

or transmitting another audio file:

sudo ./fm_transmitter -f 100.0 acoustic_guitar_duet.wav

## Result

The Raspberry Pi successfully transmitted an FM signal at **100 MHz** with **200 kHz bandwidth**.

## Terminal Output

![Terminal Output](terminal-output.png)
