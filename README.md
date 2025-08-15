# CMake for the QR-Code-generator

## About

CMake build scripts for the [QR-Code-generator library](https://github.com/nayuki/QR-Code-generator).

## CMake configuration options

This project supports the following build-time configuration options, which can be enabled or disabled using `-DOPTION_NAME=ON/OFF`:

| Name | Description | Default |
| ------- | ------- | ------- |
| QRCODEGEN_BUILD_EXAMPLES | Build examples and demos. | OFF |
| QRCODEGEN_BUILD_TESTS | Build and run unit tests. | OFF |

## Building with CMake

Clone the upstream repository, create the necessary symlinks and start the build process:

```
git clone https://github.com/nayuki/QR-Code-generator.git qrcodegen
git clone https://github.com/EasyCoding/qrcodegen-cmake.git qrcodegen-cmake
ln -s ../qrcodegen-cmake/{cmake,CMakeLists.txt} qrcodegen/
mkdir -p qrcodegen-build
cmake -S qrcodegen -B qrcodegen-build -DCMAKE_BUILD_TYPE=RelWithDebInfo -DBUILD_SHARED_LIBS:BOOL=ON -DQRCODEGEN_BUILD_EXAMPLES:BOOL=ON -DQRCODEGEN_BUILD_TESTS:BOOL=ON
cmake --build qrcodegen-build
```

## Installing with CMake

Install the entire library:

```
sudo cmake --install qrcodegen-build
```

Install only one library flavor (either C or C++ respectively):
```
sudo cmake --install qrcodegen-build --component {qrcodegen|qrcodegencpp}
```

## Running tests with CTest

Run unit tests:

```
ctest --test-dir qrcodegen-build --output-on-failure
```
