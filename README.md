# raspbian-f2fs

script takes .zip image, and either:
- creates a f2fs sdcard (partition resize on the go, double check the sdcard device name)
- creates a f2fs new image to flash (not resized)

In either case it boots, further tests are needed.

I could not find a way to resize the f2fs partition, so the sdcard method is prefered.
