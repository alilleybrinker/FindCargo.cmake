
# `FindCargo.cmake`

This is a CMake find module designed to find `cargo`, the Rust language build tool,
and report its location, version, and channel ("stable", "nightly", "beta").

This allows projects using CMake as their build system to integrate with Cargo,
without having to write their own custom logic to identify Cargo and figure out
information about what version it is, what channel, etc.
