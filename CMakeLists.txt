cmake_minimum_required(VERSION 3.29.0) # 设置 CMake 的最低版本要求

project(planning # 项目名称
    VERSION 0.0.1 # 版本号
    DESCRIPTION "a demo of cmake planning" # 项目描述
    HOMEPAGE_URL "https://github.com/yhr123del/cmake_planning_demo" # 项目主页
    LANGUAGES CXX # 使用的编程语言
)

set(CMAKE_CXX_STANDARD 17) # 设置 C++ 标准为 C++17

#变量和目录设置
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) # 可执行文件输出目录
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process) # process目录
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map) # pnc_map目录

#添加子目录
add_subdirectory(src) #将 上一行的变量传递给子目录，子目录也可以使用这些变量。