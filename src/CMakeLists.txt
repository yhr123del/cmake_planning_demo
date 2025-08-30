project(planning_main) #项目名称

add_subdirectory(pnc_map) #添加子目录pnc_map
add_subdirectory(process) #添加子目录process

add_executable(${PROJECT_NAME} planning_main.cpp) #添加可执行文件
# 在 add_executable 之后添加：
target_link_options(${PROJECT_NAME} PRIVATE -Wl,--subsystem=console) # 设置子系统为控制台


target_include_directories(${PROJECT_NAME} # 添加头文件搜索路径
PUBLIC # 头文件目录
${Process_Dir} # process目录
)

target_link_libraries(${PROJECT_NAME} # 链接库
PUBLIC # 库目录
process # process库
) 