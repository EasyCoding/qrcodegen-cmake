# CMake for the QR-Code-generator

## About

CMake build scripts for the [QR-Code-generator library](https://github.com/nayuki/QR-Code-generator).

## Building with CMake

Available configuration options:

  * `BUILD_EXAMPLES` - build examples.
  * `BUILD_TESTS` - build tests.

Clone the upstream repository, create the necessary symlinks and start the build process:

```
git clone https://github.com/nayuki/QR-Code-generator.git qrcodegen
git clone https://github.com/EasyCoding/qrcodegen-cmake.git qrcodegen-cmake
ln -s ../qrcodegen-cmake/{cmake,CMakeLists.txt} qrcodegen/
mkdir -p qrcodegen-build
cmake -S qrcodegen -B qrcodegen-build -DCMAKE_BUILD_TYPE=RelWithDebInfo -DBUILD_SHARED_LIBS:BOOL=ON -DBUILD_EXAMPLES:BOOL=ON -DBUILD_TESTS:BOOL=ON
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

## Running tests

Run tests on modern CMake versions (3.20 or higher):

```
ctest --test-dir qrcodegen-build --output-on-failure
```

Run tests on older CMake versions:

```
pushd qrcodegen-build
ctest --output-on-failure
popd
```
