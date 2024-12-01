# OnOffShim

Check the [pinout](pins.md) which pins are used by the OnOffShim.

## Enable power down using the button

Install the [daemon](https://github.com/pimoroni/clean-shutdown):

```bash
curl https://get.pimoroni.com/onoffshim | bash
```

... and reboot.

## Power LED

Enable the GPIO serial port by adding the following line to `/boot/firmware/config.txt`:

```
enable_uart=1
```

Connect the power LED to pin 8 (TxD) and pin 6 (GND) with a 330 ohm resistor.

Configure `cleanshutd` in `/etc/cleanshutd.conf`:

```plaintext
#daemon_active=1
trigger_pin=17                                                                               #led_pin=off                                                                      poweroff_pin=4
#hold_time=1                                                                                 #shutdown_delay=0
#polling_rate=1
```
