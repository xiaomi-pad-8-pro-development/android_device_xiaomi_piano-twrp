# TWRP device tree for the Xiaomi Pad 8 Pro (piano)

TWRP 16 recovery device tree.

## Build

Clone into a TWRP 16 source and build the recovery image:

```
git clone https://github.com/xiaomi-pad-8-pro-development/android_device_xiaomi_piano-twrp -b seventeen device/xiaomi/piano
source build/envsetup.sh
lunch twrp_piano-bp2a-eng
mka recoveryimage
```

The recovery is refused by the bootloader if its ramdisk is too big, so
the build checks the size and fails instead of making a broken image.

## Good to know

Decrypting data needs a recovery built with the same security patch level
as the firmware on the tablet. Rebuild after every HyperOS firmware update.
