# Operating Systems Notes

## What is an Operating System (OS)?

- The OS is kind of a **layer of abstraction** between the user/programs and the hardware. It simplifies the complexity of hardware, allowing programmers and users to interact with the system without knowing hardware-level details.
- **Primary Goals of the OS:**
  1. **Create abstractions** for hardware resources.
  2. **Implement and manage these abstractions.**
- Programs are the real "users" of the OS, as they leverage its abstractions to perform tasks.

<img width="700" alt="Page 1" src="https://github.com/user-attachments/assets/6e175c9b-2eb2-41db-b89a-579cdc293b3c">

---

## Operating System as a Resource Manager

One of the goals of the operating system is to efficiently manage resources. This is done using two key strategies:

### 1. Time Multiplexing
- Different programs use a resource (e.g., CPU) one after another in a rapid sequence.
- **Example:** A single processor runs one program for a short time, then switches to another. This happens so fast that users perceive all programs as running simultaneously.

### 2. Space Multiplexing
- A resource (e.g., memory) is divided into smaller chunks, and each program gets its own share simultaneously.
- **Example:** RAM is divided among active applications, with each program using its allocated portion at the same time.

---

## CPU and Multiplexing
- A single processor can perform only **one task at a specific time**.
- The OS uses **time slicing** to switch between tasks quickly, creating the illusion of multitasking.
- **Multiple processors or cores** increase performance because each processor can handle a different task independently.

---

## RAM and Space Sharing
- RAM is a shared resource. Programs get portions of the total available RAM dynamically.
- **Example:** In a system with 16 GB of RAM and 8 running programs, the OS allocates memory to each program based on its needs, not necessarily evenly.
- **Key OS Responsibilities:**
  1. Ensures each program has its own allocated memory space (**memory isolation**).
  2. Allows programs to coexist in memory simultaneously to support multitasking.

---
