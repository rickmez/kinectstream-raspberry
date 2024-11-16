cmake_minimum_required(VERSION 3.5.0)
project(KinectStream VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

# Find OpenCV package
find_package(OpenCV REQUIRED)

# Include OpenCV headers
include_directories(${OpenCV_INCLUDE_DIRS})

# Add your executable or project files
add_executable(KinectStream main.cpp)  # Replace 'main.cpp' with your source files

# Link OpenCV libraries to your project
target_link_libraries(KinectStream ${OpenCV_LIBS})

set_property(TARGET KinectStream PROPERTY CXX_STANDARD 17)