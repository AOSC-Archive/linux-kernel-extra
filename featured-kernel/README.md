# Featured Kernels

## `linux-kernel-ck`

This variant of Linux Kernel adds [Con Kolivas' Kernel patchset](http://ck.kolivas.org/patches/)
to specially improve responsiveness and interactivity for everyday use on
desktop computers (with CPU that has fewer than 16 cores). CK Kernel features:

- [The Multiple Queue Skiplist Scheduler](https://en.wikipedia.org/wiki/Brain_Fuck_Scheduler)
(MuQSS, was BFS before), whose main focus is to _"achieve excellent desktop
interactivity and responsiveness without heuristics and tuning knobs that are
difficult to understand"_;
- Many improvements on process scheduling, specially tuned for desktop
computers.

Note that since MuQSS does not rely on ticks for rescheduling interrupts, we
have set the tick rate to 100Hz (`CONFIG_HZ=100`), to (as MuQSS describes)
"benefit from the lower overhead and higher throughput of fewer timer ticks",
and (hopefully) reduce heating and power drain. This kernel is suitable for
laptop computers.

## `linux-kernel-grsec`

This variant of Linux Kernel adds [PaX/Grsecurity](https://en.wikipedia.org/wiki/Grsecurity)
to enhance security of Linux Kernel.

Due to the upstream decision, this kernel is not being maintained now.

## `linux-kernel-libre`

This variant of Linux Kernel does not add anything; instead, it removes all
non-free binary blobs that are included in vanilla Linux Kernel. If you would
like to use a 100% free (as in freedom) system, you may want this.

This kernel is AOSC mainline kernel without binary blobs.

See https://www.fsfla.org/ikiwiki/selibre/linux-libre/ for more information.

## `linux-kernel-zen`

This variant is [ZEN kernel](https://github.com/zen-kernel/zen-kernel) with AOSC
configurations (broken-out patches are from the maintainer Jan Steffens
(@heftig): http://pkgbuild.com/~heftig/zen-patches/). The ZEN kernel is _"the
result of a collaborative effort of kernel hackers to provide the best Linux
kernel possible for everyday systems"_
(https://wiki.archlinux.org/index.php/Kernels), just like `linux-kernel-ck`,
only with different maintainers and optimization directions.

Note that ZEN is developed with emphasis of responsiveness. Although ZEN is
similar to CK, we instead have tuned this kernel for absolute interactivity
(`CONFIG_ZEN_INTERACTIVE=y`). In addition, we have enabled **native march
compilation (`CONFIG_MNATIVE=y`)**, which means **this kernel will only be able
to run on the machine where the kernel is compiled (or newer)**. While this
fully utilize your processor (and boost the system), you should know that **this
kernel is not portable once it is compiled**.

See https://github.com/zen-kernel/zen-kernel/issues/30 for more information.
