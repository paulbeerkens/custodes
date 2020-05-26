
set (HEADER_FILES
        ClientService.h
        )

set(SOURCE_FILES
        ClientService.cpp
        )

add_library(ClientService STATIC ${SOURCE_FILES} ${HEADER_FILES})

target_include_directories(ClientService INTERFACE ../.) #Allow this library to be included using it's directory name

target_link_libraries(ClientService libWebServer libLog)

target_link_libraries(ClientService project_warnings)
