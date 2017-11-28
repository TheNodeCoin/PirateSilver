## Snatching some Pirate Silver booty. Arrrrrrrrr! #
![alt text][logo]

[logo]: http://www.yim778.com/data/out/57/825665.jpg "ARRRRRR"

### On Linux

For beginners, From Scratch:

Open a terminal [ctrl+alt t]

Dependencies to build and use: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.55.

Copy & Paste.  Reference - [ctrl+shift c]- copy in terminal [ctrl+shift v]- paste in terminal

`sudo apt update`
`sudo apt upgrade`
`sudo apt install git screen gcc g++ build-essential cmake libboost-all-dev`

OR, You may download them from:

* http://gcc.gnu.org/
* http://www.cmake.org/
* http://www.boost.org/
* Alternatively, it may be possible to install them using a package manager.

Clone Github.com Repo:

Prep:
In terminal after dependencies are installed, you can `cd` (change directory) to an existing folder, or create another one with `sudo mkdir folder_name`. Change directory to that folder `cd folder_name`.

Copy & Paste in terminal.
`git clone https://github.com/TheNodeCoin/PirateSilver.git`
`cd PirateSilver && make`

Starting Pirate daemon.

After the coin is 100% built, `cd build/release/src`.
You can choose to run the Pirate Coin in the current terminal `./piratesilver`.  However, closing the terminal will shutdown the daemon.  Alternatively, you can run PS in screen `sudo screen ./piratesilver`.  This allows you to detach [ctrl+a d] the screen leaving it running while closing the terminal.  To reattach the screen simply open a terminal [ctrl+alt t] and type `sudo screen -r`.

Congrats, You are now running a Pirate node.

Build Overview:

In order to build, you will have to change the directory to where the cloned git is located, and run `make`. The resulting executables can be found in the same directory under `build/release/src`.

Starting wallet:
`cd PirateSilver/build/release/src && ./simplewallet`.  Follow the instructions and type `help` for list of commands.  You can start mining in the daemon with `start_mining`.  Good luck!

**Advanced options:**

* Parallel build: run `make -j<number of threads>` instead of `make`.
* Debug build: run `make build-debug`.
* Test suite: run `make test-release` to run tests in addition to building. Running `make test-debug` will do the same to the debug version.
* Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++` before running `make`.

### On Windows
Dependencies: MSVC 2013 or later, CMake 2.8.6 or later, and Boost 1.55. You may download them from:

* http://www.microsoft.com/
* http://www.cmake.org/
* http://www.boost.org/

To build, change to a directory where this file is located, and run theas commands: 
```
mkdir build
cd build
cmake -G "Visual Studio 12 Win64" ..
```

And then do Build.
Good luck!
