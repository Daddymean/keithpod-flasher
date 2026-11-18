# keithpod-flasher

Static ESP Web Tools page for the Waveshare ESP32-S3-Touch-AMOLED-2.06 watch. MIT. No secrets.

Intended to be served as GitHub Pages at `https://daddymean.github.io/keithpod-flasher/` from a public `Daddymean/keithpod-flasher` repository (this folder only: the page, the manifest, and the merged factory `.bin`). Firmware v0.5.0: clips go to the Keithpod Companion Android app over Bluetooth LE (LE Secure Connections pairing with a 6-digit code on the watch; records stay AES-encrypted with the device secret and are deleted on the watch only after the phone confirms their SHA-256). The phone sets the clock, so Wi-Fi stays off by default. The AMOLED sleeps after 8 s and wakes on wrist raise, touch, or PWR.

Rebuild the binary from `firmware/keithpod`:

```
pio run -e waveshare_amoled206
```

The PlatformIO post-script refreshes the `.bin` and the version in `manifest.json`. Never commit `include/secrets.h` or any real Wi-Fi password, server URL, or device secret.
