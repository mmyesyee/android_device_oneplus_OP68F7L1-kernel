# Prebuilt kernel for OnePlus PYS110 (OP68F7L1)

`Image` is the stock uncompressed arm64 kernel (`Linux kernel ARM64 boot
executable Image, little-endian, 4K pages`, 35,772,928 bytes) extracted from the
ColorOS 16 (Android 16, `UKQ1.231108.001`) boot image of the device.

It is used because this LineageOS tree does not build a kernel: `boot` and
`init_boot` are never flashed either (the stock `init_boot` carries KernelSU),
and `vendor_boot` / `dtbo` stay stock. `device/oneplus/mt6878-common` sets the
boot header v4 parameters, and the device tree points `TARGET_PREBUILT_KERNEL`
at this file.

Source kernel (if a rebuild is ever needed):
`OnePlusOSS/android_kernel_oneplus_mt6878` (`oneplus/mt6878_b_16.0.0_pad_go_2`)
with `OnePlusOSS/android_kernel_modules_and_devicetree_oneplus_mt6878`.
