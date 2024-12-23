cmake_minimum_required(VERSION 3.20) #设置cmake最低版本

# 设置项目名称 版本 语言
project(yuri VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11) # 设置c++ 最低版本
set(CMAKE_CXX_STANDARD_REQUIRED ON) # 要求使用指定版本号
set(CMAKE_EXPORT_COMPILE_COMMANDS ON) # 开启生成 compile_commands.json


# 全局包含头文件
INCLUDE_DIRECTORIES(
    ${PROJECT_SOURCE_DIR}
)

find_package(Threads REQUIRED)

# 设置可执行文件名
add_executable(server server_main.cpp server.cpp)
add_executable(client client.cpp peers.cpp)