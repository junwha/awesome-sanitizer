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
  - [Sanitizer Unification](#sanitizer-unification)
- [Rust](#rust)
  - [Address Sanity](#address-sanity-1)
  - [Undefined Behavior](#undefined-behavior-1)
  - [Data Races](#data-races-1)
  - [Uninitialized Reads](#uninitialized-reads-1)
- [GPU](#gpu)
  - [Sanitizers by Vendors](#sanitizers-by-vendors)
  - [Data Races](#data-races-and-others)
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

- [SafePM](https://dl.acm.org/doi/10.1145/3492321.3519574) - A sanitizer for persistent memory.
    ![Conference](https://img.shields.io/badge/ACM_EUROSYS-2022-green)
    [![Star](https://img.shields.io/github/stars/TUM-DSE/safepm.svg?style=social&label=TUM-DSE/safepm)](https://github.com/TUM-DSE/safepm)

- [BoKASAN](https://www.usenix.org/conference/usenixsecurity23/presentation/cho) - Binary-only Kernel Address Sanitizer for effective kernel fuzzing.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2023-red)
  [![Star](https://img.shields.io/github/stars/seclab-yonsei/BoKASAN.svg?style=social&label=seclab-yonsei/BoKASAN)](https://github.com/seclab-yonsei/BoKASAN)  

- [OBSan](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f103_paper.pdf) - An out-of-bound sanitizer to harden DNN executables.
  ![Conference](https://img.shields.io/badge/NDSS-2023-lightblue)
  [![Star](https://img.shields.io/github/stars/yanzuochen/obsan.svg?style=social&label=yanzuochen/obsan)](https://github.com/yanzuochen/obsan)

- [ASanity](https://ieeexplore.ieee.org/abstract/document/10188628) - On bug shadowing by early ASan exits.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2023-blue)

- [GWP-ASan](https://arxiv.org/abs/2311.09394) - Sampling-Based Detection of Memory-Safety Bugs in Production.
  ![Conference](https://img.shields.io/badge/IEEE_ICSE-2024-blue)
  [![Star](https://img.shields.io/github/stars/google/gwpsan.svg?style=social&label=google/gwpsan)](https://github.com/google/gwpsan)

- [GIANTSAN](https://dl.acm.org/doi/10.1145/3620665.3640391) - Efficient memory sanitization with segment folding.
  ![Conference](https://img.shields.io/badge/ACM_ASPLOS-2024-9163aa) ![Conference](https://img.shields.io/badge/ACM_TCS-2025-047e63)
  [![Star](https://img.shields.io/github/stars/AceSrc/GiantSan-Artifact.svg?style=social&label=AceSrc/GiantSan-Artifact)](https://github.com/AceSrc/GiantSan-Artifact)
  
- [Top of the Heap](https://dl.acm.org/doi/10.1145/3658644.3690310) - Efficient memory error protection of safe heap objects.
  ![Conference](https://img.shields.io/badge/ACM_CCS-2024-a0501b)

- [ShadowBound](https://www.usenix.org/conference/usenixsecurity24/presentation/yu-zheng) - Efficient heap memory protection through advanced shadow metadata management and customized compiler optimization.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)
  [![Star](https://img.shields.io/github/stars/cla7aye15I4nd/shadowbound.svg?style=social&label=cla7aye15I4nd/shadowbound)](https://github.com/cla7aye15I4nd/shadowbound)

- [CAMP](https://www.usenix.org/conference/usenixsecurity24/presentation/lin-zhenpeng) - Compiler and allocator-based heap memory protection using boundary-checking instrumentation and escape tracking.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)
  [![Star](https://img.shields.io/github/stars/cla7aye15I4nd/CAMP.svg?style=social&label=cla7aye15I4nd/CAMP)](https://github.com/cla7aye15I4nd/CAMP)

- [IPEA-San](https://www.ndss-symposium.org/ndss-paper/facilitating-non-intrusive-in-vivo-firmware-testing-with-stateless-instrumentation/) - Pointer capability-based sanitizer for resource-constrained IoT firmware with stateless instrumentation.
  ![Conference](https://img.shields.io/badge/NDSS-2024-lightblue)

- [Sticky Tags](https://ieeexplore.ieee.org/document/10646704) - Efficient and deterministic spatial memory error mitigation using ARM MTE with persistent memory tags.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2024-blue)

- [CMASan](https://www.computer.org/csdl/proceedings-article/sp/2025/223600a074/21B7RisjQY0) - Custom Memory Allocator-aware Address Sanitizer.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2025-blue)
  [![Star](https://img.shields.io/github/stars/S2-Lab/CMASan.svg?style=social&label=S2-Lab/CMASan)](https://github.com/S2-Lab/CMASan)

- [DFirmSan](https://www.sciencedirect.com/science/article/pii/S0167404825001567?casa_token=2yJobOJo0_IAAAAA:SqBqM9nbyqtIQ2el6rhlDX5lJRv-rhbDZwuMXAOwHbnul4TTyat9d6eFwRDW-E7g3ZKbyAI_7TUY) - DFirmSan: A lightweight dynamic memory sanitizer for Linux-based firmware
  ![Conference](https://img.shields.io/badge/ELSEVIER_C&S-2025-orange)
  [![Star](https://img.shields.io/github/stars/dierye/dfirmsan.svg?style=social&label=dierye/dfirmsan)](https://github.com/dierye/dfirmsan)

- [RangeSanitizer](https://download.vusec.net/papers/rsan_sec25.pdf) - Detecting Memory Errors with Efficient Range Checks
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2025-red)
  [![Star](https://img.shields.io/github/stars/vusec/rangesanitizer.svg?style=social&label=vusec/rangesanitizer)](https://github.com/vusec/rangesanitizer)
  
- [OLASan](https://www.computer.org/csdl/proceedings-article/icse/2025/056900a749/251mHpwGM3S) - Practical Object-Level Sanitizer with Aggregated Memory Access and Custom Allocator
  ![Conference](https://img.shields.io/badge/IEEE_ICSE-2025-blue)

- [Beyond Tag Collision](https://dl.acm.org/doi/10.1145/3719027.3765059) - Cluster-based memory management for tag-based sanitizers.
  ![Conference](https://img.shields.io/badge/ACM_CCS-2025-a0501b)
  [![Star](https://img.shields.io/github/stars/Yiruma96/ClusterTag-repo.svg?style=social&label=Yiruma96/ClusterTag-repo)](https://github.com/Yiruma96/ClusterTag-repo)

- [PSan](https://security.csl.toronto.edu/wp-content/uploads/2025/11/sxu_acsac2025_psan.pdf) - Hybrid metadata scheme for efficient pointer checking combining fat pointers and shadow memory.
  ![Conference](https://img.shields.io/badge/ACSAC-2025-1a85ff)

- [NanoTag](https://arxiv.org/abs/2509.22027) - Systems support for efficient byte-granular overflow detection on ARM MTE.
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2026-blue)
  [![Star](https://img.shields.io/github/stars/ice-rlab/nanotag.svg?style=social&label=ice-rlab/nanotag)](https://github.com/ice-rlab/nanotag)

- [FPN](https://www.ndss-symposium.org/ndss-paper/fast-pointer-nullification-for-use-after-free-prevention/) - Compiler-instrumented use-after-free prevention via fast pointer nullification at region-level metadata.
  ![Conference](https://img.shields.io/badge/NDSS-2026-lightblue)

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

- [DMARacer](https://dl.acm.org/doi/10.1145/3719027.3765126) - Dynamic detection of vulnerable DMA race conditions in Linux kernel drivers.
  ![Conference](https://img.shields.io/badge/ACM_CCS-2025-a0501b)
  [![Star](https://img.shields.io/github/stars/vusec/dmaracer.svg?style=social&label=vusec/dmaracer)](https://github.com/vusec/dmaracer)

- [HawkSet](https://dl.acm.org/doi/10.1145/3689031.3717477) - Automatic and efficient concurrent persistent memory bug detection via lockset analysis.
  ![Conference](https://img.shields.io/badge/ACM_EUROSYS-2025-green)

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

- [QMSan](https://hexhive.epfl.ch/publications/files/25NDSS3.pdf) - QMSan: Efficiently Detecting Uninitialized Memory Errors During Fuzzing
  ![Conference](https://img.shields.io/badge/NDSS-2025-lightblue)
  [![Star](https://img.shields.io/github/stars/heinzeen/qmsan.svg?style=social&label=heinzeen/qmsan)](https://github.com/heinzeen/qmsan)

- [Janitizer](https://dl.acm.org/doi/abs/10.1145/3696443.3708930) - Rethinking Binary Tools for Practical and Comprehensive Security
  ![Conference](https://img.shields.io/badge/CGO-2025-827429)

- [BSan](https://www.ndss-symposium.org/wp-content/uploads/ndss26-poster-91.pdf) - A Non-Intrusive and Comprehensive Binary-Level Memory Sanitizer
  ![Conference](https://img.shields.io/badge/NDSS_Poster-2026-lightblue)

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

- [T-PRUNIFY](https://www.usenix.org/system/files/usenixsecurity24-zhai.pdf) - Pruning redundant sanitizer checks by developer-implemented type checks.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2024-red)
  [![Star](https://img.shields.io/github/stars/seclab-ucr/TPrunify.svg?style=social&label=seclab-ucr/TPrunify)](https://github.com/seclab-ucr/TPrunify)

- [Type++](https://nebelwelt.net/publications/files/25NDSS.pdf) - Prohibiting type confusion with inline type information.
  ![Conference](https://img.shields.io/badge/NDSS-2025-lightblue)
  [![Star](https://img.shields.io/github/stars/HexHive/typepp.svg?style=social&label=HexHive/typepp)](https://github.com/HexHive/typepp)

- [Sourcerer](https://link.springer.com/chapter/10.1007/978-3-031-97620-9_5) - Channeling the void: precise type confusion detection covering void* casts.
  ![Conference](https://img.shields.io/badge/DIMVA-2025-7d3c98)
  [![Star](https://img.shields.io/github/stars/HexHive/Sourcerer.svg?style=social&label=HexHive/Sourcerer)](https://github.com/HexHive/Sourcerer)

### Dataflow Analysis

- [DataFlowSanitizer (Clang Documentation)](https://clang.llvm.org/docs/DataFlowSanitizer.html) - A general data flow analysis framework.

### Sanitizer Unification
- [CombiSan](https://download.vusec.net/papers/combisan_sec26.pdf) - Unifying Software Sanitizers for Comprehensive Fuzzing
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2026-red)
  [![Star](https://img.shields.io/github/stars/vusec/combisan.svg?style=social&label=vusec/combisan)](https://github.com/vusec/combisan)

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

- [LiteRSan](https://arxiv.org/abs/2509.16389) - Lightweight Memory Safety Via Rust-specific Program Analysis and Selective Instrumentation
  ![Conference](https://img.shields.io/badge/arxiv-2025-b31b1b)

- [SafeFFI](https://www.usenix.org/conference/usenixsecurity26/presentation/braunsdorf) - Efficient sanitization at the boundary between safe and unsafe code in Rust and mixed-language applications.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2026-red)

### Undefined Behavior

- [Miri](https://dl.acm.org/doi/10.1145/3776690) - Practical undefined behavior detection for Rust.
  ![Conference](https://img.shields.io/badge/ACM_POPL-2026-4a5568)
  [![Star](https://img.shields.io/github/stars/rust-lang/miri.svg?style=social&label=rust-lang/miri)](https://github.com/rust-lang/miri)

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

### Data Races and Others

- [iGUARD](https://dl.acm.org/doi/abs/10.1145/3477132.3483545) - In-GPU advanced race detection.
  ![Conference](https://img.shields.io/badge/ACM_SOSP-2021-177e25)
  [![Star](https://img.shields.io/github/stars/csl-iisc/iGUARD-SOSP21.svg?style=social&label=csl-iisc/iGUARD-SOSP21)](https://github.com/csl-iisc/iGUARD-SOSP21)

- [HiRace](https://dl.acm.org/doi/10.1109/SC41406.2024.00042) - Accurate and fast data race checking for GPU programs using source-code instrumentation.
  ![Conference](https://img.shields.io/badge/IEEE_SC-2024-blue)

- [GPUArmor](https://arxiv.org/abs/2502.17780) - Hardware-software co-design for efficient and scalable memory safety on GPUs.
  ![Conference](https://img.shields.io/badge/IEEE_ISCA-2025-336699)

- [RedSan](https://dl.acm.org/doi/full/10.1145/3712285.3759830) - A Redundant Memory Instruction Sanitizer for GPU Programs
  ![Conference](https://img.shields.io/badge/ACM_SC-2025-333)

- [SafeRace](https://dl.acm.org/doi/10.1145/3763075) - Assessing and addressing WebGPU memory safety in the presence of data races.
  ![Conference](https://img.shields.io/badge/ACM_OOPSLA-2025-d46b08)

- [TritonSan](http://github.com/microsoft/triton-shared/blob/main/triton-san/doc/triton-conf-2025-poster.pdf) - Toward Precise Debugging of Triton Kernels via LLVM Sanitizers
  ![Microsoft](https://img.shields.io/badge/Microsoft-f25022)
  [![Star](https://img.shields.io/github/stars/heinzeen/qmsan.svg?style=social&label=microsoft/triton-shared)](https://github.com/microsoft/triton-shared/blob/main/triton-san/README.md)

- [Triton-Sanitizer](https://dl.acm.org/doi/abs/10.1145/3779212.3790241) - A Fast and Device-Agnostic Memory Sanitizer for Triton with Rich Diagnostic Context
 ![Conference](https://img.shields.io/badge/ACM_ASPLOS-2026-9163aa)

- [SuperCollider](https://dl.acm.org/doi/10.1145/3808339) - Scalable and effective data race detection for CUDA programs.
  ![Conference](https://img.shields.io/badge/ACM_PLDI-2026-8c5a2c)

- [CuSafe](https://hongyi.lu/papers/cusafe-sec26.pdf) - Fast detection of memory safety vulnerabilities in CUDA programs.
  ![Conference](https://img.shields.io/badge/USENIX_SEC-2026-red)

---

## Miscellaneous

- [SoK: Sanitizing for security](https://ieeexplore.ieee.org/abstract/document/8835294)
  ![Conference](https://img.shields.io/badge/IEEE_S&P-2019-blue)

- [DySan](https://dl.acm.org/doi/abs/10.1145/3433210.3453095) - Dynamically sanitizing motion sensor data through adversarial networks.
  ![Conference](https://img.shields.io/badge/ACM_Asia_CCS-2021-a0501b)
  [![Star](https://img.shields.io/github/stars/DynamicSanitizer/DySan.svg?style=social&label=DynamicSanitizer/DySan)](https://github.com/DynamicSanitizer/DySan)

- [NeuralSanitizer](https://ieeexplore.ieee.org/abstract/document/10504286) - Detecting backdoors in neural networks.
  [![Transaction](https://img.shields.io/badge/IEEE_TIFS-2024-blue)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)
  [![Star](https://img.shields.io/github/stars/zhuhong1996/NeuralSanitizer.svg?style=social&label=zhuhong1996/NeuralSanitizer)](https://github.com/zhuhong1996/NeuralSanitizer)

- [UBfuzz](https://dl.acm.org/doi/10.1145/3617232.3624874) - Finding bugs in sanitizer implementations.
  ![Conference](https://img.shields.io/badge/ACM_ASPLOS-2024-9163aa)
  [![Star](https://img.shields.io/github/stars/shao-hua-li/UBGen.svg?style=social&label=shao-hua-li/UBGen)](https://github.com/shao-hua-li/UBGen)

- [WBSan](https://dl.acm.org/doi/abs/10.1145/3696410.3714622) - WebAssembly Bug Detection for Sanitization and Binary-Only Fuzzing
  [![Transaction](https://img.shields.io/badge/IEEE_WWW-2025-blue)](https://dl.acm.org/doi/proceedings/10.1145/3696410)

- [Optimal String Sanitization Against Strategic Attackers](https://ieeexplore.ieee.org/abstract/document/11173687)
  [![Transaction](https://img.shields.io/badge/IEEE_TIFS-2025-blue)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)

- [ProSan](https://ieeexplore.ieee.org/abstract/document/11352994) - Utility-Based Prompt Privacy Sanitizer
  [![Transaction](https://img.shields.io/badge/IEEE_TIFS-2026-blue)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)

---

## Contributing

Please refer to the guidelines at [contributing.md](https://github.com/junwha0511/awesome-sanitizer#contributing.md) for details.
