#--------------------------------------------------------------------------------------------------
# Tester0: hello world
#--------------------------------------------------------------------------------------------------
add_executable(test_hello_world test_hello_world.cpp)
target_link_libraries(test_hello_world PUBLIC project_options)
add_test(Tester0 test_hello_world)