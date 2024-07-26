cmake_minimum_required(VERSION 3.8)
project(tbot_nav2)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)

install(DIRECTORY launch/
  DESTINATION share/${PROJECT_NAME}/launch
)

# Install the param files
install(DIRECTORY param/
  DESTINATION share/${PROJECT_NAME}/param
)

# Install the map files
install(DIRECTORY map/
  DESTINATION share/${PROJECT_NAME}/map
)

ament_package()
