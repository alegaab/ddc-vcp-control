# DDC VCP Control

**DDC VCP Control** is a small Qt/PySide6 desktop utility for Linux that lets you control custom DDC/CI VCP codes from a simple graphical interface.

It was created for monitors that do not expose brightness or speaker volume through the usual desktop controls, or that use non-standard VCP codes.

The app provides configurable sliders for:

- monitor brightness;
- monitor speaker volume;
- custom VCP codes;
- KDE OSD feedback;
- XDG/KDE autostart.

> This project was written entirely with the assistance of AI.  
> The code was generated with ChatGPT and then tested and configured on real hardware by the maintainer.

---

## Why this exists

Some monitors expose useful controls through DDC/CI, but desktop environments may not support the exact VCP codes used by a specific model.

For example, on some monitors:

| Function | Standard / common VCP | Custom example |
|---|---:|---:|
| Brightness | `0x10` | `0x6B` |
| Speaker volume | `0x62` | `0x62` |

KDE/Plasma usually controls audio through PipeWire/PulseAudio and brightness through PowerDevil/backlight/DDC backends. This is not always enough for monitors that expose hardware speaker volume or non-standard brightness controls.

DDC VCP Control lets the user choose the VCP codes manually.

---

## Features

- Simple Qt GUI.
- Two configurable sliders by default:
  - brightness;
  - monitor volume.
- Custom VCP code per slider.
- Configurable I2C bus, for example `/dev/i2c-8`.
- Configurable step size, min and max values.
- Optional KDE OSD integration.
- Optional autostart at login.
- Tray icon support.
- Fast shortcut mode for keyboard keys, knobs or macro pads.
- Uses `ddcutil` under the hood.
- Does not require patching KDE, PowerDevil or the kernel.

---

## Screenshot

![DDC VCP Control screenshot](screenshots/main-window.png)
