PSDK3 v2
========

Based on the work of Estwald, Marioga and other sceners and bookstores as PSL1GHT, Tiny3D and PS3 SoundLib, aims to be an environment PSDK3
stable on PS3 homebrew programming under Windows, without external influences that threaten the integrity of the bookstores, or the
applications that are built with them, when someone decides to change everything, breaking compatibility with applications created
with such a clear bookstores and causing injury. Here the motto is "if something works, do not touch" and can add things, but not
subtract, or fiddling pijoteramente the code.

What you have to do:

- Download the ZIP (on the button).

- Create in root C: folder called "PSDK3v2" and unzip the content (can be installed on other drives or directories
- changing Make files *. bat, if you prefer

- Extract the file MinGW.7z (I use IZArc) and You'll have the folder "MinGW" with the environment to Make, etc.

- In PSDK3v2 \ MinGW \ msys \ 1.0 \ etc edit the file "profile" and at the end, where it says "export PS3SDK =" / c/PSDK3v2 ""
change the route you are going to use, if you want to launch the console (msys.bat) with environment variables
necessary.

- Extract ps3dev.7z and You'll have the folder "ps3dev" with PS3 compilers, and compiled the necessary bookshops
and utilities

What has the project:

- MinGW: environment MinGW / MSYS installed specifically to work with the PS3 tools.

- Ps3dev: contains compilers, compiled external bookstores and other support tools such as scetool
to sign applications (in replacement of geohot), create packages, as well as some necessary DLL.

- Psl1ght: contains the library already compiled psl1ght

- Libraries-src: contains the source codes PSL1GHT, Tiny3D and PS3 SoundLib

- Project: contains the source codes and examples files. Bat to create the executables

Changing the installation path from C: to another
-------------------------------------------------

Apart from the changes mentioned above in / etc / profile (SoloFor the console), if you edit the Make *. Bat and change:

set PS3SDK = / F/PSDK3v2
set WIN_PS3SDK = F :/ PSDK3v2

the path that you, enough..

compiling the source on windows
----------

Make_clean.bat -> Delete all compiled files, except the. Pkg

Make_SELF.bat -> Creates a. Self signed with the keys 3.40 (by scetool)

Make_EBOOT.BIN.bat -> Create the self NPDRM EBOOT.BIN of the application. This is interesting, if upgrading is FTP one. Pkg
                       already installed

Make_PKG.bat -> Create the. Pkg to install the application.

The "scetool" requires a file with keys using a relative path. For this reason we have included utility "fake_scetool"
to support it.

ppu_rules has been modified in order to use this application. By default, it contains the keys in "SCETOOL_FLAGS". may
overburden defining SCETOOL_FLAGS: = yaadir more parameters with SCETOOL_FLAGS + =. The keys 3.40 operate in CFW we use
and that's why I have chosen.

The Makefile of reference have the examples of project / sample. Specifically, "fireworks3D" is an example of utilization joint
of Tiny3D and PS3 SoundLib and bookshops necessary

I hope these tools will be useful in your projects.

regards
