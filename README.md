# keithpod-flasher

Static ESP Web Tools page for the Waveshare ESP32-S3-Touch-AMOLED-2.06 watch. MIT. No secrets.

Intended to be served as GitHub Pages at `https://daddymean.github.io/keithpod-flasher/` from a public `Daddymean/keithpod-flasher` repository (this folder only: the page, the manifest, and the merged factory `.bin`). Until that repo exists, flash with [esptool-js](https://espressif.github.io/esptool-js/): Connect, 115200 baud, write `keithpod-waveshare_amoled206-factory.bin` at offset `0x0`.

Rebuild the binary from `firmware/keithpod`:

```
pio run -e waveshare_amoled206
```

The PlatformIO post-script refreshes the `.bin` and the version in `manifest.json`. Never commit `include/secrets.h` or any real Wi-Fi password, server URL, or device secret.
