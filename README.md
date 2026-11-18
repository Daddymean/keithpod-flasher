# keithpod-flasher

Static ESP Web Tools page for the Waveshare ESP32-S3-Touch-AMOLED-2.06 watch. MIT. No secrets.

Intended to be served as GitHub Pages at `https://daddymean.github.io/keithpod-flasher/` from a public `Daddymean/keithpod-flasher` repository (this folder only: the page, the manifest, and the merged factory `.bin`). Firmware v0.4.0: the AMOLED sleeps after 8 s and wakes on wrist raise, touch, or PWR. Recording keeps going while the screen is dark.

Rebuild the binary from `firmware/keithpod`:

```
pio run -e waveshare_amoled206
```

The PlatformIO post-script refreshes the `.bin` and the version in `manifest.json`. Never commit `include/secrets.h` or any real Wi-Fi password, server URL, or device secret.
