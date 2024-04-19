# Move User Certs (Android 14)

Based on [this article](https://httptoolkit.com/blog/android-14-install-system-ca-certificate/).

This Magisk module moves certificates from the user certificate store to the system store.

## Why would I want user certificates in my system store?

Mainly to intercept traffic using your own CA certs from i.e. Burp. 
This module is mainly focused to fix the "burden" of injecting the certificates manually into zygote after each reboot of the device.

## Important Notice

This was solely created for Android 14, not higher not lower. If you need this functionality but for older versions of Android use [Move Certficates](https://github.com/Magisk-Modules-Repo/movecert).

## Usage

1. Download the `.zip` file from the [latest release](https://github.com/DimuHvH/moveusercerts/releases)].
2. Go to *Magisk -> Modules -> Install from storage* and select the downloaded `.zip` file.
3. Reboot.

If a new version comes out (prob wont), repeat steps.

The module does its work during the system boot. If you add new certificate(s),
you'll have to reboot the device for the new certificate to be copied to the system store.

## Building
```shell
./dist.sh
```
