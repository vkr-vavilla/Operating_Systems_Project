# 🧠 xv6-Based Operating System Extensions

> ⚙️ Developed as part of the Operating Systems course at UTA (CS 3320)  
> 🔐 Designed with Embedded Systems in mind


---

## 📌 Overview

This project is a complete extension of the [xv6](https://pdos.csail.mit.edu/6.828/2018/xv6.html) teaching operating system, restructured and enhanced to simulate real-world OS behaviors. Through intensive low-level C and x86 assembly work, I added new kernel features, improved system performance, and enforced memory and process security boundaries. The project is a direct reflection of my interest and growing experience in **Embedded Systems**, **Operating Systems Internals**, and **Secure System Design**.

---

## 🧩 Key Features

### 🔧 System Call Design & Security
- Implemented secure custom system calls: `shmget`, `shmdel`, and others.
- Added syscall validation and filtering mechanisms to prevent misuse.
- Wrote low-level assembly stubs for syscall entry points (`usys.S`).

### 🧠 Shared Memory & Page Management
- Created shared memory APIs for inter-process communication (IPC).
- Integrated reference counting into the kernel’s page allocator.
- Enhanced physical memory tracking to prevent leaks and access violations.

### 📦 Buffer Cache Synchronization
- Built a spinlock-based buffer cache system in `bio.c`.
- Applied `sleep()`/`wakeup()` for I/O blocking and safe disk access.
- Reduced I/O overhead by caching frequently accessed disk blocks.

### ⚙️ Process Control Mechanisms
- Extended process lifecycle: `fork`, `exec`, `wait`, `kill`, and zombie cleanup.
- Added debugging tools to trace process creation and destruction in real time.

### 🧪 Custom Shell & Userland Utilities
- Developed a custom user shell (`_sh`) and tools like `_ls`, `_cat`, `_echo`.
- Linked all user programs with system call wrappers and compiled with xv6’s user-level toolchain.

---

## 💡 Skills & Technologies Gained

| Domain              | Skills/Technologies                                                                 |
|---------------------|-------------------------------------------------------------------------------------|
| **Languages**        | C, x86 Assembly                                                                    |
| **OS Concepts**      | System Calls, Memory Management, Process Scheduling, Filesystems                   |
| **Embedded Systems** | QEMU Simulation, Virtual Boot Environments, Direct Memory Access                   |
| **Cybersecurity**    | Privilege Separation, Syscall Sanitization, Race Condition Avoidance               |
| **Tools**            | QEMU, Bochs, GDB, Make, GCC Toolchain, Git                                          |
| **Debugging**        | Printk Tracing, Stack Walks, Breakpoint Debugging in Assembly and C                |

---

## 📂 Directory Structure

```bash
📁 xv6-operating-systems-project/
├── bio.c            # Buffer cache logic with spinlocks
├── syscall.c/h      # System call implementations and definitions
├── user.h           # User-visible syscall declarations
├── usys.S           # Assembly syscall stubs
├── _sh, _ls, _cat   # Custom user programs (shell, utilities)
├── Makefile         # Build script for OS and userland
└── README.md        # Project documentation (this file)
```

---

## 🛠️ How to Build & Run

> Requires QEMU and an x86 GCC cross-compiler

```bash
# Clone this repository
git clone https://github.com/yourusername/xv6-operating-systems-project.git
cd xv6-operating-systems-project

# Build the kernel and user programs
make

# Run in QEMU virtual machine
make qemu

# Optionally, run in Bochs
make bochs
```

---

## 📚 What I Learned

- 🧠 Deep understanding of user/kernel separation and syscall handling
- 💻 Secure, low-level memory and buffer management
- 🔒 Defense-in-depth coding practices and attack surface reduction
- 🧪 Debugging kernel panics, stack overflows, and illegal memory access
- ⚙️ Realistic OS simulation with process and I/O scheduling in xv6

---

## 💼 Why This Matters

This project is an academic but practical replication of tasks performed in embedded and systems-level roles. It gave me real hands-on experience working near the hardware, optimizing low-level performance, and securing critical kernel resources.

**Highlights for Employers:**
- Experience writing memory-safe C and system-level Assembly code
- Proven ability to debug and extend a Unix-style kernel
- Comfort working with QEMU, virtual machines, and cross-compilation
- Cybersecurity-aware development practices at the OS level

---

## 👨‍💻 About Me

**Vamshi Vavilla**  
🎓 Computer Engineering | Minors: Cybersecurity, Mathematics, and Physics  
🔗 [LinkedIn](https://www.linkedin.com/in/yourprofile)  
📧 vamshivavilla@email.com  

---

## 🤝 Let’s Connect

I am currently seeking **internship** or **full-time opportunities** in:

- 🛠️ Embedded Systems Development  
- 🧠 Operating Systems Engineering  
- 🔐 Security Research and Kernel Development  

If you're looking for a developer who loves working close to the hardware, solving real systems problems, and writing secure low-level code—I'd love to chat.

---

> “Working with xv6 taught me that understanding the kernel means understanding the machine.”  
> — Vamshi Vavilla
