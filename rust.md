```
Welcome to Rust!

This will download and install the official compiler for the Rust
programming language, and its package manager, Cargo.

Rustup metadata and toolchains will be installed into the Rustup
home directory, located at:

   C:\Users\LMMQXYX\.rustup </u>

This can be modified with the RUSTUP_HOME environment variable.

The Cargo home directory located at:

  C:\Users\LMMQXYX\.cargo

This can be modified with the CARGO_HOME environment variable.

The cargo, rustc, rustup and other commands will be added to
Cargo's bin directory, located at:

  C:\Users\LMMQXYX\.cargo\bin

This path will then be added to your PATH environment variable by
modifying the HKEY_CURRENT_USER/Environment/PATH registry key.

You can uninstall at any time with rustup self uninstall and
these changes will be reverted.

Current installation options:


   default host triple: x86_64-pc-windows-msvc
     default toolchain: stable (default)
               profile: default
  modify PATH variable: yes

1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
>
```

# if the download speed is too low, then try the following way. remember to execute the rustup-init.exe in the later command line.If your computer system is linux, then change the .sh file.
``` $ENV:RUSTUP_DIST_SERVER='https://mirrors.ustc.edu.cn/rust-static' ```
``` $ENV:RUSTUP_UPDATE_ROOT='https://mirrors.ustc.edu.cn/rust-static/rustup' ```