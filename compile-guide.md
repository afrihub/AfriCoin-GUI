# Linux (Tested with ubuntu)

Start with updating and upgrading the current operating system

`sudo apt-get update; sudo apt-get upgrade`


Then start installing the necessary dependencies needed to compile the code.

`sudo apt-get install libboost-all-dev cmake make g++ gcc git`


Now, download the repo (AfriCoin) so we can start too build the source and also entering the correct directory to build the files too.

`git clone https://github.com/afrihub/AfriCoin.git; cd AfriCoin; mkdir build; cd build`

Now, we need to run cmake and make and the source files will start to build, once the percentage counter hits %100, you can locate the binaries in the src file.

`cmake ..; make`


# Windows (Used windows server 2012)
We recommend compiling using a fresh device.

Start with downloading and installing the necessary dependencies:

* Microsoft Visual Studio 2017 (Link: https://www.visualstudio.com/downloads/)
* CMake 3.9.5 (Link: https://cmake.org/)
* Boost with MSVC 14.1 Support (Link: https://studiofreya.com/2017/04/23/building-boost-1-64-with-visual-studio-2017/)
* Git CLI (Link: https://desktop.github.com/)


Remeber to include the necessary paths for Command Prompt.
Also make a folder where you would like to download the source files too, then change '/path/dir/AfriCoin-Dev' to your location for your files.

Open Command Prompt (CMD)
`cd /path/dir/AfriCoin-Dev`

Procced to retrive the source code by
`git clone https://github.com/afrihub/AfriCoin.git; cd AfriCoin; mkdir build`

Then, procced to start the cmake proccess to generate the Visual Studio Project.
`cd build; cmake ..`

Now, when you enter the AfriCoin/build, you will see project file for visual studio, open this up and change Debug to Release and start the build.

Once, that is completed, you will need to go to src/Release and you will see the files there africoind, miner, simplewallet, walletd.
