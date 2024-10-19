cmake_minimum_required(VERSION 3.6)
project(learn-curl VERSION 0.1.0)

# Add curl static library from source
option(BUILD_CURL_EXE "" OFF)
option(BUILD_SHARED_LIBS "" OFF)
option(BUILD_STATIC_LIBS "" ON)
option(CURL_DISABLE_INSTALL "" ON)
option(BUILD_LIBCURL_DOCS "" OFF)
option(BUILD_MISC_DOCS "" OFF)
option(ENABLE_CURL_MANUAL "" OFF)
option(BUILD_EXAMPLES "" OFF)
option(BUILD_TESTING "" OFF)

if(WIN32)
    option(CURL_USE_SCHANNEL "" ON)
    option(CURL_USE_LIBPSL "" OFF)
    option(USE_WIN32_IDN "" ON)
endif()

if(APPLE)
    option(USE_APPLE_IDN "" ON)
endif()

add_subdirectory(thirdparty/curl)

add_subdirectory(examples)
