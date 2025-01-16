# Awesome Sanitizer [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
A curated list of sanitizer resources.

Sanitizers are dynamic tools that detect software bugs through compiler instrumentation.

## Contents
- [C/C++](#cc)
  - [Address Sanity](#address-sanity)
  - [Undefined Behavior](#undefined-behavior)
  - [Data Races](#data-races)
  - [Uninitialized Reads](#uninitialized-reads)
  - [Type Confusion](#type-confusion)
  - [Dataflow Analysis](#dataflow-analysis)
- [Rust](#rust)
  - [Address Sanity](#address-sanity-1)
  - [Data Races](#data-races-1)
  - [Uninitialized Reads](#uninitialized-reads-1)
- [GPU](#gpu)
  - [Sanitizers by Vendors](#sanitizers-by-vendors)
  - [Data Races](#data-races-2)
- [Etc](#etc)

---

## C/C++

### Address Sanity

- [AddressSanitizer (Paper)](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf) - A fast address sanity checker.  
  - [AddressSanitizer (Clang Documentation)](https://clang.llvm.org/docs/AddressSanitizer.html) - Official Clang docs.  
  - [wiki/AddressSanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer) - Google sanitizers wiki.  
  - [HOWTO: Use Address Sanitizer](https://www.osc.edu/resources/getting_started/howto/howto_use_address_sanitizer) - Basic usage tutorial.

- [ASAN--](https://www.usenix.org/conference/usenixsecurity22/presentation/zhang-yuchen) - Debloating Address Sanitizer.  
  - [junxzm1990/ASAN--](https://github.com/junxzm1990/ASAN--) - Repository for ASAN--.

- [RetroWrite](https://ieeexplore.ieee.org/abstract/document/9152762) - Statically instrumenting COTS binaries for fuzzing and sanitization.  
  - [HexHive/retrowrite](https://github.com/HexHive/retrowrite) - RetroWrite implementation.

- [BoKASAN](https://www.usenix.org/conference/usenixsecurity23/presentation/cho) - Binary-only Kernel Address Sanitizer for effective kernel fuzzing.  
  - [seclab-yonsei/BoKASAN](https://github.com/seclab-yonsei/BoKASAN) - Repository for BoKASAN.

- [SafePM](https://dl.acm.org/doi/10.1145/3492321.3519574) - A sanitizer for persistent memory.  
  - [TUM-DSE/safepm](https://github.com/TUM-DSE/safepm) - SafePM repository.

- [FuZZan](https://www.usenix.org/conference/atc20/presentation/jeon) - Efficient sanitizer metadata design for fuzzing.  
  - [HexHive/FuZZan](https://github.com/HexHive/FuZZan) - FuZZan repository.

- [SANRAZOR](https://www.usenix.org/conference/osdi21/presentation/zhang) - Reducing redundant sanitizer checks in C/C++ programs.  
  - [SanRazor-repo/SanRazor](https://github.com/SanRazor-repo/SanRazor) - SanRazor repository.

- [OBSan](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f103_paper.pdf) - An out-of-bound sanitizer to harden DNN executables.  
  - [yanzuochen/obsan](https://github.com/yanzuochen/obsan) - OBSan repository.

- [ASanity](https://ieeexplore.ieee.org/abstract/document/10188628) - On bug shadowing by early ASan exits.

- [CMASan](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a074/21B7RisjQY0) - Custom Memory Allocator-aware Address Sanitizer.

- [GIANTSAN](https://dl.acm.org/doi/10.1145/3620665.3640391) - Efficient memory sanitization with segment folding.

### Undefined Behavior

- [UndefinedBehaviorSanitizer (Clang Documentation)](https://clang.llvm.org/docs/UndefinedBehaviorSanitizer.html) - Official Clang docs.  
  - [Improving Application Security with UndefinedBehaviorSanitizer and GCC](https://blogs.oracle.com/linux/post/improving-application-security-with-undefinedbehaviorsanitizer-ubsan-and-gcc) - Oracle blog post.  
  - [A Guide to Undefined Behavior in C and C++](https://blog.regehr.org/archives/213) - John Regehr's blog.

### Data Races

- [ThreadSanitizer (Paper)](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/35604.pdf) - Data race detection in practice.  
  - [ThreadSanitizer (Clang Documentation)](https://clang.llvm.org/docs/ThreadSanitizer.html) - Official Clang docs.  
  - [wiki/ThreadSanitizer](https://github.com/google/sanitizers/wiki/ThreadSanitizerCppManual) - Google sanitizers wiki.

- [BINTSAN](https://www.usenix.org/conference/usenixsecurity24/presentation/schilling) - A Binary-level Thread Sanitizer or Why Sanitizing on the Binary Level is Hard.

### Uninitialized Reads

- [MemorySanitizer (Paper)](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/43308.pdf) - Fast detector of uninitialized memory use in C++.  
  - [MemorySanitizer (Clang Documentation)](https://clang.llvm.org/docs/MemorySanitizer.html) - Official Clang docs.  
  - [wiki/MemorySanitizer](https://github.com/google/sanitizers/wiki/MemorySanitizer) - Google sanitizers wiki.

- [MTSan](https://www.usenix.org/conference/usenixsecurity23/presentation/chen-xingman) - A feasible and practical memory sanitizer for fuzzing COTS binaries.

- [FloatZone](https://www.usenix.org/conference/usenixsecurity23/presentation/gorter) - Accelerating memory error detection using the floating point unit.  
  - [vusec/floatzone](https://github.com/vusec/floatzone) - FloatZone repository.

- [MSET](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a088/21TfesaEHTy) - Evaluating the effectiveness of memory safety sanitizers.

### Type Confusion

- [TypeSan](https://dl.acm.org/doi/abs/10.1145/2976749.2978405) - Practical type confusion detection.  
  - [vusec/typesan](https://github.com/vusec/typesan) - TypeSan repository.

- [CastSan](https://link.springer.com/chapter/10.1007/978-3-319-99073-6_1) - Efficient detection of polymorphic C++ object type confusions with LLVM.

- [HexType](https://dl.acm.org/doi/abs/10.1145/3133956.3134062) - Efficient detection of type confusion errors for C++.  
  - [HexHive/HexType](https://github.com/HexHive/HexType) - HexType repository.

- [EffectiveSan](https://dl.acm.org/doi/abs/10.1145/3192366.3192388) - Type and memory error detection using dynamically typed C/C++.  
  - [GJDuck/EffectiveSan](https://github.com/GJDuck/EffectiveSan) - EffectiveSan repository.

- [TCD](https://ieeexplore.ieee.org/abstract/document/8987463/) - Statically detecting type confusion errors in C++ programs.

- [Type++](https://nebelwelt.net/publications/files/25NDSS.pdf) - Prohibiting type confusion with inline type information.  
  - [HexHive/typepp](https://github.com/HexHive/typepp/) - Type++ repository.

- [T-PRUNIFY](https://www.usenix.org/system/files/usenixsecurity24-zhai.pdf) - Pruning redundant sanitizer checks by developer-implemented type checks.

### Dataflow Analysis

- [DataFlowSanitizer (Clang Documentation)](https://clang.llvm.org/docs/DataFlowSanitizer.html) - A general data flow analysis framework.

---

## Rust

### Address Sanity

- [AddressSanitizer (Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#addresssanitizer) - AddressSanitizer for Rust.  
- [HWAddressSanitizer (Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#hwaddresssanitizer) - Hardware-assisted ASan for Rust.

- [ERASan](https://www.computer.org/csdl/proceedings-article/sp/2024/313000a239/1WPcYZde4BW) - Efficient Rust Address Sanitizer.  
  - [S2-Lab/ERASan](https://github.com/S2-Lab/ERASan) - ERASan repository.

- [RustSan](https://www.usenix.org/system/files/usenixsecurity24-cho-kyuwon.pdf) - Retrofitting AddressSanitizer for efficient sanitization of Rust.

### Data Races

- [ThreadSanitizer (Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer) - ThreadSanitizer for Rust.

### Uninitialized Reads

- [MemorySanitizer (Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memorysanitizer) - MSan for Rust.  
- [MemTagSanitizer (Rust Unstable Book)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memtagsanitizer) - Memory tagging for Rust.

---

## GPU

### Sanitizers by Vendors

- [NVIDIA: cuCatch](https://dl.acm.org/doi/abs/10.1145/3591225) - A debugging tool for efficiently catching memory safety violations in CUDA applications.
- [AMD: Using the AddressSanitizer on a GPU](https://rocm.docs.amd.com/en/latest/conceptual/using-gpu-sanitizer.html) - Beta release for AMD's GPU sanitizer.

### Data Races

- [iGUARD](https://dl.acm.org/doi/abs/10.1145/3477132.3483545) - In-GPU advanced race detection.  
  - [csl-iisc/iGUARD-SOSP21](https://github.com/csl-iisc/iGUARD-SOSP21) - iGUARD repository.

---

## Etc

- [NeuralSanitizer](https://ieeexplore.ieee.org/abstract/document/10504286) - Detecting backdoors in neural networks.
- [DySan](https://dl.acm.org/doi/abs/10.1145/3433210.3453095) - Dynamically sanitizing motion sensor data through adversarial networks.  
  - [DynamicSanitizer/DySan](https://github.com/DynamicSanitizer/DySan) - DySan repository.

---

## Contributing

Please refer to the guidelines at [Contributing.md](https://github.com/junwha0511/awesome-sanitizer#Contributing.md) for details.

<sub><i><a href="http://ecotrust-canada.github.io/markdown-toc/">Table of contents generated with markdown-toc</a></i></sub>
