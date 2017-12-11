<img src="https://raw.github.com/t04glovern/office-christmas-lights/master/img/project-banner.png" data-canonical-src="https://raw.github.com/t04glovern/office-christmas-lights/master/img/project-banner.png" align="center"/>

<div align = "center">
    <h1>Office <em>Christmas</em> Lights </h1>
    <p>Infuse high levels of jolly into my co-workers.</p>
    <a href="https://manparvesh.mit-license.org/" target="_blank"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
    <a href="https://www.arduino.cc/" target="_blank"><img src="https://img.shields.io/badge/Platform-Arduino-blue.svg" alt="License"></a>
    <a href="https://travis-ci.org/t04glovern/office-christmas-lights" target="_blank"><img src="https://travis-ci.org/t04glovern/office-christmas-lights.svg?branch=master" alt="Build Status"></a>
</div>

## Setup

You can change the way the LED function using some of the variables found in `main.cpp`. Extra configuration around the colour definitions can be found in `main.h`

All credit for most of this implementation goes to [kriegsman's TwinkleFOX implementation](https://gist.github.com/kriegsman/756ea6dcae8e30845b5a)

```cpp
// Overall twinkle speed.
// 0 (VERY slow) to 8 (VERY fast).
// 4, 5, and 6 are recommended, default is 4.
#define TWINKLE_SPEED 4

// Overall twinkle density.
// 0 (NONE lit) to 8 (ALL lit at once).
// Default is 5.
#define TWINKLE_DENSITY 5

// How often to change color palettes.
#define SECONDS_PER_PALETTE 30
// Also: toward the bottom of the file is an array
// called "ActivePaletteList" which controls which color
// palettes are used; you can add or remove color palettes
// from there freely.

// If AUTO_SELECT_BACKGROUND_COLOR is set to 1,
// then for any palette where the first two entries
// are the same, a dimmed version of that color will
// automatically be used as the background color.
#define AUTO_SELECT_BACKGROUND_COLOR 0

// If COOL_LIKE_INCANDESCENT is set to 1, colors will
// fade out slighted 'reddened', similar to how
// incandescent bulbs change color as they get dim down.
#define COOL_LIKE_INCANDESCENT 1
```

## Platform IO

This project is build and run with PlatformIO. The library dependencies can be found in the `platformio.ini` file. Below is the current configuration targetting the Arduino Uno board. This can be changed to any variable of the Atmel AVR range.

```ini
[env:uno]
platform = atmelavr
board = uno
framework = arduino

lib_deps =
  FastLED@3.1.6
```

## License

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)