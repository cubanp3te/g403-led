# Logitech Prodigy Mouse LED control

Allows you to control the LED lighting of your G203 Prodigy Mouse programmatically.
Inspired by and based on [g810-led](https://github.com/MatMoul/g810-led) and
[g203-led](https://github.com/smasty/g203-led).

## Requirements

- Python 3.5+
- PyUSB 1.0.2+
- **Root privileges**

## Installation

1. Clone the repository: `git clone https://github.com/smasty/g203-led.git`
2. Prepare _virtualenv_: `virtualenv ./env`
3. Install dependencies: `env/bin/pip install -r requirements.txt`
4. Run (as root) the script for your model:
    - `sudo ./g203-led.py solid 00FFFF`
    - `sudo ./g403-led.py solid 00FFFF`

Note that the g403 has to independent lights: one on the scroll
wheel, and one on the mouse itself. This script will set both
lights to use the same configuration, but it can be
customized to set them independently.

## Usage

Make sure to use the script for your mouse model. The example below uses the `g403-led` script.

```text
Usage:
    g403-led solid {color} - Solid color mode
    g403-led cycle [{rate} [{brightness}]] - Cycle through all colors
    g403-led breathe {color} [{rate} [{brightness}]] - Single color breathing
    g403-led intro {on|off} - Enable/disable startup effect

Arguments:
    Color: RRGGBB (RGB hex value)
    Rate: 100-60000 (Number of milliseconds. Default: 10000ms)
    Brightness: 0-100 (Percentage. Default: 100%)
```
