cmake_minimum_required(VERSION 3.12)
project(WxApp LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 1. Find the wxWidgets package and specify required components
find_package(wxWidgets REQUIRED COMPONENTS core base)

# 2. Include the wxWidgets use file (sets up include paths and macros)
include(${wxWidgets_USE_FILE})

# 3. Define your executable target
add_executable(Render src/main.cpp)

# 4. Link the wxWidgets libraries to your executable
target_link_libraries(Render PRIVATE ${wxWidgets_LIBRARIES})