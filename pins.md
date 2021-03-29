Use               | Pin Name          | Pin Number | Pin Number | Pin Name           | Use
:-----------------|:------------------|:----------:|:----------:|:-------------------|:---
OnOffShim         | 3V3 (Power)       |      1     |      2     | 5V (Power)         | OnOffShim
OLED              | GPIO2 (SDA I2C)   |      3     |      4     | 5V (Power)         | OnOffShim / OLED
OLED              | GPIO3 (SCL I2C)   |      5     |      6     | Ground             | Power LED
OnOffShim        | GPIO4             |      7     |      8     | SPIO14 (UART0 TXD) | Power LED
OLED         | Ground            |      9     |     10     | GPIO15 (UART0 RXD) | Available
OnOffShim         | GPIO17            |     11     |     12     | GPIO18             | HifiBerry MiniAmp
Available         | GPIO27            |     13     |     14     | Ground             | Previous song
Available        | GPIO22            |     15     |     16     | GPIO23             | Previous song
Available         | 3V3 (Power)       |     17     |     18     | GPIO24             | Available
Available         | GPIO10 (SPI MISO) |     19     |     20     | Ground             | Play/pause
Available         | GPIO9 (SPI MISO)  |     21     |     22     | GPIO25             | Play/pause
Available         | GPIO11 (SPI SCLK) |     23     |     24     | GPIO8 (SPI CE0)    | Available
Volume up         | Ground            |     25     |     26     | GPIO7 (SPI CE1)    | Volume up
Reserved          | ID SD (I2C ID)    |     27     |     28     | ID SC (I2C ID)     | Reserved
Volume down         | GPIO5             |     29     |     30     | Volume down             | Available
Available         | GPIO6             |     31     |     32     | GPIO12             | Next song
Available         | GPIO13            |     33     |     34     | Ground             | Next song
HifiBerry MiniAmp | GPIO19            |     35     |     36     | GPIO16             | HifiBerry MiniAmp
HifiBerry MiniAmp | GPIO26            |     37     |     38     | GPIO20             | HifiBerry MiniAmp
Available         | Ground            |     39     |     40     | GPIO21             | HifiBerry MiniAmp

Quellen:
- [HifiBerry MiniAmp](https://www.hifiberry.com/docs/hardware/gpio-usage-of-hifiberry-boards/)
- [OLED](https://cdn.shopify.com/s/files/1/1509/1638/files/0-96_inch_OLED_I2C_Display_-_pinout.pdf)
- [OnOffShim](https://de.pinout.xyz/pinout/onoff_shim#)
- [Potentiometer] (https://github.com/MiczFlor/RPi-Jukebox-RFID/wiki/Audio-RotaryKnobVolume) 