project(planning_main)

add_subdirectory(pnc_map)
add_subdirectory(process)
add_subdirectory(show_result)

add_executable(${PROJECT_NAME} planning_main.cpp)

target_include_directories(${PROJECT_NAME}
PUBLIC
${Proess_Dir}
)

target_include_directories(${PROJECT_NAME}
PUBLIC
${Show_Result_Dir}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
process
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
show_result
)