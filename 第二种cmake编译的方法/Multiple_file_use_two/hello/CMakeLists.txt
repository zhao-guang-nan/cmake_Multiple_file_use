# Add header file include directories
include_directories(./ ./helloTwo)

aux_source_directory(. DIR_HELLO_SRCS)
add_library(hello ${DIR_HELLO_SRCS} ./helloTwo/helloTwo.cpp)