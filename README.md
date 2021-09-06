rust-fftw3
===========
[![Rust](https://github.com/rust-math/fftw/workflows/Rust/badge.svg)](https://github.com/rust-math/fftw/actions)

Rust bindings for the [FFTW C library](https://www.fftw.org/) for computing discrete Fourier transforms, as well as discrete cosine and sine transforms.

This repository includes three crates:

- [![Crate](https://img.shields.io/crates/v/fftw.svg)](https://crates.io/crates/fftw)
  [![docs.rs](https://docs.rs/fftw/badge.svg)](https://docs.rs/fftw)
  `fftw`: A safe wrapper in Rust
- [![Crate](https://img.shields.io/crates/v/fftw-sys.svg)](https://crates.io/crates/fftw-sys)
  [![docs.rs](https://docs.rs/fftw-sys/badge.svg)](https://docs.rs/fftw-sys)
  `fftw-sys`: An unsafe wrapper in Rust
- [![Crate](https://img.shields.io/crates/v/fftw-src.svg)](https://crates.io/crates/fftw-src)
  [![docs.rs](https://docs.rs/fftw-src/badge.svg)](https://docs.rs/fftw-src)
  `fftw-src`: A crate for downloading and compiling the FFTW library


Feature flags
--------------

- `source`: Download and compile FFTW (default)
    - (Linux, macOS) Needs a C-compiler and the `make` build tool to compile the FFTW library
    - (Windows) Downloads a precompiled binary from the [FFTW website](https://www.fftw.org/install/windows.html)
- `system`: Use the system's libfftw3 (experimental)
    - You must install FFTW before building this crate
    - For Linux systems, please install FFTW using your package manager, e.g. in Debian or Ubuntu run `apt install libfftw3-dev`
    - For macOS, please run `brew install fftw` by using [Homebrew](https://github.com/Homebrew/brew)
    - This feature is unsupported on Windows
- `intel-mkl` Use Intel MKL backend through [intel-mkl-src](https://github.com/rust-math/intel-mkl-src)
    - Only Linux and Windows are supported

|Feature  | Linux | Windows | macOS |
|:--------|:-----:|:-------:|:-----:|
|source   |✔️     |✔️       |✔️     |
|system   |✔️     |-        |✔️     |
|intel-mkl|✔️     |✔️       |-      |

LICENSE
--------
See [LICENSE.md](./LICENSE.md)
