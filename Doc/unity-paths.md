Unity's Paths
=============

Unity의 내장된 경로는 아래의 것들이 있다.  

* Application.temporaryCachePath
* Application.streamingAssetsPath
* Application.dataPath
* Application.persistentDataPath


아래는 플랫폼별 경로에 대한 설명이다. 

iOS
---

* Application.persistentDataPath : /var/mobile/Applications/프로그램ID/Documents 
파일 읽기 쓰기 가능 
* Application.dataPath : /var/mobile/Applications/프로그램ID/앱이름.app/Data 
* Application.streamingAssetsPath : /var/mobile/Applications/프로그램ID/앱이름.app/Data/Raw 
파일 읽기 가능, 쓰기 불가능 


Android
-------

### External

* Application.persistentDataPath : /mnt/sdcard/Android/data/번들이름/files 
파일 읽기 쓰기 가능 
* Application.dataPath : /data/app/번들이름-번호.apk 
* Application.streamingAssetsPath : jar:file:///data/app/번들이름.apk!/assets 
파일이 아닌 WWW로 읽기 가능 

### Internal

* Application.persistentDataPath : /data/data/번들이름/files/ 
파일 읽기 쓰기 가능 
* Application.dataPath : /data/app/번들이름-번호.apk 
* Application.streamingAssetsPath : jar:file:///data/app/번들이름.apk!/assets 
파일이 아닌 WWW로 읽기 가능 

