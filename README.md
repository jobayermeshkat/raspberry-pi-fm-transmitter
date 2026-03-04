# Raspberry Pi FM Transmitter

## Objective
To transmit an FM signal using Raspberry Pi GPIO.

## Software Used
- Raspberry Pi OS
- fm_transmitter
- sox

## Commands Used

sudo apt update

sudo apt install sox

git clone https://github.com/markondej/fm_transmitter

cd fm_transmitter

make

sox -n -r 22050 -c 1 -b 16 test.wav synth 10 sine 1000

sudo ./fm_transmitter -f 100.0 acoustic_guitar_duet.wav

## Output
The Raspberry Pi successfully transmitted an FM signal at 100 MHz with 200 kHz bandwidth.

![Terminal Output](terminal-output.png)
