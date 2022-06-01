cmake_minimum_required (VERSION 3.8)
cmake_policy(SET CMP0079 NEW)

project ("MyAABBLib")

add_subdirectory("MyAABBLib")

set(SFML_STATIC_STD_LIB TRUE)
set(BUILD_SHARED_LIBS OFF)

add_subdirectory(Vendor/SFML)

target_link_libraries(${PROJECT_NAME} PRIVATE sfml-graphics sfml-audio)