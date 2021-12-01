add_library(asio INTERFACE)
#target_compile_options(asio INTERFACE ASIO_STANDALONE)
target_include_directories(asio INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include/")
target_link_libraries(asio INTERFACE pthread)  # Using ASIO requires you link your final executable/library with your system's threading library (e.g. pthread on linux)