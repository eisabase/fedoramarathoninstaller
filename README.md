# fedoramarathoninstaller
Fedora x86_64 Marathon Installer

Bash script specifically to install the AlephOne Marathon Trilogy in Fedora linux.

WARNING: if you use proprietary ffmpeg in a end-user application, look at the package changes before commiting. The user is responsible for any changes arising from ffmpeg.

Requirements:
1. Fedora linux
2. DNF pacakge manager
3. wget and the base C compiling tools

This script is a modified version of the pi-apps version(gplv3). It installs AlephOne and the 3 Marathon games for x86_64 fedora. The script is still very basic, I just tweaked some things so you can run the installer as a user. If you don't have dnf or you have a different architecture, it's up to you to make the right changes.
What it does. 1. installs redhat-lsb, but this isn't necessary for the current script state. 2. downgrades ffmpeg. 3. replaces proprietary ffmpeg with free replacements. 4. Installs all development dependancies. 5. Installs Marathon trilogy and cleans up after itself.
Enjoy!
./install to install. ./uninstall to uninstall

To link absolute path of the icons, go into .local/share/applications/marathon.desktop and link the icon paths.
