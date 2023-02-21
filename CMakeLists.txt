cmake_minimum_required(VERSION 3.14)

project("unqlite-playground")

set(unqlite_ROOT "P:/Downloads/cpp-libraries/unqlite-1.1.9/build/unqlite")

SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

include_directories("${unqlite_ROOT}/include")

add_executable(${PROJECT_NAME}
    "src/main.cpp"
)

target_link_libraries(${PROJECT_NAME} "${unqlite_ROOT}/lib/libunqlite.a")
