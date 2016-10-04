cmake_minimum_required(VERSION 3.3)

project(boost_range)

add_library(boost_range INTERFACE)

target_include_directories(boost_range BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_range DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::range ALIAS boost_range)
