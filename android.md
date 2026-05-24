# Building an android client (blocks)

## Please READ!
This is just stuff I wanted to write down so that other people who have the source code can build their own android clients.

**ALSO THIS IS STILL A WORK IN PROGRESS AS I HAVE NOT COMPLETELY COMPLETED MY BUILD YET. (24/05/2026)**

## What you need:
- Android Studio 2.2.3 (min. 1.1.0)
- The latest version of Java 7 **JDK**
- android-ndk-r10e (MUST BE THIS VERSION)
- cmake 2.8.12.2 + ninja (MUST BE THIS VERSION)
- Some Unix environment (terminal emulator or system, **REQUIRED**)

> if you have Contribs already setup, this will be faster but be aware there are still more libraries you need to get.

## Contribs you need
first off you need to have these new contribs in a new `android/arm` folder

e.g `{CONTRIB_PATH}/android/arm/openssl/openssl1.0.2c/`

- Google Breakpad (somewhere in May 2014 under `google-breakpad/20MAY2014`)
> Note: you need to find the `src/third_party/lss/linux_syscall_support.h` file.
- openssl 1.0.2c (under `openssl/openssl1.0.2c`)
- curl-7.43.0 (under `curl/curl-7.43.0`)

# end for now
