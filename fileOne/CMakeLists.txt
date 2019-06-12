cmake_minimum_required (VERSION 2.6)

include_directories ("./file")#向工程添加多个特定的头文件搜索路径
add_subdirectory (file)#添加源文件.cc的目录
add_library(fileOne fileOne.cc ./file/file.cc)#生成库的名字为MathFunctions