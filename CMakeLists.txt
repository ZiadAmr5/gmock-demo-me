cmake_minimum_required(VERSION 3.21)
project(myProj)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


find_package(GTest REQUIRED)
add_executable(reg_test registration_service.cpp registration_service_test.cpp)
target_link_libraries(reg_test PRIVATE GTest::gmock_main)
