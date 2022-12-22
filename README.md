TWRP Device Tree for JIO JHSD200 (franklin)
===================================

The JIO JHSD200 (codenamed _"JHSD200"_ or _"franklin"_) have following parameters:

Basic                   | Spec Sheet
-----------------------:|:-------------------------
CPU                     | Octa-core Amlogic S905X2
GPU                     | Mali-G31 MP2 Dvalin
Shipped Android Version | Android 9
Memory                  | 8/32gb
Network                 | Gigabit Ethernet, WIFI 802.11 b/g/n/ac, Bluetooth 4.0
Video                   | HDMI 2.1 to 4K with 60 Hz + HDR, AV 3,5mm.
USB                     | USB 3,0x1, USB 2,0x1
Power Supply            | 5W/2A
Misc			| IR-port

![JIO JHSD200](https://github.com/0xNoob-bash/DumprX-CI/raw/main/jio-set-top-box-six-ott.jpg "JSD200")

## Compile

First checkout Minimal TWRP with OmniROM Tree:

```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
repo sync
```

And execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true # Only if using Minimal TWRP Tree
. build/envsetup.sh
lunch omni_JHSD200-eng
mka recoveryimage
``
