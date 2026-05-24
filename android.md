
# Building an android client (blocks)

## !!!! READ !!!!
This is just stuff I wanted to write down so that other people who have the source code can build their own android clients.

**ALSO THIS IS STILL A WORK IN PROGRESS AS I HAVE NOT COMPLETELY COMPLETED MY BUILD YET. (24/05/2026)**

## What you need:
- Android Studio 2.2.3 (min. 1.1.0)
- The latest version of Java 7 **JDK**
- android-ndk-r10e (MUST BE THIS VERSION)
- cmake 2.8.12.2 + ninja (MUST BE THIS VERSION)
- Some Unix environment (terminal emulator or system, **REQUIRED**)

### Small note
Please make sure the client folder (the entire codebase) is NOT named `Build` as it is meant to be called anything else such as `Client`. However, make the `Build` folder outside of the project (as that is where the cmake scripts will be generated at.)

> Note: if you have Contribs already setup, this will be faster but be aware there are still more libraries you need to get.

## Those more libraries you need
first off you need to have these new contribs in a new `android/arm` folder

e.g `{CONTRIB_PATH}/android/arm/openssl/openssl1.0.2c/`

- Google Breakpad (somewhere in May 2014 under `google-breakpad/20MAY2014`)
> Note: you need to find the `src/third_party/lss/linux_syscall_support.h` file.
- openssl 1.0.2c (under `openssl/openssl1.0.2c`)
- curl-7.43.0 (under `curl/curl-7.43.0`)

## Fixes (before building)
### build.gradle
At the root of the Android project you should see a `build.gradle` file.

Replace its contents with the following:
```
// Top-level build file where you can add configuration options common to all sub-projects/modules.
buildscript {
    repositories {
        mavenCentral()
        maven { url 'https://maven.fabric.io/public' }
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.2.3'
        classpath 'io.fabric.tools:gradle:1.25.4'
    }
}
```
> Note: The gradle version **must** match the Android Studio version you use.

### App
In the App project there is a CMakeLists.txt file, open that up and add the line as shown below. 

```
... ysics)

project(libwww C CXX)

include_proje...
```
This should be added BEFORE the libwww stuff (but after the includes), this is just so that the compiler won't complain about the C/C++ cross compiling during the build.

## Building libroblox.so
Before doing anything, you NEED to build the `libroblox.so` object. 

To do this, go to the `cmake` folder and run the `configure-android.sh` inside. Once that has been ran (successfully), there should be new folders such as `release`, `noopt` and `debug`.

For this we will select the `release` folder. 

Run `make` inside the folder. 

It should now begin building. Good luck.

# This guide is most likely not complete.
