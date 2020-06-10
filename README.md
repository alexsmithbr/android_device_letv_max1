# Letv/Leeco Max1/X900 Device Tree

This is the device tree for Letv/Leeco Max1/X900, intended to be used with LineageOS.

**Note: This is not fully working yet. Use at your own risk.**

## Installation

We have three projects involved:

1. This one, which you should checkout to devices/letv/max1
2. https://github.com/alexsmithbr/android_device_letv_common.git, which you should checkout to devices/letv/common
3. https://github.com/alexsmithbr/android_kernel_letv_msm8994.git, which you should checkout to kernel/letv/msm8994

Once you have the above set up, you have to tell LineageOS you have this device ready to be built. You do this with:

```bash
cd <lineage_root>
source build/envsetup.sh
./device/letv/max1/setup-makefiles.sh
```

At this point, you can either:

```bash
breakfast lineage_max1-eng
breakfast lineage_max1-userdebug
breakfast lineage_max1-user
```

And then either:

```bash
mka recoveryimage
mka bacon
```

## Further information

Follow this thread on XDA: https://forum.xda-developers.com/android/help/help-building-lineageos-leeco-letv-t3894262/

