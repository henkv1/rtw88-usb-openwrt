# rtw88-usb-openwrt
OpenWrt kernel driver for RTW8812AU, RTW8821AU, RTW8811AU, RTW8822BU, RTW8812BU, RTW8822CU, RTW8821CU, RTW8811CU, RTW8723DU

Installation:
- Download the SDK for your device
- Update the package feeds: ./scripts/feeds update -a ; ./scripts/feeds install -a (see: https://openwrt.org/docs/guide-developer/toolchain/using_the_sdk for information on using the SDK)
- Run make menuconfig
- Clone this repository in package/kernel/rtw88. Specify the desired branch with -b *branch*: git clone -b snapshot https://github.com/henkv1/rtw88-usb-openwrt.git package/kernel/rtw88-usb
- Compile the package: make package/rtw88-usb/compile

The firmware package is named rtw88-firmware* and you can find it in the bin/packages/*architecture*/base/ directory. 
The kernel module package is named kmod-rtw88-usb_* and you can find it in the bin/target/*architecture*/*model*/packages/ directory. You can copy both packages to your device and install it using opkg install *package*. 

Please note that you need to install both packages for your device to make the module work.
