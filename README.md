# rtw88-usb-openwrt
OpenWrt kernel driver for RTW8812AU, RTW8821AU, RTW8811AU, RTW8822BU, RTW8812BU, RTW8822CU, RTW8821CU, RTW8811CU

Installation:
- Download the SDK for your device
- Update the package feeds: ./scripts/feeds update -a ; ./scripts/feeds install -a (see: https://openwrt.org/docs/guide-developer/toolchain/using_the_sdk for information on using the SDK)
- Run make menuconfig
- Clone this repository in package/kernel/rtw88: git clone https://github.com/henkv1/rtw88-usb-openwrt.git package/kernel/rtw88-usb
- Compile the package: make package/rtw88-usb/compile
