# OS Standards Quick Reference Index

A curated index summarizing the core engineering standards that dictate directory layouts, application configuration, and API specifications across Unix-like and Linux platforms.

---

## 🗂️ Core Standards Index

| Standard | Governing Body | Primary Focus | Official Specification Link |
| :--- | :--- | :--- | :--- |
| **POSIX.1-2024** | IEEE & The Open Group | OS C APIs, Shell, and Core Utilities | [The Open Group Base Specs (Issue 8)](https://opengroup.org) |
| **FHS 3.0** | Linux Foundation | Global system storage layout guidelines | [Linux Foundation FHS Reference](https://linuxfoundation.org) |
| **XDG Base Directory** | Freedesktop.org | User-space configuration & cache locations | [Freedesktop XDG Specification](https://freedesktop.org) |
| **Linux Kernel API** | Linux Kernel Org | System calls, user-space headers, ABI stability | [Linux Kernel Documentation](https://kernel.org) |

---

## 📑 Detailed Summaries

### 1. POSIX (Portable Operating System Interface)
Maintained by the **Austin Group** (a joint technical working group between the IEEE, ISO/IEC, and The Open Group). It ensures source-code portability across various distributions of Unix and Unix-like environments.

* **Base Definitions:** Defines fundamental core concepts, formatting conventions, and standard C header file structures.
* **System Interfaces:** Documents execution models, threading (pthreads), and exact C programming language function signatures.
* **Shell & Utilities:** Outlines the strict syntax rules for the command execution shell and basic system command behavior.
* **Latest Source:** [POSIX.1-2024 (Issue 8) Online Publication](https://opengroup.org).

### 2. FHS (Filesystem Hierarchy Standard)
Maintained by the **Linux Foundation**. It governs the uniform layout, naming schema, and usage rules of all files and directory trees under the root (`/`) system namespace.

* **Static vs Variable Data:** Strictly isolates static, shareable read-only binaries (`/usr`) from dynamic, machine-specific runtime files (`/var`).
* **Essential Binaries:** Dictates the boundary responsibilities between critical recovery commands (`/bin` or `/sbin`) and general system utilities.
* **Latest Source:** [FHS 3.0 Full Text Manual](https://linuxfoundation.org).

### 3. XDG Base Directory Specification
Maintained by **Freedesktop.org**. It prevents arbitrary cluttering of the root user directory (`$HOME`) by defining designated, program-accessible workspace paths.

* `$XDG_CONFIG_HOME`: Dedicated user settings folder (Defaults to `$HOME/.config`).
* `$XDG_CACHE_HOME`: Non-essential application data buffer (Defaults to `$HOME/.cache`).
* `$XDG_DATA_HOME`: Architecture-independent user-specific operational scripts (Defaults to `$HOME/.local/share`).
* `$XDG_STATE_HOME`: Persistent status files like history and logs (Defaults to `$HOME/.local/state`).
* **Latest Source:** [Freedesktop XDG Base Directory Specification](https://freedesktop.org).

### 4. Linux Kernel API & System Call Interface
Maintained by the **Linux Kernel Community**. It outlines the strict separation boundary and execution pathways between user programs and direct kernel privileges.

* **Syscall Interface:** Standardizes how programs switch into kernel space to request system resources (memory, hardware, network).
* **POSIX Variations:** Documents where the Linux kernel mirrors standard POSIX compliance and where it provides highly optimized extensions (such as `epoll` or `io_uring`).
* **Latest Source:** [Linux Kernel User-Space API Guide](https://kernel.orguserspace-api/index.html).
