# OLED

See [here](https://splittscheid.de/phoniebox-display/#ftoc-installation-des-oled-display) for documentation

See [oled_phoniebox](https://github.com/splitti/oled_phoniebox) on GitHub

Install:

```bash
cd
rm o4p_installer.sh
wget https://raw.githubusercontent.com/splitti/oled_phoniebox/master/scripts/install/o4p_installer.sh
chmod +x o4p_installer.sh
./o4p_installer.sh
```

TODO: answers

The installer replaces the service for GPIO handling. Instead of `gpio_settings.ini` you must now use [`gpio-buttons.py`](gpio-buttons.py).
