# Awesome Sanitizer [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of sanitizer resources.

Sanitizers are dynamic tools that detect software bugs through compiler instrumentation, inserting runtime checks into the code during compilation. They are often paired with fuzzing, which uses random inputs to thoroughly test the instrumented code.

![Sanitizer_logo](https://github.com/user-attachments/assets/05b83fdd-2930-46df-ba78-e34a339bb6ac)

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
- [Miscellaneous](#miscellaneous)

---

## C/C++

### Address Sanity

- [AddressSanitizer (Paper)](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf) - A fast address sanity checker.
  ![Conference](https://img.shields.io/badge/USENIX_ATC-2022-red)
  - [AddressSanitizer (Clang Documentation)](https://clang.llvm.org/docs/AddressSanitizer.html) - Official Clang (LLVM) docs for Address Sanitizer.  
  - [wiki/AddressSanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer) - Address Sanitizer page in Google sanitizers wiki.  
  - [HOWTO: Use Address Sanitizer](https://www.osc.edu/resources/getting_started/howto/howto_use_address_sanitizer) - Basic usage tutorial for Address Sanitizer.

- [ASAN--](https://www.usenix.org/conference/usenixsecurity22/presentation/zhang-yuchen) - Debloating Address Sanitizer.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2012-red)
  [![Star](https://img.shields.io/github/stars/junxzm1990/ASAN--.svg?style=social&label=junxzm1990/ASAN--)](https://github.com/junxzm1990/ASAN--)

- [FuZZan](https://www.usenix.org/conference/atc20/presentation/jeon) - Efficient sanitizer metadata design for fuzzing.
  ![Conference](https://img.shields.io/badge/USENIX_ATC-2020-red)
  [![Star](https://img.shields.io/github/stars/HexHive/FuZZan.svg?style=social&label=HexHive/FuZZan)](https://github.com/HexHive/FuZZan)

- [SANRAZOR](https://www.usenix.org/conference/osdi21/presentation/zhang) - Reducing redundant sanitizer checks in C/C++ programs.
  ![Conference](https://img.shields.io/badge/USENIX_OSDI-2021-red)
  [![Star](https://img.shields.io/github/stars/SanRazor-repo/SanRazor.svg?style=social&label=SanRazor-repo/SanRazor)](https://github.com/SanRazor-repo/SanRazor)

- [RetroWrite](https://ieeexplore.ieee.org/abstract/document/9152762) - Statically instrumenting COTS binaries for fuzzing and sanitization.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2022-blue)
  [![Star](https://img.shields.io/github/stars/HexHive/retrowrite.svg?style=social&label=HexHive/retrowrite)](https://github.com/HexHive/retrowrite)

- [BoKASAN](https://www.usenix.org/conference/usenixsecurity23/presentation/cho) - Binary-only Kernel Address Sanitizer for effective kernel fuzzing.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2023-red)
  [![Star](https://img.shields.io/github/stars/seclab-yonsei/BoKASAN.svg?style=social&label=seclab-yonsei/BoKASAN)](https://github.com/seclab-yonsei/BoKASAN)
  
- [SafePM](https://dl.acm.org/doi/10.1145/3492321.3519574) - A sanitizer for persistent memory.
    ![Conference](https://img.shields.io/badge/ACM_EUROSYS-2022-green)
    [![Star](https://img.shields.io/github/stars/TUM-DSE/safepm.svg?style=social&label=TUM-DSE/safepm)](https://github.com/TUM-DSE/safepm)

- [OBSan](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f103_paper.pdf) - An out-of-bound sanitizer to harden DNN executables.
  ![Conference](https://img.shields.io/badge/NDSS-2023-lightblue)
  [![Star](https://img.shields.io/github/stars/yanzuochen/obsan.svg?style=social&label=yanzuochen/obsan)](https://github.com/yanzuochen/obsan)

- [ASanity](https://ieeexplore.ieee.org/abstract/document/10188628) - On bug shadowing by early ASan exits.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2023-blue)

- [GWP-ASan](https://arxiv.org/abs/2311.09394) - Sampling-Based Detection of Memory-Safety Bugs in Production.
  ![Conference](https://img.shields.io/badge/IEEE_ICSE-2024-blue)
  [![Star](https://img.shields.io/github/stars/google/gwpsan.svg?style=social&label=google/gwpsan)](https://github.com/google/gwpsan)

- [GIANTSAN](https://dl.acm.org/doi/10.1145/3620665.3640391) - Efficient memory sanitization with segment folding.
  ![Conference](https://img.shields.io/badge/ACM_ASPLOS-2024-9163aa)
  [![Star](https://img.shields.io/github/stars/AceSrc/GiantSan-Artifact.svg?style=social&label=AceSrc/GiantSan-Artifact)](https://github.com/AceSrc/GiantSan-Artifact)
  
- [CMASan](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a074/21B7RisjQY0) - Custom Memory Allocator-aware Address Sanitizer.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2025-blue)

### Undefined Behavior

- [UndefinedBehaviorSanitizer (Clang Documentation)](https://clang.llvm.org/docs/UndefinedBehaviorSanitizer.html) - Official Clang (LLVM) docs for Undefined Behavior Sanitizer.  
  - [Improving Application Security with UndefinedBehaviorSanitizer and GCC](https://blogs.oracle.com/linux/post/improving-application-security-with-undefinedbehaviorsanitizer-ubsan-and-gcc) - Basic usage tutorial for Undefined Behavior Sanitizer in Oracle blog.  
  - [A Guide to Undefined Behavior in C and C++](https://blog.regehr.org/archives/213) - Basic usage tutorial for Undefined Behavior Sanitizer in John Regehr's blog.

### Data Races

- [ThreadSanitizer (Paper)](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/35604.pdf) - Data race detection in practice.  
  - [ThreadSanitizer (Clang Documentation)](https://clang.llvm.org/docs/ThreadSanitizer.html) - Official Clang (LLVM) docs for Thread Sanitizer.  
  - [wiki/ThreadSanitizer](https://github.com/google/sanitizers/wiki/ThreadSanitizerCppManual) - Thread Sanitizer page in Google sanitizers wiki.

- [BINTSAN](https://www.usenix.org/conference/usenixsecurity24/presentation/schilling) - A Binary-level Thread Sanitizer or Why Sanitizing on the Binary Level is Hard.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)

### Uninitialized Reads

- [MemorySanitizer (Paper)](https://static.googleusercontent.com/media/research.google.com/ko//pubs/archive/43308.pdf) - Fast detector of uninitialized memory use in C++.  
  - [MemorySanitizer (Clang Documentation)](https://clang.llvm.org/docs/MemorySanitizer.html) - Official Clang docs.  
  - [wiki/MemorySanitizer](https://github.com/google/sanitizers/wiki/MemorySanitizer) - Google sanitizers wiki.

- [MTSan](https://www.usenix.org/conference/usenixsecurity23/presentation/chen-xingman) - A feasible and practical memory sanitizer for fuzzing COTS binaries.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2023-red)

- [FloatZone](https://www.usenix.org/conference/usenixsecurity23/presentation/gorter) - Accelerating memory error detection using the floating point unit.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2023-red)
  [![Star](https://img.shields.io/github/stars/vusec/floatzone.svg?style=social&label=vusec/floatzone)](https://github.com/vusec/floatzone)

- [MSET](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a088/21TfesaEHTy) - Evaluating the effectiveness of memory safety sanitizers
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2025-blue)

### Type Confusion

- [TypeSan](https://dl.acm.org/doi/abs/10.1145/2976749.2978405) - Practical type confusion detection.
  ![Conference](https://img.shields.io/badge/ACM_CCS-2016-a0501b)
  [![Star](https://img.shields.io/github/stars/vusec/typesan.svg?style=social&label=vusec/typesan)](https://github.com/vusec/typesan)

- [HexType](https://dl.acm.org/doi/abs/10.1145/3133956.3134062) - Efficient detection of type confusion errors for C++.
  ![Conference](https://img.shields.io/badge/ACM_CCS-2017-a0501b)
  [![Star](https://img.shields.io/github/stars/HexHive/HexType.svg?style=social&label=HexHive/HexType)](https://github.com/HexHive/HexType)

- [CastSan](https://link.springer.com/chapter/10.1007/978-3-319-99073-6_1) - Efficient detection of polymorphic C++ object type confusions with LLVM.
  ![Conference](https://img.shields.io/badge/ESORICS-2018-ff9999)

- [EffectiveSan](https://dl.acm.org/doi/abs/10.1145/3192366.3192388) - Type and memory error detection using dynamically typed C/C++.
  ![Conference](https://img.shields.io/badge/ACM_PLDI-2018-8c5a2c)
  [![Star](https://img.shields.io/github/stars/GJDuck/EffectiveSan.svg?style=social&label=GJDuck/EffectiveSan)](https://github.com/GJDuck/EffectiveSan)

- [TCD](https://ieeexplore.ieee.org/abstract/document/8987463) - Statically detecting type confusion errors in C++ programs.
  ![Conference](https://img.shields.io/badge/IEEE_ISSRE-2019-blue)

- [Type++](https://nebelwelt.net/publications/files/25NDSS.pdf) - Prohibiting type confusion with inline type information.
  ![Conference](https://img.shields.io/badge/NDSS-2025-lightblue)
  [![Star](https://img.shields.io/github/stars/HexHive/typepp.svg?style=social&label=HexHive/typepp)](https://github.com/HexHive/typepp)

- [T-PRUNIFY](https://www.usenix.org/system/files/usenixsecurity24-zhai.pdf) - Pruning redundant sanitizer checks by developer-implemented type checks.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)
  [![Star](https://img.shields.io/github/stars/seclab-ucr/TPrunify.svg?style=social&label=seclab-ucr/TPrunify)](https://github.com/seclab-ucr/TPrunify)

### Dataflow Analysis

- [DataFlowSanitizer (Clang Documentation)](https://clang.llvm.org/docs/DataFlowSanitizer.html) - A general data flow analysis framework.

---

## Rust

### Address Sanity

- [AddressSanitizer (Rust Documentation)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#addresssanitizer) - Address Sanitizer for Rust.  
- [HWAddressSanitizer (Rust Documentation)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#hwaddresssanitizer) - Hardware-assisted Address Sanitizer  for Rust.  

- [ERASan](https://www.computer.org/csdl/proceedings-article/sp/2024/313000a239/1WPcYZde4BW) - Efficient Rust Address Sanitizer.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)
  [![Star](https://img.shields.io/github/stars/S2-Lab/ERASan.svg?style=social&label=S2-Lab/ERASan)](https://github.com/S2-Lab/ERASan)

- [RustSan](https://www.usenix.org/system/files/usenixsecurity24-cho-kyuwon.pdf) - Retrofitting AddressSanitizer for efficient sanitization of Rust.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)
  [![Star](https://img.shields.io/github/stars/sslab-skku/RustSan.svg?style=social&label=sslab-skku/RustSan)](https://github.com/sslab-skku/RustSan)

### Data Races

- [ThreadSanitizer (Rust Documentation)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#threadsanitizer) - Thread Sanitizer for Rust.

### Uninitialized Reads

- [MemorySanitizer (Rust Documentation)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memorysanitizer) - Memory Sanitizer for Rust.  
- [MemTagSanitizer (Rust Documentation)](https://doc.rust-lang.org/beta/unstable-book/compiler-flags/sanitizer.html#memtagsanitizer) - Memory tagging for Rust.

---

## GPU

### Sanitizers by Vendors

- [NVIDIA: cuCatch](https://dl.acm.org/doi/abs/10.1145/3591225) - A debugging tool for efficiently catching memory safety violations in CUDA applications.
- [AMD: Using the AddressSanitizer on a GPU](https://rocm.docs.amd.com/en/latest/conceptual/using-gpu-sanitizer.html) - Document for AMD's GPU sanitizer.

### Data Races

- [iGUARD](https://dl.acm.org/doi/abs/10.1145/3477132.3483545) - In-GPU advanced race detection.
  ![Conference](https://img.shields.io/badge/ACM_SOSP-2021-177e25)
  [![Star](https://img.shields.io/github/stars/csl-iisc/iGUARD-SOSP21.svg?style=social&label=csl-iisc/iGUARD-SOSP21)](https://github.com/csl-iisc/iGUARD-SOSP21)

---

## Miscellaneous

- [DySan](https://dl.acm.org/doi/abs/10.1145/3433210.3453095) - Dynamically sanitizing motion sensor data through adversarial networks.
  ![Conference](https://img.shields.io/badge/ACM_Asia_CCS-2021-a0501b)
  [![Star](https://img.shields.io/github/stars/DynamicSanitizer/DySan.svg?style=social&label=DynamicSanitizer/DySan)](https://github.com/DynamicSanitizer/DySan)

- [NeuralSanitizer](https://ieeexplore.ieee.org/abstract/document/10504286) - Detecting backdoors in neural networks.
  [![Transaction](https://img.shields.io/badge/IEEE_IFS-2024-blue)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)
  [![Star](https://img.shields.io/github/stars/zhuhong1996/NeuralSanitizer.svg?style=social&label=zhuhong1996/NeuralSanitizer)](https://github.com/zhuhong1996/NeuralSanitizer)

---

## Contributing

Please refer to the guidelines at [contributing.md](https://github.com/junwha0511/awesome-sanitizer#contributing.md) for details.
