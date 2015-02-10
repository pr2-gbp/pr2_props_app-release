cmake_minimum_required(VERSION 2.8.3)
project(pr2_props_app)
find_package(catkin REQUIRED COMPONENTS roslib rospy  pr2_position_scripts std_srvs)

catkin_package(
    DEPENDS roslib rospy pr2_props pr2_position_scripts std_srvs
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(FILES pr2_props.app pr2props.jpg pr2_props.interface pr2props_repeat.jpg pr2_repeat_props_high.app pr2_repeat_props.interface pr2_repeat_props_low.app DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

install(DIRECTORY launch/ DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

install(PROGRAMS scripts/prop_repeat scripts/prop_runner DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
