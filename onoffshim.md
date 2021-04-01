# OnOffShim

Check the [pinout](https://de.pinout.xyz/pinout/onoff_shim#) which pins are used by the OnOffShim.

## Enable power down using the button

Install the [daemon](https://github.com/pimoroni/clean-shutdown):

```bash
curl https://get.pimoroni.com/onoffshim | bash
```

... and reboot.

## Power LED

Enable the GPIO serial port by adding the following line to `/boot/config.txt`:

```
enable_uart=1
```

Connect the power LED to pin 8 (TxD) and pin 6 (GND) with a 330 ohm resistor.
