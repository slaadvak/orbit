# Copyright (c) 2020 The Orbit Authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.

project(OrbitCaptureGgpClient)

add_executable(OrbitCaptureGgpClient main.cpp)

target_compile_options(OrbitCaptureGgpClient PRIVATE 
        ${STRICT_COMPILE_FLAGS})

target_include_directories(OrbitCaptureGgpClient PUBLIC 
        ${CMAKE_CURRENT_LIST_DIR}/include)

target_include_directories(OrbitCaptureGgpClient PRIVATE 
        ${CMAKE_CURRENT_LIST_DIR})

target_sources(OrbitCaptureGgpClient PUBLIC
        include/OrbitCaptureGgpClient/OrbitCaptureGgpClient.h)

target_sources(OrbitCaptureGgpClient PRIVATE
        main.cpp
        OrbitCaptureGgpClient.cpp)

target_link_libraries(OrbitCaptureGgpClient PUBLIC 
        OrbitBase
        OrbitProtos)

