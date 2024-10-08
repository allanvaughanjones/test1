cmake_minimum_required(VERSION 2.8)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS -pthread)
project(test1)
find_package(fmt)
find_package(nlohmann_json 3.2.0 REQUIRED)

add_executable(${PROJECT_NAME}
	"main.cpp")

target_link_libraries(${PROJECT_NAME}
	nlohmann_json::nlohmann_json
	fmt
	stdc++fs
	)

