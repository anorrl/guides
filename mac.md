# Building a mac client (blocks)

## !!! READ !!! 

This is just stuff I wanted to write down so that other people who have the source code can build their own mac clients.

**ALSO THIS IS STILL A WORK IN PROGRESS AS I HAVE NOT COMPLETELY COMPLETED MY BUILD YET. (30/05/2026)**

## IMPORTANT THINGS TO KNOW.

Scrap all ideas of 32 bit (unless you want to go THAT far), if you want to support (mostly) all machines even to the newest you will need to scrap any ideas of building in 32 bit.
This guide will specifically target 64 bit builds.

Yes that also means you will need to build most of the libraries.

OpenSSL 1.0.2c needs some stupid patch to get `ROTATE` to properly build. No biggie tho.

If you are keeping Qt4 then you need to grab precompiled builds from a package manager like MacPorts or something like that since it WILL NOT build AND install (via the mpkg)

You WILL need to rebuild the CoreScriptConverter app.

### What you will need
- XCode 9
- Patience

# Contributors

- meditext - He knows the most about mac stuff, I'm just writing this down here for easier setup later on
- GlitchySavvy - this GOAT set up a Mojave VM on his ***AMD*** machine and let me remote access it to do all this

Cannot thank these people ENOUGH!
