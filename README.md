
# `FindCargo.cmake`

This is a CMake find module designed to find `cargo`, the Rust language build tool,
and report its location, version, and channel ("stable", "nightly", "beta").

This allows projects using CMake as their build system to integrate with Cargo,
without having to write their own custom logic to identify Cargo and figure out
information about what version it is, what channel, etc.

## Usage

You can use this find module by either 1) adding it to a location in the
`CMAKE_MODULES_PATH`, or by 2) adding its location to the `CMAKE_MODULES_PATH`.
Once it's in the modules path, simply add `find_package(Cargo)` to your
`CMakeLists.txt` file.

```cmake
# Replace <CARGO FIND MODULE PATH> with the path to this find module.
set(CMAKE_MODULE_PATH "<CARGO FIND MODULE PATH>" ${CMAKE_MODULE_PATH})
```

## Background

This find module is adapted from [one I'd contributed for the Pact project][pact],
specifically for their reference implementation in Rust. I'd worked on an effort
which added a new FFI module, exposing the core mechanisms of the reference
implementation to be called by other languages. The Cargo find module enabled
us to use CMake to build and install the artifacts produced by Cargo, and made
it easier to integrate a Rust codebase with other languages.

[pact]: https://github.com/pact-foundation/pact-reference/blob/master/rust/pact_ffi/cmake/FindCargo.cmake

