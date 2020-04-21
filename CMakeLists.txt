cmake_minimum_required(VERSION 3.5)
project(duckietown_msgs)

# Default to C99
if(NOT CMAKE_C_STANDARD)
  set(CMAKE_C_STANDARD 99)
endif()

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(rosidl_default_generators REQUIRED)
find_package(ament_cmake REQUIRED)
find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(visualization_msgs REQUIRED)
find_package(sensor_msgs REQUIRED)

## Generate messages and services
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/CarControl.msg"
  "msg/CoordinationSignal.msg"
  "msg/CoordinationSignalETHZ17.msg"
  "msg/DuckieSensor.msg"
  "msg/LanePose.msg"

  "msg/IntersectionPose.msg"
  "msg/IntersectionPoseImg.msg"
  "msg/IntersectionPoseImgDebug.msg"

  "msg/TurnIDandType.msg"
# "msg/LEDControl.msg"
  "msg/LEDDetection.msg"
  "msg/MaintenanceState.msg"
  "msg/LEDDetectionArray.msg"
  "msg/LEDDetectionDebugInfo.msg"
  "msg/WheelsCmd.msg"
  "msg/WheelsCmdStamped.msg"
  "msg/Pose2DStamped.msg"
  "msg/SignalsDetection.msg"
  "msg/SignalsDetectionETHZ17.msg"
  "msg/Twist2DStamped.msg"
  "msg/Twist2DStampedETHZ17.msg"
  "msg/AprilTagDetection.msg"
  "msg/AprilTagDetectionArray.msg"
  "msg/AprilTagsWithInfos.msg"
  "msg/TagInfo.msg"
  "msg/Pixel.msg"
  "msg/Vector2D.msg"
  "msg/Segment.msg"
  "msg/SegmentList.msg"
  "msg/Rect.msg"
  "msg/Rects.msg"
  "msg/SceneSegments.msg"
  "msg/SourceTargetNodes.msg"
  "msg/CoordinationClearance.msg"
  "msg/CoordinationClearanceETHZ17.msg"
# "msg/IntersectionDetection.msg"
# "msg/CoordinationSignal.msg"
# "msg/TrafficLightDetection.msg"
  "msg/VehicleCorners.msg"
  "msg/VehiclePose.msg"
# "msg/VehicleDetection.msg"
  "msg/FSMState.msg"
  "msg/BoolStamped.msg"
  "msg/BoolStampedETHZ17.msg"
  "msg/StopLineReading.msg"
  "msg/LEDInterpreter.msg"
  "msg/AntiInstagramHealth.msg"
  "msg/AntiInstagramTransform.msg"
  "msg/AntiInstagramTransformCB.msg"
  "msg/KinematicsWeights.msg"
  "msg/KinematicsParameters.msg"
  "msg/ThetaDotSample.msg"
  "msg/Vsample.msg"
  "msg/Trajectory.msg"
  "msg/ObstacleType.msg"
  "msg/ObstacleImageDetection.msg"
  "msg/ObstacleImageDetectionList.msg"
  "msg/ObstacleProjectedDetection.msg"
  "msg/ObstacleProjectedDetectionList.msg"

  "msg/Num.msg"

  "srv/SetFSMState.srv"
  "srv/SetValue.srv"
  "srv/SetVariable.srv"
  "srv/GetVariable.srv"
#  "srv/Service2.srv"
  DEPENDENCIES builtin_interfaces std_msgs geometry_msgs visualization_msgs sensor_msgs
)

ament_package()
