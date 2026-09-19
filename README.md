# Microphone Mute LED Controller for Acer Nitro AN515-46

Shell script for controlling the microphone mute LED on the Acer Nitro AN515-46 (Realtek ALC287).

It initializes the codec GPIO using `hda-verb` and monitors microphone state changes via `pactl`.  
The script supports four LED modes:

- `mute` — LED is ON when the microphone is muted
- `active` — LED is ON when the microphone is active
- `off` — LED is always OFF
- `on` — LED is always ON

## Requirements

You need to install the `alsa-tools` package, or just the `hda-verb` binary on the system.  
The script also requires `pactl`.

## Hardware configuration

- `CODEC_DEVICE="/dev/snd/hwC2D0"`
- `GPIO_BIT=0x10`
- `GPIO_MASK=0x10`
