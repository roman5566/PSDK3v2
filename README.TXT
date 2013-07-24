PSDK3 v2
Based on the work of Estwald, Marioga and other sceners and in bookstores as PSL1GHT, Tiny3D and PS3 SoundLib, PSDK3 intended to be a stable environment in PS3 homebrew programming under Windows, without external influences that threaten the integrity of the libraries, or applications that are built with them, when someone decides to change everything, breaking compatibility with applications built with those libraries and causing a clear prejudice. 
Here the motto is "if something works, do not touch" and you can add things, but not subtract, or fiddling with the code

What to do:

Download the ZIP (click on the download button).

Create in folder in the root of drive "C:" called "PSDK3v2" and unzip into the content (can be installed on other drives or directories * Make changing files. Bat, if you prefer, a posteriori)

MinGW.7z Extract the file (I use IZArc) and have the folder "MinGW" with the environment to Make, etc.

In PSDK3v2 \ MinGW \ msys \ 1.0 \ etc edit the file "profile" and at the end, where it says "export PS3SDK =" / c/PSDK3v2 "" changes the route you are going to use, if you want to launch the console (msys . bat) with the required environment variables.

Extract ps3dev.7z and have the folder "ps3dev" with PS3 compilers, and compiled the necessary libraries and utilities

What has the project:

MinGW: environment MinGW / MSYS installed specifically to work with the PS3 tools.

ps3dev: contains compilers, compiled external libraries and other supporting tools like scetool to sign applications (in replacement of geohot), create packages and some required DLL.

psl1ght: contains the library already compiled psl1ght

libraries-src: contains the source code of PSL1GHT, Tiny3D and PS3 SoundLib

project: contains the source code of the examples and files. bat to create the executables

Changing the installation path from C: to another

Apart from the changes mentioned above in / etc / profile (SoloFor the console), if you edit the Make *. Bat and change:

September PS3SDK = / F/PSDK3v2 September WIN_PS3SDK = F :/ PSDK3v2

by the corresponding path will suffice.

how to compile the source code
--------------------------------

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
