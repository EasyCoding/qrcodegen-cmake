#
# SPDX-FileCopyrightText: 2021 EasyCoding Team and contributors
#
# SPDX-License-Identifier: MIT
#

cmake_minimum_required(VERSION 3.12)

project(QR-Code-generator
    VERSION 1.7.0
    DESCRIPTION "High-quality QR Code generator library in Java, TypeScript/JavaScript, Python, C++, C, Rust"
    HOMEPAGE_URL "https://www.nayuki.io/page/qr-code-generator-library"
    LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# =======================
# === Paths detection ===
# =======================

include(GNUInstallDirs)

# ========================
# === C library target ===
# ========================

set(QRCODEGEN_SOURCES
    c/qrcodegen.c
)

set(QRCODEGEN_HEADERS
    c/qrcodegen.h
)

add_library(qrcodegen
    ${QRCODEGEN_SOURCES}
    ${QRCODEGEN_HEADERS}
)

target_include_directories(qrcodegen PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/c>
    $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}/qrcodegen>
)

set_property(TARGET qrcodegen PROPERTY PUBLIC_HEADER ${QRCODEGEN_HEADERS})
set_property(TARGET qrcodegen PROPERTY VERSION ${CMAKE_PROJECT_VERSION})
set_property(TARGET qrcodegen PROPERTY SOVERSION 1)

install(TARGETS qrcodegen
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
    BUNDLE DESTINATION ${CMAKE_INSTALL_BINDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/qrcodegen
)

# ==========================
# === C++ library target ===
# ==========================

set(QRCODEGENCPP_SOURCES
    cpp/qrcodegen.cpp
)

set(QRCODEGENCPP_HEADERS
    cpp/qrcodegen.hpp
)

add_library(qrcodegencpp
    ${QRCODEGENCPP_SOURCES}
    ${QRCODEGENCPP_HEADERS}
)

target_include_directories(qrcodegencpp PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/cpp>
    $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}/qrcodegencpp>
)

set_property(TARGET qrcodegencpp PROPERTY PUBLIC_HEADER ${QRCODEGENCPP_HEADERS})
set_property(TARGET qrcodegencpp PROPERTY VERSION ${CMAKE_PROJECT_VERSION})
set_property(TARGET qrcodegencpp PROPERTY SOVERSION 1)

install(TARGETS qrcodegencpp
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
    BUNDLE DESTINATION ${CMAKE_INSTALL_BINDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/qrcodegencpp
)
