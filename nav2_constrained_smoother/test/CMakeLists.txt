ament_add_gtest(test_constrained_smoother
  test_constrained_smoother.cpp
)
target_link_libraries(test_constrained_smoother
  ${library_name}
  angles::angles
  ${geometry_msgs_TARGETS}
  nav2_costmap_2d::nav2_costmap_2d_client
  nav2_costmap_2d::nav2_costmap_2d_core
  nav2_util::nav2_util_core
  rclcpp::rclcpp
  tf2_ros::tf2_ros
)

ament_add_gtest(test_smoother_cost_function
  test_smoother_cost_function.cpp
)
target_link_libraries(test_smoother_cost_function
  ${library_name}
  rclcpp::rclcpp
)
