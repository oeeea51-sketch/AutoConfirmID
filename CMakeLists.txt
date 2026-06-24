cmake_minimum_required(VERSION 3.25)

project(AutoConfirmID VERSION 1.0.0 LANGUAGES CXX)

find_package(geode REQUIRED)

add_geode_mod(
    ${PROJECT_NAME}
    ${PROJECT_VERSION}
    mod.json
)

# ИСПРАВЛЕНО: Убрали точку со слэшем, теперь робот точно найдет файл!
target_sources(${PROJECT_NAME} PRIVATE main.cpp)
