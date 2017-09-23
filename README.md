# Semi-official ABBS tree for extra Linux Kernel variants

This repository contains kernel configuration for Linux Kernel with extra
functionalities (e.g. enhancements, aggressive improvements, special flavor).

NOTE: No binary is provided. You will need to read our semi-comprehensive guide
on how to build packages from an ABBS tree [here](https://github.com/AOSC-Dev/aosc-os-abbs/wiki).

More to come in the future. If you would like more, you are welcomed to create a
PR to us (but please first read our [contribution guidelines]()).

## Kernel variants

### `featured-kernel`

This class of packages provides Linux Kernel with special features that are not
present in vanilla Kernel code, such as Con Kolivas' Kernel Patch Set
(`linux-ck`), PaX/Grsecurity kernel security enhancement (`linux-grsec`), etc.
Features in the [AOSC mainline kernel](https://github.com/AOSC-Dev/aosc-os-abbs/tree/staging/extra-kernel/linux-kernel)
will be all retained.

These kernels should work on all architectures. However, some kernels might be
somewhat platform-specific. If you are not sure, please first check upstreams of
these kernel improvements.

### `machine-kernel`

This class of packages provides Linux Kernel with machine-specific
optimizations, while retaining all the features that a mainline
[AOSC kernel](https://github.com/AOSC-Dev/aosc-os-abbs/tree/staging/extra-kernel/linux-kernel)
provides. For instance, `linux-kernel-broadwell` is a Kernel configuration with
standard features, but specifically optimized for Intel Broadwell processors
during build-time. Which should provide a significant boost in performance on
machines with the respective processor family.
