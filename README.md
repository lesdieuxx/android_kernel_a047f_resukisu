# android_kernel_a047f_resukisu

- Includes **ReSukiSU** and **SUSFS**.
- Disabled Samsung security mechanisms.
- Set lz4 as default compressor for ZRAM.
- SELinux setenforce support.
- BFQ ioscheduler as default.
- All available CPU governors are enabled. (Default not changed, still energy_step)
- Enabled KSM (Kernel Samepage Merging). I don't know if this has usages other than virtualization but enabled it anyways.
- Timer frequency increased to 1000 Hz from 250 Hz.
- TCP Congestion algorithm set to BBR.
