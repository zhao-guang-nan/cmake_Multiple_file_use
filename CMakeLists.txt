cmake_minimum_required (VERSION 2.6)#cmake的版本要求
project (Tutorial)#输出工程的名字
include_directories ("${PROJECT_SOURCE_DIR}/fileOne")#向工程添加多个特定的头文件搜索路径
add_subdirectory (fileOne)#添加源文件.cc的目录
include_directories ("${PROJECT_SOURCE_DIR}/fileTwo")#向工程添加多个特定的头文件搜索路径
add_subdirectory (fileTwo)#添加源文件.cc的目录
set (EXTRA_LIBS ${EXTRA_LIBS} fileOne fileTwo)#EXTRA_LIBS其实就是MathFunctions
 
# add the executable
add_executable(Tutorial main.cc)#可执行文件的名字 Tutorial
target_link_libraries (Tutorial  ${EXTRA_LIBS})#链接到MathFunctions目录下的库文件 
