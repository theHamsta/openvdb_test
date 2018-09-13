project( openvdb_test )
cmake_minimum_required( VERSION 3.5 )

set (CMAKE_CXX_STANDARD 14)

aux_source_directory(source SOURCES)
include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/include/
	)

add_executable( openvdb_test main.cpp  )

target_link_libraries( openvdb_test PUBLIC 
							tbb
							openvdb
							Half                                                                      
							IexMath                                                                  
							Iex                                                                             
							IlmThread                                                               
							Imath
							)
