# Unity-Paths
Note on various unity specific paths and file handling related issues.(Note: written based on Unity 5.x, can be different on the previous version)


###iPhone

* **Application.persistentDataPath**: /var/mobile/Applications/[program_ID]/Documents  (read/write)
* **Application.dataPath**: /var/mobile/Applications/[program_ID]/[appname].app/Data  (read only)
* **Application.streamingAssetsPath**: /var/mobile/Applications/[program_ID]/[appname].app/Data/Raw   (read only)
* **Application.temporaryCachePath**: /var/mobile/Applications/[program_ID]/Library/Caches  (read/write)

###Android

####[External]
* **Application.persistentDataPath**: /mnt/sdcard/Android/data/[bundle id]/files  (read/write)
* **Application.dataPath**: /data/app/[bundle id-number].apk
* **Application.streamingAssetsPath**: jar:file:///data/app/[bundle id].apk!/assets  (read only, should access via WWW)
* **Application.temporaryCachePath**: /mnt/sdcard/Android/data/[bundle id]/cache

####[Internal]
* **Application.persistentDataPath**: /data/data/[bundle id]/files/  (read/write)
* **Application.dataPath**: /data/app/[bundle id-number].apk
* **Application.streamingAssetsPath**: jar:file:///data/app/[bundle id].apk!/assets  (read only, should access via WWW)
* **Application.temporaryCachePath**: /data/data/com.xxx.xxx/cache/

###WEB
read only

* **Application.persistentDataPath**: /
* **Application.dataPath**: folder in unity3d file
* **Application.streamingAssetsPath**: empty
* **Log**: C:\Users\username\AppData\Local\Temp\UnityWebPlayer\log\log_UNIQUEID.txt

###Window Player
* **Application.persistentDataPath**: [UserDirectory]/AppData/LocalLow/[Company]/[Product Name]  (read/write)
* **Application.dataPath**: [Exe file]/[Exe file]_Data : read/write
* **Application.streamingAssetsPath**: [Exe file]/[Exe file]_Data/StreamingAssets  (read/write)
* **Application.temporaryCachePath**: %LocalAppData%/Local/Temp/Temp/%Company%/%Product%
* **Log**: _EXECNAME_Data_\output_log.txt

###MAC Player
* **Application.persistentDataPath**: [UserDirectory]/Library/Caches/unity.[Company].[Product] (read/write)
* **Application.dataPath**: [Exe file].app/Contents
* **Application.streamingAssetsPath**: [Exe file].app/Contents/Data/StreamingAssets (read/write)
* **Log**: ~/Library/Logs/Unity/Player.log

###Window Editor
* **Application.persistentDataPath**: [UserDirectory]/AppData/LocalLow/[Company]/[Product]  (read/write)
* **Application.dataPath**: [ProjectDirectory]/Assets
* **Application.streamingAssetsPath**: [ProjectDirectory]/Assets/StreamingAssets	 (read/write)
* **Log**: C:\Users\username\AppData\Local\Unity\Editor\Editor.log

###MAC Editor
* **Application.persistentDataPath**: [UserDirectory]/Library/Caches/unity.[Company].[Product]  (read/write)
* **Application.dataPath**: [ProjectDirectory]/Assets
* **Application.streamingAssetsPath**: [ProjectDirectory]/Assets/StreamingAssets  (read/write)
* **Log**: ~/Library/Logs/Unity/Editor.log

##Other Editor paths (less knonwn)

It also provides less known various editor paths as the followings:

* Unity preferences folder
* Editor assembly path
* Engine assembly path
* External script editor path
* layout folder path
* Assetstore download folder path
* Editor log path


## References

* [Unity's Paths](http://masa795.hatenablog.jp/entry/2013/05/14/100024)
* [StandardPaths](https://github.com/nickgravelyn/UnityToolbag/tree/master/StandardPaths) on [UnityToolbag](https://github.com/nickgravelyn/UnityToolbag) github repository


##License

This code is distributed under the terms and conditions of the MIT license.

Except [UnityDiskSpacePlugin](https://github.com/asus4/UnityDiskSpacePlugin), the license of the that follow theirs.

Copyright (c)2016 Kim, Hyoun Woo
