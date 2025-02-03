cmake_minimum_required(VERSION 3.16)

project(MORA-CHESS-ENGINE)

# Especificar la versión de C++
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Habilitar optimización máxima
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3")

# Agregar todos los archivos fuente
set(SOURCE_FILES
    attacks.cpp
    bitboards.cpp
    evaluation.cpp
    main.cpp
    move.cpp
    movegenerator.cpp
    pawnhashtable.cpp
    position.cpp
    search.cpp
    timemanagement.cpp
    transpositiontable.cpp
    uci.cpp
)

# Crear el ejecutable
add_executable(MORA ${SOURCE_FILES})
target_include_directories(MORA PRIVATE ${CMAKE_SOURCE_DIR}/src)
