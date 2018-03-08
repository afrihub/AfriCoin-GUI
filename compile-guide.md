# Linux (Tested with ubuntu)


git clone https://github.com/afrihub/AfriCoin-GUI.git
cd AfriCoin-GUI
git clone https://github.com/afrihub/AfriCoin.git
mv AfriCoin cryptonote
mkdir build; cd build
cmake .. ; make 


Start with updating and upgrading the current operating system

`sudo apt-get update; sudo apt-get upgrade`


Then start installing the necessary dependencies needed to compile the code.

`sudo apt-get remove qt5-default qttools5-dev-tools && sudo apt-get autoremove && sudo apt-get clean && sudo apt-get autoclean`

`sudo apt-get install build-essential libqt4-dev qt5-qmake cmake qt5-default python-sphinx texlive-latex-base inotify-tools openssl libssl-dev libdb++-dev libminiupnpc-dev git`

`sudo apt-get install sqlite3 libsqlite3-dev g++ libpng-dev gedit python gcc make libbz2-dev libdb-dev libssl-dev libreadline-dev autoconf libtool libleveldb-dev libblkid-dev e2fslibs-dev
sudo apt-get install libboost-all-dev qt5-default qttools5-dev-tools`


Now, download the repo (AfriCoin and GUI) so we can start too build the source and also entering the correct directory to build the files too.

`git clone https://github.com/afrihub/AfriCoin-GUI.git`

`cd AfriCoin-GUI`

`git clone https://github.com/afrihub/AfriCoin.git`

`mv AfriCoin cryptonote`

Now, we need to run cmake and make and the source files will start to build, once the percentage counter hits %100, you can locate the binaries in the src file.

`
mkdir build; cd build`

`cmake ..; make`



# Windows (Used windows server 2012)
We recommend compiling using a fresh device.

Start with downloading and installing the necessary dependencies:

* Microsoft Visual Studio 2017 (Link: https://www.visualstudio.com/downloads/)
* CMake 3.9.5 (Link: https://cmake.org/)
* Boost with MSVC 14.1 Support (Link: https://studiofreya.com/2017/04/23/building-boost-1-64-with-visual-studio-2017/)
* Git CLI (Link: https://desktop.github.com/)
* QT 5.5+ (With MSVC, you can use lower versions aslong as the extensions are correct)


Remeber to include the necessary paths for Command Prompt.
Also make a folder where you would like to download the source files too, then change '/path/dir/AfriCoin-Dev' to your location for your files.

Open Command Prompt (CMD)
`cd /path/dir/AfriCoin-Dev`

Procced to retrive the source code by
`git clone https://github.com/afrihub/AfriCoin.git; cd AfriCoin; mkdir build`

Then, procced to start the cmake proccess to generate the Visual Studio Project.
`cd build; cmake ..`

Now, when you enter the AfriCoin/build, you will see project file for visual studio, open this up and change Debug to Release and start the build.

Once, that is completed, you will need to go to src/Release and you will see the files there.

You will need to locate your qt install path and locate windeployqt.exe, then enter this in the folder with binaries.
`c:/qt/bin/windeploy.exe AfriCoin.exe`

This will grab all the neccesary *.ddls, and other extension to make the software portable.

