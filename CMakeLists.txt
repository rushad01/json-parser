cmake_minimum_required(VERSION 3.5.0)
project(json-parser VERSION 0.1.0 LANGUAGES C CXX)

file(GLOB JSON_PARSER_SRC CONFIGURE_DEPENDS "src/*.h" "src/*.cpp")

add_executable(json-parser ${JSON_PARSER_SRC})

include(CTest)
enable_testing()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
