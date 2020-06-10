# Letv/Leeco Max1/X900 Device Tree

This is the device tree for Letv/Leeco Max1/X900, intended to be used with LineageOS.

**Note: This is not fully working yet. Use at your own risk.**

## Installation

We have three projects involved:

1. This one, which you should checkout to devices/letv/max1
2. https://github.com/alexsmithbr/android_device_letv_common.git, which you should checkout to devices/letv/common
3. https://github.com/alexsmithbr/android_kernel_letv_msm8994.git, which you should checkout to kernel/letv/msm8994

Once you have the above set up, extract the proprietary blobs and set up the device:

```bash
cd <lineage_root>
source build/envsetup.sh
cd device/letv/max1
```

**Option 1:** from plugged-in device

Ensure your device is plugged-in and accessible via adb, then:

```bash
./extract-files.sh
```

**Option 2:** from a local tree

Supposing your device tree lies at ~/android/system_dump/max1_complete_tree/:

```bash
./extract-files.sh ~/android/system_dump/max1_complete_tree/
```

The above will also run setup-makefiles.sh, so the device will be seen by breakfast.

Now you can either:

```bash
breakfast lineage_max1-eng
breakfast lineage_max1-userdebug
breakfast lineage_max1-user
```
And then build.

To create a recovery image:

```bash
mka recoveryimage
```

To do a complete build:

```bash
mka bacon
```

## Further information

Follow this thread on XDA: https://forum.xda-developers.com/android/help/help-building-lineageos-leeco-letv-t3894262/

