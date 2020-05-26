cmake_minimum_required(VERSION 3.8)

set(HEADER_FILES
        )

set(SOURCE_FILES

        Main.cpp)

add_executable(Custodes ${SOURCE_FILES} ${HEADER_FILES})

#external libraries
target_link_libraries(Custodes libWebServer libLog)

#set_project_warnings(Custodes)

#internal libraries
target_link_libraries(Custodes project_warnings)
target_link_libraries(Custodes ClientService)
