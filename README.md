# CMake for the QR-Code-generator

[![GitHub version](https://img.shields.io/github/v/release/EasyCoding/qrcodegen-cmake?sort=semver&color=brightgreen&logo=git&logoColor=white)](https://github.com/EasyCoding/qrcodegen-cmake/releases)
[![Linux CI status](https://github.com/EasyCoding/qrcodegen-cmake/actions/workflows/linux.yml/badge.svg)](https://github.com/EasyCoding/qrcodegen-cmake/actions/workflows/linux.yml)
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
ln -s ../qrcodegen-cmake/{cmake,CMakeLists.txt} qrcodegen/
mkdir -p qrcodegen-build
cmake -S qrcodegen -B qrcodegen-build -DCMAKE_BUILD_TYPE=RelWithDebInfo -DBUILD_SHARED_LIBS:BOOL=ON -DBUILD_EXAMPLES:BOOL=ON -DBUILD_TESTS:BOOL=ON
cmake --build qrcodegen-build
```

## Install with CMake

```
sudo cmake --install qrcodegen-build
```

Install only one library flavor (either C or C++ respectively):
```
sudo cmake --install qrcodegen-build --component {qrcodegen|qrcodegencpp}
```
