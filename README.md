Get a crude tone out from the built-in audio jack on the Raspberry Pi 4, using PWM to save processing power. Can be used to trigger an external field recorder, like the Zoom H6, or to just get a reference tone to which to sync your clips.

Connect GPIO 21 (the default CinePi rec-out-pin) with a jumper wire to GPIO 20. The script then uses pin 20 as an input pin to detect whether recording started/ended.
