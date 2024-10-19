macro(add_example _example_name)
    add_executable(${_example_name} ${_example_name}.c)
    target_link_libraries(${_example_name} PRIVATE libcurl_static)
endmacro()

add_example(url2file)
