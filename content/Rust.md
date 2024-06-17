Any function whose name ends with a ! is a macro. Macros and functions are different in how they operate. For example
```rust
println!() //this is a macro
println()  //this is a function
```

Rust macros are executed at compile-time and are hygienic in compilation and execution

If you see a *.pdb* filename extension, that is a debugging information file

Crates are packages of codes. I think of them as libraries that go under the `[dependencies]` section in *cargo.toml*

Source code files go into the *src* subdirectory. Everything else goes into the parent directory
When building a cargo directory, the executable file will be found in the default debug build folder (*/target/debug/*)

>[!Note]
>When executing a .exe file in PowerShell, type `./exe_name`

When accessing invalid or non-extant elements of an array, Rust will not execute the code and spit garbage values; it will stop compiling and will throw an error. This is a key part of Rust's memory safety principles