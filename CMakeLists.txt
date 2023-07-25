cmake_minimum_required(VERSION 3.5)

project(imgui CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "" FORCE)

set(CMAKE_C_STANDARD 17)
set(CMAKE_CXX_STANDARD 20)

add_library(${PROJECT_NAME} STATIC
	imconfig.h
	imgui.h
	imgui.cpp
	imgui_draw.cpp
	imgui_internal.h
	imgui_tables.cpp
	imgui_widgets.cpp
	imstb_rectpack.h
	imstb_textedit.h
	imstb_truetype.h
	imgui_demo.cpp
)

target_include_directories(${PROJECT_NAME}
PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)
