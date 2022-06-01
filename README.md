# OVERVIEW OF LNGCNV

[coprosize](https://github.com/piotrbajdek/coprosize) employs power and cubic regression models allowing to estimate the producer's body mass based on coprolite diameter. Models can be chosen accordingly to the supposed producer's taxon (at this stage of program development, only tetrapod models are implemented) and its diet type (carnivorous, herbivorous, omnivorous, unspecified). Implemented regression formulae are provided in [Supplement 1. Regression models](https://github.com/piotrbajdek/coprosize/blob/main/docs/supplement-1.ods) and constructed based on the data given in [Supplement 2. Scat diameters and body masses](https://github.com/piotrbajdek/coprosize/blob/main/docs/supplement-2.ods).

As it is aimed for science, [coprosize](https://github.com/piotrbajdek/coprosize) is written in Rust. The reasons for this choice are (1) the high code correctness guaranteed by Rust, (2) to ensure that each program version will be hosted 'for perpetuity' in the [registry](https://docs.rs/crate/coprosize/latest) and (3) that each program version will remain easily installable and cross-platform 'for perpetuity', thanks to the Rust's strict policy of backward compatibility.

**As of v1.0.0-alpha.1, coprosize remains in an unstable fast-development phase. This program version is not intended for scientific research but for presentation of the technology and testing!**

# SCREENSHOTS

[Static links to changeable images of the _most recent_ version of coprosize! This may include pre-releases!]

![help-image](https://github.com/piotrbajdek/coprosize/blob/main/docs/images/help-image.png?raw=true)

![example-image-1](https://github.com/piotrbajdek/coprosize/blob/main/docs/images/example-image-1.png?raw=true)

# CITATION AND REUSE

Please, always refer to a specific program version--implemented formulae are subject to change if new data are available (or simply studied by the author) or bugs of any kind are detected. Although coprosize is designed with the needs of a user in mind, you are perfectly OK to reuse my models in your study without really installing coprosize as long as you cite this computer program as the original source. You are also OK to modify and fork coprosize under terms of the [MIT license](https://github.com/piotrbajdek/coprosize/blob/main/LICENSE).

Bajdek, P., 2022. coprosize (version 1.0.0-alpha.1). [computer software] https://github.com/piotrbajdek/coprosize

# INSTALLATION ON LINUX

[coprosize](https://github.com/piotrbajdek/coprosize) should run smoothly on Windows and macOS. Yet, it is being developed and tested on Fedora Linux.

## METHOD 1

**1.** Install from crates.io by the use of cargo:

_cargo install coprosize \--version 1.0.0-alpha.1_

By default, the file will be downloaded to .cargo/bin/, a hidden folder in your home directory.

**2a.** For convenience, you will probably want to copy lngcnv to /usr/bin/ as in Method 2 (3a, 3b).

**2b.** Alternatively, add ~/.cargo/bin directory to your PATH variable (see documentation of your shell).

## METHOD 2

**1.** Download the binary 'coprosize' for Linux x86_64 from GitHub:

https://github.com/piotrbajdek/coprosize/releases/tag/v1.0.0-alpha.1

**2.** Make the file executable:

_sudo chmod +x ./coprosize_

**3a.** Install coprosize via copying the binary to /usr/bin/

_sudo cp coprosize /usr/bin/_

**3b.** On Fedora Silverblue / Kinoite:

_sudo cp coprosize /var/usrlocal/bin/_

## METHOD 3

Download the coprosize source from GitHub. Then, build and install the program:

https://github.com/piotrbajdek/coprosize/releases/tag/v1.0.0-alpha.1

_cargo build && sudo cp target/debug/coprosize /usr/bin/_

# COPROSIZE CRATE ON CRATES.IO

The Rust community’s crate registry

https://crates.io/crates/coprosize