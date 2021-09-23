cmake_minimum_required(VERSION 3.2)
project(glad)

add_library(glad STATIC
	src/glad.c
	include/glad/glad.h
	include/KHR/khrplatform.h)
