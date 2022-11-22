# 코르도바 앱 입문
[Cordova](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html) <br>

# 파일 설명
[[test](https://github.com/alstjr7437/CordovaStudy/test)] 운동 소개 앱 / 자기 소개 앱 들어가 있는 android cordova <br>
[[hello](https://github.com/alstjr7437/CordovaStudy/hello)] 임시 테스트용 android cordova <br>
[[코르도바 앱 만들기 설정파일](https://github.com/alstjr7437/CordovaStudy/코르도바앱만들기설정파일.txt)] 코르도바 설정용 텍스트 파일<br>

# 기본 설정

## 1. JDK 설정
[jdk-8u162-windox-x64.exe](https://www.oracle.com/kr/java/technologies/javase/javase8-archive-downloads.html) <br>
java 1.8.0_202 버전 설치하기(다른 버전은 오류가 남)

## 2.hybridapp 디렉토리 만들기
C드라이브에 hybridapp 만들기

### 2-1. Apache-ant 설치하기
[apache-ant-1.9.16-bin.zip](https://ant.apache.org/bindownload.cgi)<br>
apachec-ant 1.9.16 버전 압축 파일 다운해서 hybridapp 부분에 넣고 압축 풀기


### 2-2. Gradle 설치하기
[Gradle](https://gradle.org/releases/)<br>
3.5 또는 7.3 버전 압축 파일 다운해서 hybridapp 부분에 넣고 압축 풀기

## 3. 안드로이드 스튜디오 설치
### 3-1. 가상 기계(AVD) Nexus5 또는 Nexus 5X api29로 만들기
<img src="https://github.com/alstjr7437/CordovaStudy/blob/main/img/AVD%EB%A7%8C%EB%93%A4%EA%B8%B0.JPG" width="600" height="250"><br>
### 3-2. 안드로이드 플랫폼 패키지 추가 설치하기<br>
주의) android-sdk에 설치 되는지 보기<br>
오류) 버전이 다운안됨 이라고 오류가 뜸<br>
해결법) android sdk settings > sdk location에 경로를 C:\Users\(사용자 이름)\AppData\Local\Android\android-sdk
이런식으로 android-sdk로 설정해야 android 31등 다운이 됨<br>

<b>설치 부분(없는것은 건너뛰기)</b>
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


## 4. 환경 변수 설정하기(윈도우+r > cmd)
- JAVA_HOME > c:\progrqm files\java\jdk1.8-- <br>
  + java 다운되어 있는 폴더 설정 <br>
- ANDROID_SDK_ROOT	C:\Users\(사용자이름)\AppData\Local\Android\android-sdk <br>
  + android-sdk 부분 폴더 설정 <br>
- GRADLE_HOME		C:\gradle-3.5
  + gradle 부분 폴더 설정 <br>
