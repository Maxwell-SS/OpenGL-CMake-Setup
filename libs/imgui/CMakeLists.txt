cmake_minimum_required(VERSION 3.2)
project(imgui)

add_library(imgui STATIC
	src/imgui.cpp
	src/imgui_demo.cpp
	src/imgui_draw.cpp
	src/imgui_tables.cpp
	src/imgui_widgets.cpp
	src/imgui_impl_glfw.cpp
	src/imgui_impl_opengl3.cpp
	include/imgui.h
	include/imconfig.h
	include/imgui_internal.h
	include/imstb_rectpack.h
	include/imstb_textedit.h
	include/imstb_truetype.h
	include/imgui_impl_glfw.h
	include/imgui_impl_opengl3.h)