# Generated from orogen/lib/orogen/templates/tasks/CMakeLists.txt

include(uwv_kalman_filtersTaskLib)
ADD_LIBRARY(${UWV_KALMAN_FILTERS_TASKLIB_NAME} SHARED 
    ${UWV_KALMAN_FILTERS_TASKLIB_SOURCES})
add_dependencies(${UWV_KALMAN_FILTERS_TASKLIB_NAME}
    regen-typekit)

TARGET_LINK_LIBRARIES(${UWV_KALMAN_FILTERS_TASKLIB_NAME}
    ${OrocosRTT_LIBRARIES}
    ${UWV_KALMAN_FILTERS_TASKLIB_DEPENDENT_LIBRARIES})
SET_TARGET_PROPERTIES(${UWV_KALMAN_FILTERS_TASKLIB_NAME}
    PROPERTIES LINK_INTERFACE_LIBRARIES "${UWV_KALMAN_FILTERS_TASKLIB_INTERFACE_LIBRARIES}")
SET_TARGET_PROPERTIES(${UWV_KALMAN_FILTERS_TASKLIB_NAME}
    PROPERTIES INTERFACE_LINK_LIBRARIES "${UWV_KALMAN_FILTERS_TASKLIB_INTERFACE_LIBRARIES}")

INSTALL(TARGETS ${UWV_KALMAN_FILTERS_TASKLIB_NAME}
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib/orocos)

INSTALL(FILES ${UWV_KALMAN_FILTERS_TASKLIB_HEADERS}
    DESTINATION include/orocos/uwv_kalman_filters)

