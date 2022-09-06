## CinePi-2K rec signal out
Get a crude tone out from the built-in audio jack on the Raspberry Pi 4 when recording with the CinePi-2K using PWM to save processing power. Can be used to trigger an external field recorder, like the Zoom H6, or to just get a reference tone to which to sync your clips.

## Wiring
Connect GPIO 21 (the default CinePi rec-out-pin) with a jumper wire to GPIO 20. The script then uses pin 20 as an input pin to detect whether recording started/ended.

## Installing

SSH into the Pi. Then,

```
git clone https://github.com/Tiramisioux/cinepi-2k-rec-signal.git
```

## Make script run on start-up
```
sudo nano /etc/rc.local
```
add the lines
```
python3 /home/pi/cinemate/cinepi-2k-rec-signal.py &
```
before the line exit 0

Exit by pressing ctrl-x and then selecting "yes".

... or add the scripts to the end of the file home/pi/camera/cameracore3.py (remember to add sudo for running metadata.py)

Reboot the Pi.
