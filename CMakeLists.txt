cmake_minimum_required(VERSION 2.8.3)
project(robotlocomotion_lcmtypes)

find_package(catkin REQUIRED COMPONENTS lcm_catkin bot_core_lcmtypes)

catkin_package(LIBRARIES ${PROJECT_NAME} 
  CATKIN_DEPENDS lcm_catkin bot_core_lcmtypes)

include_directories(${catkin_INCLUDE_DIRS})

AddLCM(robotlocomotion_grasp_transition_state_t
    robotlocomotion_header_t
    robotlocomotion_image_array_t
    robotlocomotion_image_t
    robotlocomotion_plan_control_t
    robotlocomotion_plan_status_t
    robotlocomotion_point_t
    robotlocomotion_pose_stamped_t
    robotlocomotion_pose_t
    robotlocomotion_quaternion_t
    robotlocomotion_residual_observer_state_t
    robotlocomotion_robot_plan_t
    robotlocomotion_robot_plan_with_supports_t
    robotlocomotion_robot_plan_w_keyframes_t
    robotlocomotion_support_body_t
    robotlocomotion_support_element_t
    robotlocomotion_support_sequence_t
    robotlocomotion_viewer2_comms_t
    robotlocomotion_viewer_command_t
    robotlocomotion_viewer_draw_t
    robotlocomotion_viewer_geometry_data_t
    robotlocomotion_viewer_link_data_t
    robotlocomotion_viewer_load_robot_t)
GenerateLCM()


catkin_package(LIBRARIES ${PROJECT_NAME} 
  CATKIN_DEPENDS lcm_catkin
  INCLUDE_DIRS ${CATKIN_DEVEL_PREFIX}/include)