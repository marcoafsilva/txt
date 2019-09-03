# Installing/Configurating Docker

## Quick Start

### 1 - First Step
#### Install Java

```
https://javadl.oracle.com/webapps/download/AutoDL?BundleId=238719_478a62b7d4e34b78b671c754eaaf38ab  
tar -vxf jre-8u211-linux-x64.tar.gz /opt/
```

### 2 - Second Step
#### Install Android SDK

```
cd $BASE_DIR
mkdir android-sdk
cd android-sdk
wget https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip
unzip sdk-tools-linux-4333796.zip
./tools/bin/sdkmanager "build-tools;28.0.3" "emulator" "platform-tools" "platforms;android-23" "tools"
```


### 3 - Third Step
#### Install Flutter

```
cd $BASE_DIR
wget https://storage.googleapis.com/flutter_infra/releases/beta/linux/flutter_linux_v1.1.8-beta.tar.xz
tar xvf flutter_linux_v1.1.8-beta.tar.xz
```


### 4 - Fourth Step
#### Export Vars (you can add them to your .bashrc)

```
export JAVA=/opt/java/bin
export JAVA_HOME=/opt/java

export ANDROID_SDK=$BASE_DIR/android-sdk
export ANDROID_PATH=$ANDROID_SDK/tools:$ANDROID_SDK/platform-tools
export FLUTTER=$BASE_DIR/bin
export PATH=$PATH:$JAVA:$PATH:$ANDROID_PATH:$FLUTTER
```


### 5 - Fifth Step
#### Checking it out

```
flutter doctor
```
