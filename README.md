# Raspberry Pi OS installer on F2FS

last tested on: 2022-01-28-raspios-bullseye-armhf-lite.zip

This script takes the .zip image, and either:
- creates a f2fs sdcard (partition resize on the go) [PREFERRED METHOD]
- creates a f2fs new image to flash (NOT live-resizable)

In either case it boots, further tests are needed.

NOTE: f2fs cannot be live-resized, so prefer the sdcard method.

When using the image method,
- default image size is increased by 500MB
- the package 'f2fs-tools' must be apt-installed
- once booted: resize.f2fs /dev/mmcblk0p2   <- "Error: Not available on mounted device!"
