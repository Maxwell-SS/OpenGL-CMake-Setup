cmake_minimum_required(VERSION 3.2)
project(json)

add_library(json STATIC
	src/json.cpp
	include/json.hpp)