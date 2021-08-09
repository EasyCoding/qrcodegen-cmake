# About

CMake build scripts for the [QR-Code-generator library](https://github.com/nayuki/QR-Code-generator).

# Build with CMake

```
git clone https://github.com/nayuki/QR-Code-generator.git qrcodegen
git clone https://github.com/xvitaly/qrcodegen-cmake.git qrcodegen-cmake
cp -f qrcodegen-cmake/CMakeLists.txt qrcodegen/
mkdir -p qrcodegen/build
cd qrcodegen/build
cmake ..
cmake --build .
```

# Install with CMake

```
cd qrcodegen/build
sudo make install
```
