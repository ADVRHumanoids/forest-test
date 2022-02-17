cmake_minimum_required(VERSION 3.0)
project(forest_test)

option(INSTALL_B_FILE "install b_file.txt" OFF)

install(FILES a_file.txt
    DESTINATION share/${PROJECT_NAME})

if(INSTALL_B_FILE)
    install(FILES b_file.txt
        DESTINATION share/${PROJECT_NAME})
endif()

install(FILES ${PROJECT_NAME}Config.cmake
    DESTINATION lib/cmake/${PROJECT_NAME})