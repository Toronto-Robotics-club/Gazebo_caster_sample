# What version of CMake is needed?
cmake_minimum_required(VERSION 2.8.3)

# The name of this package (must match name in package.xml).
project(jimmy_description)

# Find the catkin build system, and any other packages on which we depend. In
# this case we only need the roscpp library.
find_package(catkin REQUIRED COMPONENTS 
  rviz
  tf
  urdf
  xacro
  roscpp
)

# Declare our catkin package.
catkin_package()

# Specify locations of header files.
include_directories(include ${catkin_INCLUDE_DIRS})




