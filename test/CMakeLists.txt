#-----------------------------------------------------------------------------
# Test
#-----------------------------------------------------------------------------
add_compile_options(-Wall)
add_executable(test_one
    test_one.cpp)
target_link_libraries(test_one
    pumlg_compiler
    gtest_main
    gtest)
add_test(test_one test_one)

add_test(cli_help ${CMAKE_BINARY_DIR}/apps/pumlg/pumlg -h)
add_test(cli_compile ${CMAKE_BINARY_DIR}/apps/pumlg/pumlg ${CMAKE_CURRENT_SOURCE_DIR}/models/Modelica.puml)

# vim: set et fenc=utf-8 ff=unix ft=cmake sts=0 sw=4 ts=4 :
