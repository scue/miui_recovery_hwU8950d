1 the project is build android recovery only;
2 before building, make sure copy project android_prebuilt, android_bionic and anroid_hardware to the directory ,which from ICS.
3 Steps as following:
    $. build/envsetup.sh
    $make crespo
  please see the out/patch_device/crespo/ , find recovery.img 
4 please check Makefile to obtain the supported devices;

# 
## 针对U8950d手机做了一些修改：
#
[中文]
1. 把外置sd卡挂载位置设置为/sdcard
2. 把内置sd卡挂载位置设置为/internal_sd
3. 添加了USB存储（参照patch_device/ville/init.conf）,默认挂载的是外置sd卡

[English]
1. change external_sd mount point on /sdcard (/external_sd -> /sdcard)
2. change internal_sd mount point on /internal_sdcard (/sdcard -> /internal_sd)
3. patch_device/hwU8950d/init.conf add USB storage(REF:patch_device/ville/init.conf),
   USB storage default mount external sdcard(which mount point is /sdcard).
