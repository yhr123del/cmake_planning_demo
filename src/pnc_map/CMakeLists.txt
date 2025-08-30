project(pnc_map) # 项目名称

add_library(${PROJECT_NAME} # 添加库
SHARED # 共享库
pnc_map.cpp # 源文件
)