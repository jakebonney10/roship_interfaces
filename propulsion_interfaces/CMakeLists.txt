cmake_minimum_required(VERSION 3.8)

project(propulsion_interfaces)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

set(MSG_FILES
    "msg/Thrust.msg"
    "msg/ThrustArray.msg"
    "msg/ThrustStamped.msg")

rosidl_generate_interfaces(${PROJECT_NAME}
    ${MSG_FILES}
    DEPENDENCIES
    std_msgs)

ament_export_dependencies(rosidl_default_runtime)

ament_package()
