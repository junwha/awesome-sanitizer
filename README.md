# Awesome Sanitizer [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
_A curated list of sanitizer resources._

Sanitizers are dynamic tools that detect software bugs through compiler instrumentation.

# Contents
- [C/C++](#cc)
  * [address sanity](#address-sanity)
  * [undefined behavior](#undefined-behavior)
  * [data races](#data-races)
  * [uninitialized reads](#uninitialized-reads)
  * [type confusion](#type-confusion)
  * [dataflow analysis](#dataflow-analysis)
- [Rust](#rust)
  * [address sanity](#address-sanity-1)
  * [data races](#data-races-1)
  * [uninitialized reads](#uninitialized-reads-1)
- [GPU](#gpu)
  * [sanitizers by vendors](#sanitizers-by-vendors)
  * [data races](#data-races-2)
- [ETC](#ETC)

# C/C++
## address sanity

[AddressSanitizer](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf) - A Fast Address Sanity Checker.
- [AddressSanitizer (Clang documentation)](https://clang.llvm.org/docs/AddressSanitizer.html)
- [wiki/Address Sanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer)  
- [HOWTO: Use Address Sanitizer](https://www.osc.edu/resources/getting_started/howto/howto_use_address_sanitizer)
  
[ASAN--](https://www.usenix.org/conference/usenixsecurity22/presentation/zhang-yuchen) - Debloating Address Sanitizer.
- [junxzm1990/ASAN--](https://github.com/junxzm1990/ASAN--)

[RetroWrite](https://ieeexplore.ieee.org/abstract/document/9152762) - Statically Instrumenting COTS Binaries for Fuzzing and Sanitization.
- [HexHive/retrowrite](https://github.com/HexHive/retrowrite)

[BoKASAN](https://www.usenix.org/conference/usenixsecurity23/presentation/cho) - Binary-only Kernel Address Sanitizer for Effective Kernel Fuzzing.
- [seclab-yonsei/BoKASAN](https://github.com/seclab-yonsei/BoKASAN)

[SafePM](https://dl.acm.org/doi/10.1145/3492321.3519574) -  a sanitizer for persistent memory.
- [TUM-DSE/safepm](https://github.com/TUM-DSE/safepm)  

[FuZZan](https://www.usenix.org/conference/atc20/presentation/jeon) - Efficient Sanitizer Metadata Design for Fuzzing.
- [HexHive/FuZZan](https://github.com/HexHive/FuZZan)

[SANRAZOR](https://www.usenix.org/conference/osdi21/presentation/zhang) - Reducing Redundant Sanitizer Checks in C/C++ Programs.
- [SanRazor-repo/SanRazor](https://github.com/SanRazor-repo/SanRazor)

[OBSan](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f103_paper.pdf) -  An Out-Of-Bound Sanitizer to Harden DNN Executables.
- [yanzuochen/obsan](https://github.com/yanzuochen/obsan)

[ASanity](https://ieeexplore.ieee.org/abstract/document/10188628) - On Bug Shadowing by Early ASan Exits.

[CMASan](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a074/21B7RisjQY0) - Custom Memory Allocator-aware Address Sanitizer

[GIANTSAN](https://dl.acm.org/doi/10.1145/3620665.3640391) - Efficient Memory Sanitization with Segment Folding

## undefined behavior

[UndefinedBehaviorSanitizer (Clang documentation)](https://clang.llvm.org/docs/UndefinedBehaviorSanitizer.html)
- [Improving Application Security with UndefinedBehaviorSanitizer (UBSan) and GCC](https://blogs.oracle.com/linux/post/improving-application-security-with-undefinedbehaviorsanitizer-ubsan-and-gcc)
- [A Guide to Undefined Behavior in C and C++](https://blog.regehr.org/archives/213) 
  
## data races

[ThreadSanitizer](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/35604.pdf) - data race detection in practice.
- [ThreadSanitizer (Clang documentation)](https://clang.llvm.org/docs/ThreadSanitizer.html)
- [wiki/ThreadSanitizer](https://github.com/google/sanitizers/wiki/ThreadSanitizerCppManual)

[BINTSAN](https://github.com/junwha/awesome-sanitizer/edit/main/README.md) - A Binary-level Thread Sanitizer or Why Sanitizing on the Binary Level is Hard

<!-- TODO: Add sanitizers for GPU data race -->

## uninitialized reads

[MemorySanitizer](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/43308.pdf) - fast detector of uninitialized memory use in C++.
- [MemorySanitizer (Clang documentation)](https://clang.llvm.org/docs/MemorySanitizer.html)
- [wiki/MemorySanitizer](https://github.com/google/sanitizers/wiki/MemorySanitizer)

[MTSan](https://www.usenix.org/conference/usenixsecurity23/presentation/chen-xingman) - A Feasible and Practical Memory Sanitizer for Fuzzing {COTS} Binaries.

[FloatZone](https://www.usenix.org/conference/usenixsecurity23/presentation/gorter) - Accelerating Memory Error Detection using the Floating Point Unit.
- [vusec/floatzone](https://github.com/vusec/floatzone)

- [MSET](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a088/21TfesaEHTy) - Evaluating the Effectiveness of Memory Safety Sanitizers

## type confusion

[TypeSan](https://dl.acm.org/doi/abs/10.1145/2976749.2978405) - Practical Type Confusion Detection.
- [vusec/typesan](https://github.com/vusec/typesan)

[CastSan](https://link.springer.com/chapter/10.1007/978-3-319-99073-6_1) - Efficient Detection of Polymorphic C++ Object Type Confusions with LLVM.

[HexType](https://dl.acm.org/doi/abs/10.1145/3133956.3134062) - Efficient Detection of Type Confusion Errors for C++.
- [HexHive/HexType](https://github.com/HexHive/HexType)

[EffectiveSan](https://dl.acm.org/doi/abs/10.1145/3192366.3192388) - type and memory error detection using dynamically typed C/C++.
- [GJDuck/EffectiveSan](https://github.com/GJDuck/EffectiveSan)

[TCD](https://ieeexplore.ieee.org/abstract/document/8987463/) - Statically Detecting Type Confusion Errors in C++ Programs.

[type++](https://nebelwelt.net/publications/files/25NDSS.pdf) - Prohibiting Type Confusion with Inline Type Information
- [HexHive/typepp](https://github.com/HexHive/typepp/)

[T-PRUNIFY](https://www.usenix.org/system/files/usenixsecurity24-zhai.pdf) - Don't Waste My Efforts: Pruning Redundant Sanitizer Checks by Developer-Implemented Type Checks


## dataflow analysis

[DataFlowSanitizer (Clang documentation)](https://clang.llvm.org/docs/DataFlowSanitizer.html)


# Rust
## address sanity

[AddressSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#addresssanitizer)

[HWAddressSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer)

[ERASan](https://www.computer.org/csdl/proceedings-article/sp/2024/313000a239/1WPcYZde4BW) - Efficient Rust Address Sanitizer.
- [S2-Lab/ERASan](https://github.com/S2-Lab/ERASan)

[RustSan](https://www.usenix.org/system/files/usenixsecurity24-cho-kyuwon.pdf) - Retrofitting AddressSanitizer for Efficient Sanitization of Rust


## data races

[ThreadSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer)

## uninitialized reads

[MemorySanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memorysanitizer)

[MemTagSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memtagsanitizer)

# GPU

## sanitizers by vendors

[NVIDIA: cuCatch](https://dl.acm.org/doi/abs/10.1145/3591225) - A Debugging Tool for Efficiently Catching Memory Safety Violations in CUDA Applications

[AMD: Using the AddressSanitizer on a GPU (beta release)](https://rocm.docs.amd.com/en/latest/conceptual/using-gpu-sanitizer.html)

## data races

[iGUARD](https://dl.acm.org/doi/abs/10.1145/3477132.3483545) - In-GPU Advanced Race Detection
- [csl-iisc/iGUARD-SOSP21](https://github.com/csl-iisc/iGUARD-SOSP21)

[cuCatch](https://dl.acm.org/doi/abs/10.1145/3591225) - A Debugging Tool for Efficiently Catching Memory Safety Violations in CUDA Applications


# ETC

[NeuralSanitizer](https://ieeexplore.ieee.org/abstract/document/10504286) - Detecting Backdoors in Neural Networks.

[DySan](https://dl.acm.org/doi/abs/10.1145/3433210.3453095?casa_token=RPAlXNyj-fMAAAAA:7comC496zZ1bnkYLCU3iCYEglWJCjC82USuU9fK41a-kqCVWqYpppaDpjYiCVRVKcE546RD62w) - Dynamically Sanitizing Motion Sensor Data Against Sensitive Inferences through Adversarial Networks.
- [DynamicSanitizer/DySan](https://github.com/DynamicSanitizer/DySan)

# Contributing
Please refer to the guidelines at [Contributing.md](https://github.com/junwha0511/awesome-sanitizer#Contributing.md) for details.

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>




