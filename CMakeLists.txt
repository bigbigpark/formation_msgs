cmake_minimum_required(VERSION 3.0.2)
project(formation_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  std_msgs
  geometry_msgs
)

add_message_files(
  FILES
  RefPath.msg
  FormationCmdVelArr.msg
  FormationCollision.msg
  ObstacleType.msg
  ObstacleArr.msg
  FormationPositionArr.msg
  FutureStateType.msg
  FutureStateArr.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS message_generation message_runtime std_msgs geometry_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
