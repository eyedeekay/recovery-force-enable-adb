
### flashable zip to force enables adb on recovery

Copy your adb public key.

`cat ~/.android/adbkey.pub > ./files/adb_keys`

Then to build the zip file

```
cd files
7z a "../force-enable-adb.zip"  ./*
```

If adb isnt working, you can mount MTP/Mass storage and copy the zip file to sdcard.

Then flash from the recovery, you should get adb.

### Tip
You can edit the update-binary which is a shell script, for correct sysfs path or USB Vendor/Product ID for your device.
