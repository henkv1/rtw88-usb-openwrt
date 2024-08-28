# rtw88-usb-openwrt
OpenWrt kernel driver for RTW8812AU, RTW8821AU, RTW8811AU, RTW8822BU, RTW8812BU, RTW8822CU, RTW8821CU, RTW8811CU

Installation:
- Download the SDK for your device
- Update the package feeds: ./scripts/feeds update -a ; ./scripts/feeds install -a (see: https://openwrt.org/docs/guide-developer/toolchain/using_the_sdk for information on using the SDK)
- Run make menuconfig
- Clone this repository in package/kernel/rtw88: git clone https://github.com/henkv1/rtw88-usb-openwrt.git package/kernel/rtw88-usb
- Compile the package: make package/rtw88-usb/compile

The compiled package is named kmod-rtw88-usb_* and you can find it in the bin/target/*architecture*/*model*/packages/ directory. You can copy it to your device and install it using opkg install *package*. 

Please note that you also need to install the firmware packages for your device to make the module work.
