cmake_minimum_required(VERSION 3.25)
project(ProjectC)

set(CMAKE_CXX_STANDARD 23)

add_executable(ProjectC main.cpp States/Difficulty_Computerwars_State.cpp States/Difficulty_Singleplayer_State.cpp States/Intro_State.cpp States/Menu_State.cpp States/Multiplayer_State.cpp GameGUI.cpp Player.cpp ResourceManager.cpp Board.cpp Game.cpp)
set(SFML_STATIC_LIBRARIES TRUE)
set(SFML_DIR C:/SFML/lib/cmake/SFML)
find_package(SFML COMPONENTS system window graphics audio network REQUIRED)
include_directories(C:/SFML/include)
target_link_libraries(ProjectC sfml-system sfml-window sfml-graphics sfml-audio sfml-network)