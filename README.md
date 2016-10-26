# mbed driver for EA DOGM displays

This repository contains a mbed driver for EA DOGM 128x64 displays (http://www.lcd-module.com/eng/pdf/grafik/dogm128e.pdf). It's adapted from https://github.com/adafruit/ST7565-LCD, with modifications to work with this particular type of display.

Usage:

```
#include "mbed.h"
#include "ST7565.h"

ST7565 glcd(p5, p7, p8, p9, p10); // mosi, sclk, a0, rst, cs

int main() {
    glcd.begin(0x17);
    glcd.clear();
    glcd.drawstring(0, 0, "Welcome to MBED!");
    glcd.display();
    while (true);
}
```

Tested with a mbed LPC1768 board.
**Preliminary version**. Works, but certainly needs improvement.

