# MPM - Distro-independent package management

ZYpp, dpkg, RPM, Pacman; why do we do it to ourselves? The unfortunate fact is, we have done it and there's no clear way to undo it. So, let's solve it as best we can. We create a cross-platform, cross-distro package management utility able to convert from any given package format `x` to other package format `y`.

This utility can perform searches of all supported package repositories. It can install and uninstall packages from any supported repository on any supported system. We do not propose a new package format or method of management. We simply create a bridge for existing systems. We call it the Multiversal Package Manager (MPM). It will be good.

## Design & Implementation

MPM is to be created using the [Nim](https://nim-lang.org/) programming language. Nim's cross-compiler, C/C++/Python interop, comprehensible python-like syntax, and speed-fast small native binaries make it perfect for MPM's use-case. Let's set some priorities...

### Priority 1

Existing package conversion works are to either be ported to, merged into, or added to the dependency graph of MPM. Such works include [debtap](https://github.com/helixarch/debtap) and [Alien](https://sourceforge.net/projects/alien-pkg-convert/).

### Priority 2

Packages are to be installable using MPM, if only (Where appropriate) by spawning or piping to the system's package installer.

### Priority 3

A format for specifying searchable repositories is to be implemented. All standard repository formats of supported packages will be supported by MPM. MPM is to then support the automatic download & installation of any package from any repository on any system.

## Supported Package Formats

coming soon...