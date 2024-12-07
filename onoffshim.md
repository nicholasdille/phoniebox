# OnOffShim

Check the [pinout](pins.md) which pins are used by the OnOffShim.

## Enable power down using the button

Mind that [Debian Bookworm has broken GPIO handling](https://github.com/pimoroni/clean-shutdown/issues/37).

Install the [daemon](https://github.com/pimoroni/clean-shutdown):

```bash
curl https://get.pimoroni.com/onoffshim >onoffshim.sh
sed -i 's|CONFIG=/boot/config.txt|CONFIG=/boot/firmware/config.txt|' onoffshim.sh
bash onoffshim.sh onoffshim
```

Add the following lines to `/boot/firmware/config.txt` (according to a [comment on #37](https://github.com/pimoroni/clean-shutdown/issues/37#issuecomment-1952129162)):

```plaintext
dtoverlay=gpio-shutdown,gpio_pin=17,active_low=1,gpio_pull=up
dtoverlay=gpio-poweroff,gpiopin=4,active_low=1
```

Replace all mentions of `raspi-gpio` with `pinctrl`:

```shell
sed -i 's/raspi-gpio/pinctrl/' /usr/bin/cleanshutd
```

Change lin 57 to:

```shell
pinctrl get $trigger_pin | grep -q "lo //"
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
trigger_pin=17
poweroff_pin=4
```
