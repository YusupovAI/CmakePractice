# checking version
cmake_minimum_required(VERSION 3.10)

# naming preject
project(CmakeTesting LANGUAGES CXX)


execute_process(COMMAND python3 preparing.py
	WORKING_DIRECTORY A)


add_executable(main C/main.cpp)
add_subdirectory(B)
target_link_libraries(main lib_name)

 
target_include_directories(main PUBLIC .)


