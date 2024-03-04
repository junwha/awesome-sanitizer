# awesome-sanitizers
A curated list of sanitizers to detect bugs

# C/C++
## Sanitizers to detect memory errors
- [AddressSanitizer](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf) - A Fast Address Sanity Checker
  - [AddressSanitizer (Clang documentation)](https://clang.llvm.org/docs/AddressSanitizer.html)
  - [wiki/Address Sanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer)  
  - [HOWTO: Use Address Sanitizer](https://www.osc.edu/resources/getting_started/howto/howto_use_address_sanitizer)
- [ASAN--](https://www.usenix.org/conference/usenixsecurity22/presentation/zhang-yuchen) - Debloating Address Sanitizer
  - [junxzm1990/ASAN--](https://github.com/junxzm1990/ASAN--) 
- [BoKASAN](https://www.usenix.org/conference/usenixsecurity23/presentation/cho) - Binary-only Kernel Address Sanitizer for Effective Kernel Fuzzing
  - [seclab-yonsei/BoKASAN](https://github.com/seclab-yonsei/BoKASAN)
- [SafePM](https://dl.acm.org/doi/10.1145/3492321.3519574) -  a sanitizer for persistent memory
  - [TUM-DSE/safepm](https://github.com/TUM-DSE/safepm)  
- [FuZZan](https://www.usenix.org/conference/atc20/presentation/jeon) - Efficient Sanitizer Metadata Design for Fuzzing
  - [HexHive/FuZZan](https://github.com/HexHive/FuZZan)
- [SANRAZOR](https://www.usenix.org/conference/osdi21/presentation/zhang) - Reducing Redundant Sanitizer Checks in C/C++ Programs
  - [SanRazor-repo/SanRazor](https://github.com/SanRazor-repo/SanRazor)
- [OBSan](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f103_paper.pdf) -  An Out-Of-Bound Sanitizer to Harden DNN Executables
  - [yanzuochen/obsan](https://github.com/yanzuochen/obsan)
## Sanitizers to detect data races
- [ThreadSanitizer](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/35604.pdf) - data race detection in practice
  - [ThreadSanitizer (Clang documentation)](https://clang.llvm.org/docs/ThreadSanitizer.html)
  - [wiki/ThreadSanitizer](https://github.com/google/sanitizers/wiki/ThreadSanitizerCppManual)
<!-- TODO: Add sanitizers for GPU data race -->

## Sanitizers to detect uninitialized reads
- [MemorySanitizer](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/43308.pdf) - fast detector of uninitialized memory use in C++
  - [MemorySanitizer (Clang documentation)](https://clang.llvm.org/docs/MemorySanitizer.html)
  - [wiki/MemorySanitizer](https://github.com/google/sanitizers/wiki/MemorySanitizer)

## Sanitizers to detect type confusion
- [TypeSan](https://dl.acm.org/doi/abs/10.1145/2976749.2978405) - Practical Type Confusion Detection
- [CastSan](https://link.springer.com/chapter/10.1007/978-3-319-99073-6_1) - Efficient Detection of Polymorphic C++ Object Type Confusions with LLVM
- [HexType](https://dl.acm.org/doi/abs/10.1145/3133956.3134062) - Efficient Detection of Type Confusion Errors for C++
- [EffectiveSan](https://dl.acm.org/doi/abs/10.1145/3192366.3192388) - type and memory error detection using dynamically typed C/C++
- [TCD](https://ieeexplore.ieee.org/abstract/document/8987463/) - Statically Detecting Type Confusion Errors in C++ Programs

## Sanitizers for dataflow analysis
- [DataFlowSanitizer (Clang documentation)](https://clang.llvm.org/docs/DataFlowSanitizer.html)


# Rust
## Sanitizers to detect memory errors
- [AddressSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#addresssanitizer)
- [HWAddressSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer)

## Sanitizers to detect data races
- [ThreadSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer)

## Sanitizers to detect uninitialized reads
- [MemorySanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memorysanitizer)
- [MemTagSanitizer (The Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memtagsanitizer)
