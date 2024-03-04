# awesome-sanitizers
A curated list of sanitizers to detect bugs

# C/C++
## Sanitizers to detect memory errors
- [AddressSanitizer: A Fast Address Sanity Checker](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf)
  - [AddressSanitizer (Clang documentation)](https://clang.llvm.org/docs/AddressSanitizer.html)
  - [wiki/Address Sanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer)  
  - [HOWTO: Use Address Sanitizer](https://www.osc.edu/resources/getting_started/howto/howto_use_address_sanitizer)
- [Debloating Address Sanitizer](https://www.usenix.org/conference/usenixsecurity22/presentation/zhang-yuchen)
  - [junxzm1990/ASAN--](https://github.com/junxzm1990/ASAN--) 
- [BoKASAN: Binary-only Kernel Address Sanitizer for Effective Kernel Fuzzing](https://www.usenix.org/conference/usenixsecurity23/presentation/cho)
  - [seclab-yonsei/BoKASAN](https://github.com/seclab-yonsei/BoKASAN)
- [SafePM: a sanitizer for persistent memory](https://dl.acm.org/doi/10.1145/3492321.3519574)
  - [TUM-DSE/safepm](https://github.com/TUM-DSE/safepm)  
- [FuZZan: Efficient Sanitizer Metadata Design for Fuzzing](https://www.usenix.org/conference/atc20/presentation/jeon)
  - [HexHive/FuZZan](https://github.com/HexHive/FuZZan)
- [SANRAZOR: Reducing Redundant Sanitizer Checks in C/C++ Programs](https://www.usenix.org/conference/osdi21/presentation/zhang)
  - [SanRazor-repo/SanRazor](https://github.com/SanRazor-repo/SanRazor)
- [OBSan: An Out-Of-Bound Sanitizer to Harden DNN Executables.](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f103_paper.pdf)
  - [yanzuochen/obsan](https://github.com/yanzuochen/obsan)
## Sanitizers to detect data races
- [ThreadSanitizer – data race detection in practice](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/35604.pdf)
  - [ThreadSanitizer (Clang documentation)](https://clang.llvm.org/docs/ThreadSanitizer.html)
  - [wiki/ThreadSanitizer](https://github.com/google/sanitizers/wiki/ThreadSanitizerCppManual)
<!-- TODO: Add sanitizers for GPU data race -->

## Sanitizers to detect uninitialized reads
- [MemorySanitizer: fast detector of uninitialized memory use in C++](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/43308.pdf)
  - [MemorySanitizer (Clang documentation)](https://clang.llvm.org/docs/MemorySanitizer.html)
  - [wiki/MemorySanitizer](https://github.com/google/sanitizers/wiki/MemorySanitizer)

## Sanitizers to detect type confusion
- [TypeSan: Practical Type Confusion Detection](https://dl.acm.org/doi/abs/10.1145/2976749.2978405)
- [CastSan: Efficient Detection of Polymorphic C++ Object Type Confusions with LLVM](https://link.springer.com/chapter/10.1007/978-3-319-99073-6_1)
- [HexType: Efficient Detection of Type Confusion Errors for C++](https://dl.acm.org/doi/abs/10.1145/3133956.3134062)
- [EffectiveSan: type and memory error detection using dynamically typed C/C++](https://dl.acm.org/doi/abs/10.1145/3192366.3192388)
- [TCD: Statically Detecting Type Confusion Errors in C++ Programs](https://ieeexplore.ieee.org/abstract/document/8987463/)

## Sanitizers for dataflow analysis
- [DataFlowSanitizer (Clang documentation)](https://clang.llvm.org/docs/DataFlowSanitizer.html)


# Rust
## Sanitizers to detect memory errors
- [AddressSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#addresssanitizer)
- [HWAddressSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer)

## Sanitizers to detect data races
- [ThreadSanitizer (The Rust Unstable Book)]( ()

## Sanitizers to detect uninitialized reads
- [MemorySanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memorysanitizer)
- [MemTagSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memtagsanitizer)
