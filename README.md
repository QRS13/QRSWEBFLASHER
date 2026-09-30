# QRS WEB FLASHER

A browser-based ESP32 firmware flasher. Firmware files are read locally in your browser and sent directly to your board over USB serial.

## Run it

Use Chrome or Edge on HTTPS or localhost:

1. Open PowerShell in this folder, run `py -m http.server 8000`, and visit <http://localhost:8000>.
2. Choose a serial speed and click **Connect**; select your ESP32's USB serial port.
3. Select or drop in one or more `.bin` firmware files and enter each flash address from the firmware release notes.
4. Choose **Flash firmware**. The output console displays connection and flashing progress.

The flasher uses Espressif's `esptool-js` from the `esm.sh` CDN when connecting, so an internet connection is needed for the flashing library. Firmware files are not uploaded to a server.

Check the firmware's release instructions before flashing; different projects use different addresses, and some require multiple `.bin` files. Each file needs an address before flashing. **Erase all flash** is optional and removes existing settings and data. Use the output panel's **Copy** and **Clear** buttons to manage its log.
