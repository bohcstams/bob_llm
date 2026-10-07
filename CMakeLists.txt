cmake_minimum_required(VERSION 3.8)
project(bob_llm)
find_package(ament_cmake REQUIRED)
find_package(ament_cmake_python REQUIRED)
find_package(std_msgs REQUIRED)

install(DIRECTORY config DESTINATION share/${PROJECT_NAME})
ament_python_install_package(${PROJECT_NAME})
install(PROGRAMS bob_llm/llm_node.py
  DESTINATION lib/${PROJECT_NAME}
  RENAME llm
)
ament_package()
