cmake_minimum_required(VERSION 3.0)
project(forest_test_with_dep)

find_package(forest_test REQUIRED)

install(FILES a_file.txt
    DESTINATION share/${PROJECT_NAME})

install(FILES ${PROJECT_NAME}Config.cmake
    DESTINATION lib/cmake/${PROJECT_NAME})