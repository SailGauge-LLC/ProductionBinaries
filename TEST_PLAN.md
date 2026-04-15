SailGauge Production Firmware Test Plan

Flash these images in order to verify that the Flutter app reports the same
packed firmware version byte that the production firmware and BLE updater now
share.

1. `sailgauge_blue_red_led_v8.6.0.bin`
   - Expected app firmware version: `8.6.0`
   - Expected LED identity pattern: blue/red alternating

2. `sailgauge_blue_green_led_v8.7.0.bin`
   - Expected app firmware version: `8.7.0`
   - Expected LED identity pattern: blue/green alternating

3. `sailgauge_green_red_led_v8.8.0.bin`
   - Expected app firmware version: `8.8.0`
   - Expected LED identity pattern: green/red alternating

Suggested verification flow:

1. Program one image.
2. Reboot the device.
3. Connect from the Flutter app.
4. Confirm the reported firmware version matches the file name.
5. Confirm the LED identity pattern matches the file name.
6. Repeat with the next image.

