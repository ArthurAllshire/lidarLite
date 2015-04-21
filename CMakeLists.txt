cmake_minimum_required (VERSION 2.6)
#project (lidarTest) #uncomment to compile test
project (broadcastLidar) #uncommnet to compile broadcast
include_directories(include)
#add_executable(lidarTest src/lidarTest.c src/lidarLite.c include/lidarLite.h)  #uncomment to compile test
add_executable(broadcastLidar src/broadcastLidar.c src/lidarLite.c include/lidarLite.h src/udp.c include/udp.h)
#target_link_libraries (lidarTest wiringPi wiringPiDev pthread) #uncomment to compile test
target_link_libraries (broadcastLidar wiringPi wiringPiDev pthread)
