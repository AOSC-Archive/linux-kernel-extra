linux-kernel-extra
==================

This is a semi-official ABBS tree for extra Linux Kernel variants (patches,
forks, etc.) and configurations (say, for a specific machine type or processor
family). No binary is provided for packages in this tree, so you will need to
read our semi-comprehensive guide on how to build packages from an ABBS tree
[here](https://github.com/AOSC-Dev/aosc-os-abbs/wiki).

Kernel variants
---------------

#### march-kernel/linux-kernel-native

This class of packages provides Linux Kernel with native optimizations **specific
to the build machine** (-march=native flag). Which should result in a considerable
boost in performance at the price of losing any sort of portability.

#### featured-kernel/\*

This class of packages provides Linux Kernel with special features that are not
present in mainline kernel, such as the Con Kolivas' Kernel Patch Set (linux-ck),
PaX/Grsecurity kernel enhancement functionalities (linux-grsec), and so on.

Generally these kernels are designed to work on all architectures. However,
there may still be some kernels are platform-specific.

#### machine-kernel/\*

This class of packages provides Linux Kernel with machine-specific
optimizations, while retaining all the features that a mainline
[AOSC kernel](https://github.com/AOSC-Dev/aosc-os-abbs/tree/staging/extra-kernel/linux-kernel)
provides - `linux-kernel-broadwell` for instance, is a Kernel configuration with
standard features, but specifically optimized for Intel Broadwell processors
during build-time. Which should provide a significant boost in performance on
machines with the respective processor family.

(More to come in the future)
