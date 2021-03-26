# HifiBerry MiniAmp

Editieren von `/boot/config.txt`:

```bash
$ sudo vi /boot/config.txt
```

Dort müssen folgende Zeilen enthalten sein:

```plaintext
dtoverlay=hifiberry-dac
#dtparam=audio=on
```

Editieren von `/etc/asound.conf`:

```bash
$ sudo vi /etc/asound.conf
```

Folgender Inhalt muss enthalten sein:

```plaintext
pcm.hifiberry {
    type softvol
    slave.pcm "plughw:0"
    control.name "Master"
    control.card 0
} 
pcm.!default {
    type plug
    slave.pcm "hifiberry"
}
```

Neustarten:

```bash
$ sudo reboot
```

Prüfen:

```bash
$ aplay -l
```

Quelle: https://splittscheid.de/phoniebox-bauanleitung-toniebox-alternative/#ftoc-hifiberry-miniamp-einrichten
