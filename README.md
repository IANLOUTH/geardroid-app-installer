# Geardroid
## An installer for Guardian Project Apps

*I put this together to save some time after flashing my Nexus 7. In the future this will be better written and will also include AOSP image releases with kernel and system improvements.*

Tested on a Nexus 7 (flo) running Android AOSP 5.0.2r1.

#### Apps
* SuperSU 2.45
* ChatSecure v14.0.9
* F-Droid 0.78
* GNU Privacy Guard 0.3
* Orbot v14.1.4
* Orweb 0.7
* Bitmaask 0.9.0
* i2p 0.9.17.1
* GNU Privacy Guard 0.3
* Terminal Emulator for Android from @Jackpal

#### Requirements
* Nexus 7 2013 (WiFi) [Flo]
* Android Lollipop (for included Orbot)
* Fastboot & ADB
* CWM Recovery (installable from script).
* sha256sum
* curl
* GnuPG/GPG
* Java Runtime

#### Usage
```bash
dani@gearbench:~/geardroid$ ./build

-[ Building Geardroid ]-

* Fetching SuperSU 2.45
* Fetching Applications
* Verifying binaries...
	[OK] SuperSu
	[OK] i2p
	[OK] Bitmask
	[OK] Terminal
	[OK] org.fdroid.fdroid_780.apk
	[OK] Orbot-v14.1.4-LollipopPIE.apk
	[OK] Orweb-release-0.7.apk
	[OK] ChatSecure-v14.0.9.apk
	[OK] GnuPrivacyGuard-release-0.3.apk

Signature verification successful.

Would you like to test APKs? (y/n) y
	[Testing] Bitmask-Android-0.9.0.apk... jar verified.
	[Testing] ChatSecure-v14.0.9.apk... jar verified.
	[Testing] GnuPrivacyGuard-release-0.3.apk... jar verified.
	[Testing] i2p.apk... jar verified.
	[Testing] Orbot-v14.1.4-LollipopPIE.apk... jar verified.
	[Testing] org.fdroid.fdroid_780.apk... jar verified.
	[Testing] Orweb-release-0.7.apk... jar verified.
	[Testing] term.apk... jar verified.
```

##### Installing
```bash
dani@gearbench:~/geardroid$ ./install 

Installing Geardroid requires ClockworkMod Recovery.

Would you like to install CWM Recovery? (y/n) y
Please enable USB debugging, connect Nexus 7 then press [enter]...

4485 KB/s (43874648 bytes in 9.552s)

Rebooting into bootloader...
Installing recovery image...
sending 'recovery' (9094 KB)...
OKAY [  0.291s]
writing 'recovery'...
OKAY [  0.505s]
finished. total time: 0.797s

Please reboot into bootloader by holding VOLUME DOWN and POWER
Then select Recovery from the menu to continue

From the recovery menu: 
-> select: install zip 
-> choose zip from /sdcard 
-> update-SIGNED.zip

After the script finishes reboot your Nexus 7 and you're done!
Remember to configure Tor and/or Bitmask as soon as WiFi is enabled.

All complaints to dani@gearbench.uk, @DaniGearbench or /dev/null

```
