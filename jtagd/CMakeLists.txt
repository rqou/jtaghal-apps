# CMake build script for jtagd.

set(JTAGD_SOURCES main.cpp ConnectionThread.cpp)

add_executable(jtagd 
	${JTAGD_SOURCES})
target_link_libraries(jtagd jtaghal)
target_include_directories(jtagd
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
install(TARGETS jtagd RUNTIME DESTINATION /usr/bin)

