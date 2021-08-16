# CMake for the QR-Code-generator

[![GitHub version](https://img.shields.io/github/v/release/EasyCoding/qrcodegen-cmake?sort=semver&color=brightgreen&logo=git&logoColor=white)](https://github.com/EasyCoding/qrcodegen-cmake/releases)
[![GCC CI status](https://github.com/EasyCoding/qrcodegen-cmake/actions/workflows/gcc.yml/badge.svg)](https://github.com/EasyCoding/qrcodegen-cmake/actions/workflows/gcc.yml)
[![Clang CI status](https://github.com/EasyCoding/qrcodegen-cmake/actions/workflows/clang.yml/badge.svg)](https://github.com/EasyCoding/qrcodegen-cmake/actions/workflows/clang.yml)
[![GitHub issues](https://img.shields.io/github/issues/EasyCoding/qrcodegen-cmake?logo=github&logoColor=white)](https://github.com/EasyCoding/qrcodegen-cmake/issues)
[![GitHub stars](https://img.shields.io/github/stars/EasyCoding/qrcodegen-cmake?logo=github&logoColor=white)](https://github.com/EasyCoding/qrcodegen-cmake/stargazers)
[![License](https://img.shields.io/github/license/EasyCoding/qrcodegen-cmake?logo=files&logoColor=white)](LICENSE)
---

## About

CMake build scripts for the [QR-Code-generator library](https://github.com/nayuki/QR-Code-generator).

## Build with CMake

```
git clone https://github.com/nayuki/QR-Code-generator.git qrcodegen
git clone https://github.com/EasyCoding/qrcodegen-cmake.git qrcodegen-cmake
ln -s ../qrcodegen-cmake/CMakeLists.txt qrcodegen/
mkdir -p qrcodegen/build
cd qrcodegen/build
cmake ..
cmake --build .
```

## Install with CMake

```
cd qrcodegen/build
sudo cmake --install .
```
