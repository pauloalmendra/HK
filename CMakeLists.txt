cmake_minimum_required(VERSION 2.6.4)
project(CFS_HK C)

include_directories(fsw/public_inc)
include_directories(fsw/mission_inc)
include_directories(fsw/platform_inc)
include_directories(fsw/src)

aux_source_directory(fsw/src APP_SRC_FILES)
aux_source_directory(fsw/tables APP_TABLE_FILES)

# Create the app module
add_cfe_app(hk ${APP_SRC_FILES})
add_cfe_tables(hk ${APP_TABLE_FILES})
