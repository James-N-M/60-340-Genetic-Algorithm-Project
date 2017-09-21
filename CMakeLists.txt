cmake_minimum_required(VERSION 3.6)
project(cs340proj)

set(CMAKE_CXX_STANDARD 14)

set(BOOST_ROOT "C:/boost_1_63_0/")

find_package(Boost 1.63.0)

if(NOT Boost_FOUND)
    message(FATAL_ERROR "Could not find boost!")
endif()

if(Boost_FOUND)
    message(STATUS "It works!")
    include_directories(${Boost_INCLUDE_DIRS})
endif()

set(SOURCE_FILES
        ga.cxx
        ga.hxx
        main.cxx
        program_options.hxx
        types.cxx
        types.hxx)

add_executable(cs340proj ${SOURCE_FILES})