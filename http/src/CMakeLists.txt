cmake_minimum_required(VERSION 2.8.8)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC")

set(HTTP_SOURCES
FormData.cpp
Http.cpp
HttpClient.cpp
HttpHeaderParser.cpp
HttpHeader.cpp
HttpRequest.cpp
HttpResponse.cpp
HttpUrl.cpp
)

add_library(httpcpp SHARED ${HTTP_SOURCES}
    $<TARGET_OBJECTS:sockets>
)

target_link_libraries(httpcpp ssl crypto)
