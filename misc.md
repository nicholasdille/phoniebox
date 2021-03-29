# Miscellaneous

## Mopidy-Iris failed to scan local library

Make sure `/etc/sudoers` contains:

```
mopidy ALL=NOPASSWD: /usr/local/lib/python3.7/dist-packages/mopidy_iris/system.sh
```

## Volume fails to update

Make sure your `audio_ output` in `/etc/mpd.conf` uses a software mixer:

```
audio_output {
        type "alsa"
        name "My ALSA Device"
        mixer_control "Headphone"
        mixer_type "software"
}
```
