
Building the package
====================

\> sudo apt install cmake libsdl2-dev libboost-system-dev libboost-filesystem-dev libboost-date-time-dev libboost-locale-dev libfreeimage-dev libfreetype6-dev libeigen3-dev libcurl4-openssl-dev libasound2-dev libgl1-mesa-dev libvlc-dev

\> git clone https://github.com/ashwinm76/EmulationStation.git

\> git checkout debian/stretch

\> cd EmulationStation

\> gbp buildpackage --git-pristine-tar --git-pristine-tar-commit --git-upstream-tag='v%(version)s' --git-debian-branch=debian/stretch --git-export-dir=../build-area/


Adding patches
==============

\> gbp pq switch

Make your changes and commit them. The first line of the commit message will be the patch name.

\> gbp pq export --commit

Update and commit debian/changelog (and any other files in debian), if necessary.

Build the package again, as above.
