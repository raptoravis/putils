file(GLOB src *.cpp *.hpp)
add_library(mediator STATIC ${src})
target_include_directories(mediator PUBLIC .)
target_link_libraries(mediator putils)

if (UNIX)
    target_link_libraries(mediator pthread)
endif()
