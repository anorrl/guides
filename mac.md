# Building a mac client (blocks)

## !!! READ !!! 

This is just stuff I wanted to write down so that other people who have the source code can build their own mac clients.

**ALSO THIS IS STILL A WORK IN PROGRESS, I HAVE IT BUILT THO!**

> While it has been built, I had issues with running it. I forgot now but it kept crashing on boot.
> I was using the latest XCode 9 along with MacOS Mojave.

## IMPORTANT THINGS TO KNOW.

Scrap all ideas of 32 bit (unless you want to go THAT far), if you want to support (mostly) all machines even to the newest you will need to scrap any ideas of building in 32 bit.
This guide will specifically target 64 bit builds.

Yes that also means you will need to build most of the libraries.

OpenSSL 1.0.2c needs some stupid patch to get `ROTATE` to properly build. No biggie tho.

If you are keeping Qt4 then you need to grab precompiled builds from a package manager like MacPorts or something like that since it WILL NOT build AND install (via the mpkg)

You WILL need to rebuild the CoreScriptConverter (CSC) app, **do this BEFORE building the client. The build process requires it.**

### What you will need
- XCode 9 (latest)
- Patience
- most of the common Contribs like boost 1.56.0, SDL2.0.4 etc

Before building the MacClient, you NEED to build the CSC **FIRST**

If you're having issues with reflection.h use the patched up one here in this repo! (by meditext)

You need to set everything to be 64 bit in ALL projects (and targets), along with the compiler set to libstdc++ with GNU99

they ALL have to be the same because they won't be linked and the build fails.

Also forget about CONTRIB_PATH here because i can't seem to get it to work functionally, so if you figure it out good on you but otherwise you need to update the includes/libraries/references to be absolute paths.

### Patches

# Contributors

- meditext - He knows the most about mac stuff, I'm just writing this down here for easier setup later on
- GlitchySavvy - this GOAT set up a Mojave VM on his ***AMD*** machine and let me remote access it to do all this

Cannot thank these people ENOUGH!
