Triangles (TRI) "Black Pharao" Version 4.2.1.0 Release, 

* Adding 'address.o' (from the compiled triangles-qt's build folder) to the src/obj folder solved my trianglesd compiling issues. 
* Everything else is as is from https://github.com/wurstgelee/triangles.

Note: To compile on 18.04 you will need to downgrade SSL. Skip these REMOVE & INSTALL SSL commands if installing on 16.04 & just BUILD)
REMOVE & INSTALL SSL (for 18.04+)

sudo apt remove libssl-dev

sudo apt install libssl1.0-dev
BUILD

cd src/leveldb

chmod 755 *

cd ..

make -f makefile.unix

= = = 

wurstgelee's build recipe:

sudo apt-get update

sudo apt-get upgrade           

sudo apt-get install libqt4-designer libqt4-opengl libqt4-svg libqtgui4 libqtcore4 libqtwebkit4 qt4-dev-tools libqt4-dev

sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libqrencode-dev  libevent-dev libminiupnpc-dev libboost-dev libboost-all-dev

sudo apt-get install git

cd triangles/src/leveldb

chmod +x build_detect_platform

make clean

make libleveldb.a libmemenv.a

cd triangles/src

mkdir obj

make -f makefile.unix



