# About this repository
> This repository is based on [P3TERX/Actions-OpenWrt](https://github.com/P3TERX/Actions-OpenWrt) AND [chrisblue/OpenWrt-Multi](https://github.com/chrisblue/OpenWrt-Multi)

Use Github Actions Automatically compile firmware for Redmi AX6

## Usage(AX6)

1. Upload your own `AX6.config` file
2. Enter the Actions page to manually start the compilation
3. When the compilation is complete, download the compiled `xxx-factory.ubi` firmware on the Releases page (if you want to upgrade under op, download the firmware with the suffix `xxx-sysupgrade.bin`)
4. If you have previously flashed dual systems to AX6, please enter `fw_setenv flag_last_success 1` and `fw_setenv flag_boot_rootfs 1` and then restart the device to switch the system (if not, please click the [reference link(Please solve the translation problem yourself)](https://www.right.com.cn/forum/thread-6054985-1-1.html) to install the dual system)
5. Upload the firmware with the suffix of .ubi via scp
6. Flashing in the firmware `ubiformat /dev/mtd13 -y -f /tmp/openwrt-xxx-redmi_ax6-squashfs-nand-factory.ubi` PS: The file name is just an example. When flashing in, the ubi file name you downloaded will prevail
7. Enter `fw_setenv flag_last_success 0` and `fw_setenv flag_boot_rootfs 0` and then restart the device

## Default IP address and password
   | project | value |
   | :--- | :--- |
   | Default IP address | `192.168.10.1` |
   | Default password | `password` |
