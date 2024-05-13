cmake_minimum_required(VERSION 3.25)
project(SmallWheel VERSION 0.1.0 LANGUAGES C CXX)
set(CMAKE_CXX_STANDARD 17)

set(CMAKE_EXPORT_COMPILE_COMMANDS True)
file(GLOB IMGUI_SOURCE 
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_demo.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_draw.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_tables.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_widgets.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui.cpp
    )
set(IMGUI_INCLUDES ${CMAKE_CURRENT_SOURCE_DIR}/src/)

add_library(imgui STATIC ${IMGUI_SOURCE})
target_include_directories(imgui PRIVATE ${IMGUI_INCLUDES})
