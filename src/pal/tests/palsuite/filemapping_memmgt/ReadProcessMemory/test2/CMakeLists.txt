cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(TESTSOURCES
  test2.cpp
)

add_executable(paltest_readprocessmemory_test2
  ${TESTSOURCES}
)

add_dependencies(paltest_readprocessmemory_test2 coreclrpal)

target_link_libraries(paltest_readprocessmemory_test2
  pthread
  m
  coreclrpal
)


set(HELPERSOURCES
  helper.cpp
)

add_executable(paltest_readprocessmemory_test2_helper
  ${HELPERSOURCES}
)

add_dependencies(paltest_readprocessmemory_test2_helper coreclrpal)

target_link_libraries(paltest_readprocessmemory_test2_helper
  pthread
  m
  coreclrpal
)
