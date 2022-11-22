# <img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/Cordova.jpg" width="70" height="70">[Cordova](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html) 입문

# 완료 화면
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/finish3.JPG" width="300" height="600" align="left">
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/finish2.JPG" width="300" height="600" align="center">

# 파일 설명
[[test](https://github.com/alstjr7437/CordovaStudy/test)] 운동 소개 앱 / 자기 소개 앱 들어가 있는 android cordova <br>
[[hello](https://github.com/alstjr7437/CordovaStudy/hello)] 임시 테스트용 android cordova <br>
[[코르도바 앱 만들기 설정파일](https://github.com/alstjr7437/CordovaStudy/코르도바앱만들기설정파일.txt)] 코르도바 설정용 텍스트 파일<br>

# 기본 설정

## 1. JDK [다운로드](https://www.oracle.com/kr/java/technologies/javase/javase8-archive-downloads.html)
java 1.8.0_202 버전 설치하기(다른 버전은 오류가 남)

## 2.hybridapp 디렉토리 만들기
C드라이브에 hybridapp 만들기<br>
아래 부분 다운하기

### 2-1. Apache-ant [다운로드](https://ant.apache.org/bindownload.cgi)
apachec-ant 1.9.16 버전 압축 파일 다운해서 hybridapp 부분에 넣고 압축 풀기


### 2-2. Gradle [다운로드](https://gradle.org/releases/)
3.5 또는 7.3 버전 압축 파일 다운해서 hybridapp 부분에 넣고 압축 풀기

## 3. 안드로이드 스튜디오 [다운로드](https://developer.android.com/studio?hl=ko&gclid=Cj0KCQiAg_KbBhDLARIsANx7wAw8tCCqgA7kUvUSOFreHibtTyKrc_SRHAbREscrjQI7D2Cp6SBUXckaAqiaEALw_wcB&gclsrc=aw.ds)
### 3-1. 가상 기계(AVD) Nexus5 또는 Nexus 5X api29로 만들기
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/AVD%EB%A7%8C%EB%93%A4%EA%B8%B0.JPG" width="600" height="250"><br>
### 3-2. 안드로이드 플랫폼 패키지 추가 설치하기<br>

<b>설치 해야할 부분(없는것은 건너뛰기)</b>
- SDK platforms
	+ Android 12L	32
	+ Android 12	31
	+ Android 11	30
	+ Android R	29 
- SDK Tools
	+ Android SDK Tools
	+ Android SDK Platfor-tools
	+ Android SDK Build-tools
- Extra
	+ Android Support Repository
	+ Android Auto Desktop head unit emulator
	+ Android auto API simulator
	+ Google Repository
	+ Google USB Driver
	+ Google Play Services
	+ Android SDK Command-line Tools
	+ Intel x86 Emulator Accelerator(HAXM installer)
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/sdk%20%EC%84%A4%EC%A0%951.JPG" width="700" height="450">
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/sdk%20%EC%84%A4%EC%A0%952.JPG" width="700" height="450">
<hr>
주의) android-sdk에 설치 되는지 보기<br>
오류) 버전이 다운안됨 이라고 오류가 뜸<br>
해결법) android sdk settings > sdk location에 경로를 C:\Users\(사용자 이름)\AppData\Local\Android\android-sdk
이런식으로 android-sdk로 설정해야 android 31등 다운이 됨<br>


## 4. 환경 변수 설정하기(윈도우+r > cmd)
### 4-1. 시스템 변수 추가하기
- JAVA_HOME > C:\progrqm files\java\jdk1.8.0_202 <br>
  + java 다운되어 있는 폴더 설정 <br>
- ANDROID_SDK_ROOT	C:\Users\\(사용자이름)\AppData\Local\Android\android-sdk <br>
  + android-sdk 부분 폴더 설정 <br>
- GRADLE_HOME		C:\gradle-3.5
  + gradle 부분 폴더 설정 <br>
### 4-2. Path 설정하기 
%JAVA_HOME%\bin
%ANDROID_HOME%\tools
%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\build-tools
%ANDROID_HOME%\cmdline-tools\latest\bin
%ANDROID_HOME\emulator
%GRADLE_HOME%\bin
c:\HybridApp\apace-ant-1.9.16\bin

## 5. Node.js [다운로드](https://nodejs.org/ko/download/) 
cmd 창에서 <br>
node -v (node 버전 확인) <br>
npm -v (npm 버전 확인) <br>
npm update -g (npm 업데이트) <br>

## 6. phonegap(cordova 다운로드)
cmd 창에서 <br>
>npm install -g phonegap <br>
>npm install -g cordova <br>
>cordova -v <br>
>npm update -g phonegap <br>
>npm update -g cordova <br>

## 7. Android Cordova App 만들기
cmd 창에서(원하는 폴더에서) <br>
>mkdir \HybridProject <br>
>&nbsp; &nbsp; &nbsp; 프로젝트 파일 만들기 <br>
>cd \HybridProject <br>
>cordova create test com.example.test testApp -d  <br>
>&nbsp; &nbsp; &nbsp; Cordova test 파일 만들기(test부분 수정해서 파일명 변경 가능) <br>
>cd test 
>dir <br>
>dir platform <br>	
>&nbsp; &nbsp; &nbsp; 안되면 밑에 줄 해보고 하기 <br>
>cordova platform add android <br>
>&nbsp; &nbsp; &nbsp; android 플랫폼 추가하기 <br>
>dir platform <br> 
>&nbsp; &nbsp; &nbsp;안되면 dir platforms로 해보기 <br>

## 8.build.gradle(:app) 코드 추가하기
Android Studio 프로젝트 아무거나 만든 후 <br>
Gradle Scripts에 build.gradle(2번째꺼)에 android compileSdk 밑에 코드 추가하기<br>
```gradle
packagingOptions {
     exclude 'META-INF/DEPENDENCIES.txt'
     exclude 'META-INF/LICENSE.txt'
     exclude 'META-INF/NOTICE.txt'
     exclude 'META-INF/NOTICE'
     exclude 'META-INF/LICENSE'
     exclude 'META-INF/DEPENDENCIES'
     exclude 'META-INF/notice.txt'
     exclude 'META-INF/license.txt'
     exclude 'META-INF/dependencies.txt'
     exclude 'META-INF/LGPL2.1'
}
```
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/gradle%20%EC%B6%94%EA%B0%80.JPG" width="700" height="400">

## 9. AndroidManifest.xml 코드 추가하기
8번에서 만든 Android Studio 프로젝트에 <br>
manifests에 AndroidManifest.xml에 application 부분에 코드 추가하기<br>
```xml
android:largeHeap="true"
```
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/manifext%20%EC%84%A4%EC%A0%95.JPG" width="700" height="400">

## 10. debug.keystore 파일 삭제하기
C:\Users\[사용자명]\.android 내에 있는 debug.keystore 파일 삭제하기<br>
(삭제가 안될 경우 작업관리자(Ctrl+Alt+Del)에서 해당 프로세스 작업 끝내기 후에 삭제)<br>
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/debug%20%EC%82%AD%EC%A0%9C.JPG" width="700" height="400">

## 11. 프로젝트에 들어갈 html 부분 수정하기
App에 나올 html 부분에 첫번째를 index.html로 파일명 변경하기<br>
1. CDN 방식 > Download 방식으로 변경하기 <br>
2. script 추가
```html
<link rel="stylesheet" href="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css"/>
<script src="http://code.jquery.com/jquery-1.11.1.min.js"></script>
<script src="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js"></script>
<!--------- 각 링크에서 파일로 다운 후 파일에 옮겨준 후 ---------> 
<link rel="stylesheet" href="./css/jquery.mobile-1.4.5.min.css"/>
<script src="./js/jquery-1.11.1.min.js"></script>
<script src="./js/jquery.mobile-1.4.5.min.js"></script>
<!-- 헤드 부분에 코드 추가하기-->
<script src="cordova.js"></script>
```
## 12. 프로젝트 폴더 파일을 test 폴더에 www폴더에 복사하기
## 13. emulate 실행 (아이폰이거나 USB 없는 경우)
### 13-1. Android Studio에서 emulate 실행하기
### 13-2. cmd 코드 실행
test 폴더 부분까지 들어간 후 ``` >cordova emulate android ```  

## 14. 핸드폰 실행 (USB가 있고 Android폰일 경우)
### 14-1. 삼성 usb 드라이버 [다운로드](https://www.samsungsvc.co.kr/download)
### 14-2. USB 디버깅 [설정](https://m.blog.naver.com/dsmobile3550/221299587135)
### 14-3. 컴퓨터와 폰 연결
### 14-4. cmd 코드 실행
test 폴더 부분까지 들어간 후 ``` >cordova run android ```

