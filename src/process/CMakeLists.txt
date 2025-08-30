project(process) #项目名称

add_library(${PROJECT_NAME} # 添加库
SHARED # 共享库
process.cpp # 源文件
)



target_include_directories(${PROJECT_NAME} # 添加头文件搜索路径
PUBLIC # 头文件目录
${PNC_Map_Dir} # pnc_map目录
)

target_link_libraries(${PROJECT_NAME} # 链接库
PUBLIC # 库目录
pnc_map # pnc_map库
)