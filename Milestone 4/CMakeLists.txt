cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 14)
project(MicroM4)
set(CMAKE_CXX_STANDARD 14)
find_package(MPI)
SET("OpenCV_DIR" "/usr/share/OpenCV")
find_package( OpenCV REQUIRED )
include_directories(SYSTEM ${MPI_INCLUDE_PATH})
MESSAGE(STATUS "Include dirs ${OpenCV_INCLUDE_DIRS}")
MESSAGE(STATUS "LINK LIBRARIES ${OpenCV_LIBS}")
add_executable(MicroM4 MicroM4.cpp)
target_link_libraries(MicroM4 ${MPI_C_LIBRARIES})
target_link_libraries(MicroM4 ${OpenCV_LIBS})
