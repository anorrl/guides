# Setting up the source (blocks)

## Ok here's what you need:
- [The Contribs](https://archive.org/download/contribs.-7z/Contribs.7z)
- [Visual Studio 2012](https://archive.org/download/en_visual_studio_professional_2012_x86_dvd_2262334/en_visual_studio_professional_2012_x86_dvd_2262334.iso) (For build tools)
- Any visual studio higher than 2012 (or you could use the provided vs2012)
- Obviously the source.

Ok so first off, you need to set a new **SYSTEM** environment variable named **CONTRIB_PATH** that points to the directory you have EXTRACTED the Contribs.7z at.
This is CRUCIAL as it is needed for the uhm project to even build.

You also need to change instances of ROBLOX_BOOST_CONFIGS to ANORRL_BOOST_CONFIGS in the boost library if you're compiling the ANORRL client.

## IMPORTANT THINGS!
- use `Release` to build `WindowsClient`
- use `ReleaseStudio` to build `RobloxStudio`
- use `ReleaseRCC` to build `RCCService`

DO NOT BUILD IN THE WRONG CONFIGURATION IT WILL PRODUCE IN A MESSED UP BINARY!

If the build configuration of the projects in the solution are NOT Visual Studio 2012 then change them to be configured as such, unless it compiles fine...

DO NOT USE VS2013. the compiler bugs out a fuck ton and fails to compile.
