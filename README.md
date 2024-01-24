# fedora marathon installer
Fedora x86_64 Marathon Installer

Bash script specifically to install the AlephOne Engine with Marathon Trilogy (Bungie) in Fedora linux.

WARNING: if you use proprietary ffmpeg in a end-user application, look at the package changes before commiting. The user is responsible for any changes arising from ffmpeg.

WARNING UPDATE: So apparently the gnome desktop in fedora is not configured to use the Open source ffmpeg alternatives, however this causes an issue with some packages like OpenShot and OBS-Studio. The issue isn't related to the open source implementation of ffmpeg, but rather that OpenShot and OBS-Studio creates a dependancy issue when used between these files and what the repository calls for in the Gnome package group, where as OpenShot and OBS can work with the "free" version of FFMPEG(different from the open source packages), which then causes the error. So if you run into an issue with updating gnome, you MAY have to uninstall OBS and OpenShot first to complete the upgrade. This also seems to effect the Chromium Browser, however DNF just downgrades chromium instead of causing a dependancy issue. Wow, Fedora never ceases to amaze.

Requirements:
1. X86_64 Fedora linux or similar up-to-date rpm linux
2. DNF package manager
3. wget and the base C compiling tools
4. Configured Sudo to run the script

This script is a modified version of the pi-apps version(gplv3). It installs AlephOne and the 3 Marathon games for x86_64 fedora. The script is still very basic, I just tweaked some things so you can run the installer as a user. If you don't have dnf or you have a different architecture, it's up to you to make the right changes.
What it does. 1. installs redhat-lsb, but this isn't necessary for the current script state. 2. downgrades ffmpeg. 3. replaces proprietary ffmpeg with open-source replacements. 4. Installs all development dependencies. 5. Installs Marathon trilogy and cleans up after itself.
Enjoy!
./install to install. ./uninstall to uninstall

To link absolute path of the icons, go into .local/share/applications/marathon.desktop and link the icon paths.
