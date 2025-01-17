# xyzzy-mod
Wii console keys extractor.

Xyzzy is a homebrew application that allows the extraction of the OTP and SEEPROM Encryption Keys.

This modified version uses full hardware access through the HW_AHBPROT flag to read the OTP and SEEPROM chips, the System Menu binary and the ES module from the current IOS, in order to retrieve the console keys. Thus, it no longer installs a modified IOS11 nor uses PatchMii.

Other changes include:

* Compatibility with USB mass storage devices.
* Support for GCN controllers and newer WiiMotes.
* Retrieves SD IV, MD5 Blanker and MAC address.
* Besides generating a "keys.txt" file with a hexdump of every dumped key, which follows the format required by [wad2bin](https://github.com/DarkMatterCore/wad2bin), these files are also created:
    * "device.cert" (raw device certificate dump).
    * "otp.bin" (raw OTP memory dump).
    * "seeprom.bin" (raw SEEPROM memory dump) (Wii only).
    * "bootmii_keys.bin" (follows the BootMii keys.bin format) (Wii only).
    * "boot0.bin" (raw boot0 Mask ROM dump) (Wii only).
