
# `FindCargo.cmake`

This is a CMake find module designed to find `cargo`, the Rust language build tool,
and report its location, version, and channel ("stable", "nightly", "beta").

This allows projects using CMake as their build system to integrate with Cargo,
without having to write their own custom logic to identify Cargo and figure out
information about what version it is, what channel, etc.

## Background

This find module is adapted from [one I'd contributed for the Pact project][pact],
specifically for their reference implementation in Rust. I'd worked on an effort
which added a new FFI module, exposing the core mechanisms of the reference
implementation to be called by other languages. The Cargo find module enabled
us to use CMake to build and install the artifacts produced by Cargo, and made
it easier to integrate a Rust codebase with other languages.

[pact]: https://github.com/pact-foundation/pact-reference/blob/master/rust/pact_ffi/cmake/FindCargo.cmake

