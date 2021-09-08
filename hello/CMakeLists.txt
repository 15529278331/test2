cmake_minimum_required( VERSION 2.8 )

# Set the project name
project ( hello )

message( STATUS "CMAKE_PROJECT_NAME = ${CMAKE_PROJECT_NAME}" )
message( STATUS "PROJECT_SOURCE_DIR = ${PROJECT_SOURCE_DIR}" )


add_library(HELLO_STATIC ${HELLO_STATIC_SOURCE})
add_library(HELLO_SHARED ${HELLO_SHARED_SOURCE})

target_link_libraries(${PROJECT_NAME} HELLO_STATIC)
target_link_libraries(${PROJECT_NAME} HELLO_SHARED)



# Add an executable
add_executable(hello hello.cpp)
