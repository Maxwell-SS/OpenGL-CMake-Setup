cmake_minimum_required(VERSION 3.2)
set(CMAKE_CXX_STANDARD 20)
project(OpenGLSetup)

include_directories(
	${PROJECT_SOURCE_DIR}/src
	${PROJECT_SOURCE_DIR}/libs/glad/include
	${PROJECT_SOURCE_DIR}/libs/glfw/include
	${PROJECT_SOURCE_DIR}/libs/glm/include
	${PROJECT_SOURCE_DIR}/libs/imgui/include
	${PROJECT_SOURCE_DIR}/libs/json/include
	${PROJECT_SOURCE_DIR}/libs/stb/include)

# making main executable
add_executable(${PROJECT_NAME} src/main.cpp)

# glad
add_subdirectory(libs/glad EXCLUDE_FROM_ALL)
target_link_libraries(${PROJECT_NAME} PRIVATE glad)

# glad
add_subdirectory(libs/glfw EXCLUDE_FROM_ALL)
target_link_libraries(${PROJECT_NAME} PRIVATE glfw)

# glm
add_subdirectory(libs/glm EXCLUDE_FROM_ALL)
target_link_libraries(${PROJECT_NAME} PRIVATE glm)

# imgui
add_subdirectory(libs/imgui EXCLUDE_FROM_ALL)
target_link_libraries(${PROJECT_NAME} PRIVATE imgui)

# json
add_subdirectory(libs/json EXCLUDE_FROM_ALL)
target_link_libraries(${PROJECT_NAME} PRIVATE json)

# stb
add_subdirectory(libs/stb EXCLUDE_FROM_ALL)
target_link_libraries(${PROJECT_NAME} PRIVATE stb)