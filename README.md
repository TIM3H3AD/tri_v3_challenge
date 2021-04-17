Triangles (TRI) "Black Pharao" Version 4.2.1.0 Release, 

  -added a pre-compiled address.o to the src/obj folder. Everything else is as is from wurstgelee.

  wurstgelee's build recipe:

  sudo apt-get update
  sudo apt-get upgrade           

  sudo apt-get install libqt4-designer libqt4-opengl libqt4-svg libqtgui4 libqtcore4 libqtwebkit4 qt4-dev-tools libqt4-dev gcc-4.9

  sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libqrencode-dev  libevent-dev libminiupnpc-dev libboost-dev liblevedb-dev libboost-all-dev

  sudo apt-get install git

  cd triangles/src/leveldb
  chmod +x build_detect_platform
  make clean
  make libleveldb.a libmemenv.a

  cd triangles/src
  mkdir obj
  make -f makefile.unix



