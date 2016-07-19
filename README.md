linux-kernel-extra
==================

This is a semi-official ABBS tree for extra Linux Kernel variants (patches,
forks, etc.) and configurations (say, for a specific machine type or processor
family). No binary is provided for packages in this tree, so you will need to
read our semi-comprehensive guide on how to build packages from an ABBS tree
[here](https://github.com/AOSC-Dev/aosc-os-abbs/wiki).

Kernel variants
---------------

#### march-kernel/\*

This class of packages provides Linux Kernel with machine-specific
optimizations, while retaining all the features that a mainline AOSC kernel
provides - `linux-kernel-broadwell` for instance, is a Kernel configuration with
standard features, but specifically optimized for Intel Broadwell processors
during build-time. Which should provide a significant boost in performance on
machines with the respective processor family.

(More to come in the future)
