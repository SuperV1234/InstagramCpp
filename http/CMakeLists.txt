cmake_minimum_required(VERSION 2.8.8)

include_directories(
	inc
	${PROJECT_SOURCE_DIR}/sockets/inc
	${OPENSSL_INCLUDE_DIR}
)

add_subdirectory(src)
