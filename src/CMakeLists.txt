


set(HELLO_WORLD_MPI_SRC "hello_world_mpi.c")

include_directories(${MPI_C_INCLUDE_PATH})

add_executable(hello_world_mpi ${HELLO_WORLD_MPI_SRC})

target_link_libraries(hello_world_mpi ${MPI_C_LIBRARIES})


install(TARGETS hello_world_mpi 
                RUNTIME DESTINATION ${BIN_INSTALL_DIR})
