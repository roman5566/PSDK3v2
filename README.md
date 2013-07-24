PSDK3 v2
========

Basado en el trabajo de Estwald, Marioga y otros sceners y en librer�as como PSL1GHT, Tiny3D y PS3 Soundlib, PSDK3 pretende ser un entorno
estable de programaci�n de homebrew en PS3 bajo Windows, sin influencias externas que amenacen la integridad de las librer�as, ni de las 
aplicaciones que se construyen con ellas, cuando alguien decide cambiarlo todo, rompiendo la compatibilidad con las aplicaciones creadas 
con esas librer�as y provocando un claro perjuicio. Aqu� el lema es "si algo funciona, no lo toques" y se pueden a�adir cosas, pero no
restar, ni toquetear pijoteramente el c�digo.

What to do:

-Download the ZIP (on button).



- Created in root of C: the folder 'PSDK3v2' and decompresses within the content (can be installed on other drives or directories by changing 
The Make files * .bat, if you prefer, a posteriori) 

- Extracts the file MinGW.7z (i use IZArc) and you will find the folder 'MinGW' with the environment to make Make, etc. 

- In PSDK3v2 \MinGW\msys\1.0 \etc you edit the file 'profile' and in the end, where it says 'export PS3SDK= ' /c/PSDK3v2" 
Changes the route by which you wish to use, if you want to launch the console (msys.bat) with the environment variables 
Necessary.

 Pulls ps3dev.7z and you will find the folder 'ps3dev' with the compilers of the PS3, the thursday night pub crawls necessary already compiled 
And utilities 

What is contained in the draft: 

- MinGW: environment MinGW/MSYS fitted specifically to work with the tools of PS3. 

- PS3dev: contains the compilers, the thursday night pub crawls external compiled and other support tools, such as the scetool 
To sign applications (in replacement of of geohot), create packages, as well as some DLL necessary. 

- PSL1ght: contains the library psl1ght already compiled 

- Libraries-src: contains the codes sources of PSL1GHT, tiny3D and PS3 Soundlib 

- Project: contains the codes sources of the examples and the files .bat to create the executable 

Changing the installation path from C: to another 
-------------------------------------------------
 
SDL

Apart from the changes mentioned above in / etc / profile (SoloFor the console), if you edit the Make *. Bat and change:

September PS3SDK = / F/PSDK3v2
September WIN_PS3SDK = F :/ PSDK3v2

by the corresponding path, suffice.

compiling
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
