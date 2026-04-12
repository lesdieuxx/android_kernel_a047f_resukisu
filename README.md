# Samsung A04s (SM-A047F) Kernel

Modified A04s android kernel with **ReSukiSU** and **SUSFS**.

> [!WARNING]
> Please **backup** your **data** and stock **boot.img** in case of bootloop etc.<br>
> I am not responsible for your lost data, broken device or Emu War.

# Changes

- Added ReSukiSU for KernelSU implementation. (Uses SUSFS inline hooks)
- Added SUSFS v2.1.0 with needed backports.
- Added BBG (Baseband Guard) with recovery protection. We don't want to get our recovery get nuked, do we? 
	- Boot partition is allowed for flashing kernel
- Enabled SELinux switch, ability to `setenforce 0/1`.
- Disabled Samsung securities.
- Set LZ4 for default compression algorithm for ZRAM.
- Enabled all available CPU governors.
- Set timer frequency to 1000 Hz.
- Set TCP congestion algorithm to BBR.

# Flashing

First backup your stock or download it so you can go back to it anytime if something breaks.

This kernel is released as AnyKernel3 so it is very easy to flash if you have custom recovery or root.

If you don't already have a custom recovery or root, use **TWRP** (recommended) or root the device with Odin and flash the kernel after that.

# Compatibility

This kernel is based on latest A047F kernel from vendor, which has binary value `SA`. It is pretty much backward compatible, tested with U4 baseband and its working.
Forward compatibility needs testing.

# Credits

- [physwizz](https://github.com/physwizz): AnyKernel3 script and general aspects for exynos850 development
