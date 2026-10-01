### 5. LSB (Linux Standard Base)
Maintained by the **Linux Foundation**. It reduces deviations between individual Linux distributions by standardizing the binary execution environment, application binary interfaces (ABI), and foundational system libraries.

* **Application Binary Interface (ABI):** Ensures that compiled binaries can execute across compliant distributions without requiring source-code recompilation.
* **Component Standardization:** Maps out expected system libraries (like glibc, PAM, and ncurses) and commands that software developers can safely rely on.
* **System Initialization:** Traditionally standardized system init script behaviors and runtime runlevels (`/etc/init.d/`).
* **Latest Source:** [Linux Foundation Reference Specifications Portal](https://linuxfoundation.org).

---

### 6. ELF (Executable and Linkable Format)
Originally developed by the Unix System Laboratories (USL) and maintained as part of the **Tool Interface Standard (TIS)**. It serves as the standard binary format for executables, object code, shared libraries, and core dumps on Linux and Unix-like operating systems.

* **Linking vs. Execution:** Program headers guide the OS loader for execution, while section headers are strictly used by linkers (`ld`) and debuggers (`gdb`).
* **Cross-Platform Adoptability:** Serves as the flexible, standard object structure across completely different hardware ISAs (x86_64, ARM, RISC-V).
* **Dynamic Loading:** Standardizes how the dynamic linker (`ld.so`) locates and maps symbols from shared objects (`.so` files) into a running process.
* **Latest Source:** [TIS ELF Specification Version 1.2 Manual](https://linuxfoundation.orgelf/elf.pdf).

---

### 7. Wayland Display Server Protocol
Governed by the **Freedesktop.org** community. This modern architectural specification dictates how a compositor talks to its clients and manages screen rendering without unnecessary middleware overhead.

* **Direct Compositing:** Merges the display server and the window manager into a single process (the compositor) to eliminate screen tearing.
* **Client Window Isolation:** Enforces strict execution boundaries so applications cannot log keystrokes or record pixels from other application windows natively.
* **Buffer Management:** Passes shared memory handles (`dmabuf`) directly between the client application, compositor, and the Linux kernel DRM layer.
* **Latest Source:** [The Wayland Protocol Reference Manual](https://freedesktop.org).

---

### 8. X11 Core Protocol Specification
Maintained by the **X.Org Foundation**. This legacy graphics protocol defines a network-transparent windowing system used heavily across historical Unix and classic Linux system architectures.

* **Network Transparency:** Built on a classic client-server model allowing an application running on a remote server to render its UI across a local machine display.
* **Separated Window Managers:** Keeps the core display server completely agnostic of decoration styles, offloading management to external clients (e.g., i3, Openbox).
* **Extensible Core API:** Uses historical extension frameworks (like XRender or GLX) to inject 2D and 3D graphics support over the old baseline server code.
* **Latest Source:** [X Window System Core Protocol Specification](https://x.org).
