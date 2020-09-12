cmake_minimum_required (VERSION 3.5)

project(cppcheck_analysis)

# Use debug build as recommended
set(CMAKE_BUILD_TYPE Debug)

# Have cmake create a compile database
# 以下のオプションを有効ににしてcmakeを実行すると、コンパイルのためのコマンドラインが compile_commands.json ファイルとしてJSON形式でエクスポートされます。
# See: https://mjt.hatenadiary.com/entry/20120819/p1
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Add sub directories
add_subdirectory(subproject1)
add_subdirectory(subproject2)
