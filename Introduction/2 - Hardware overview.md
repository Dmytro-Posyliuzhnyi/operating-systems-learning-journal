
To understand how an operating system (OS) works, it's important to first understand the internals of the computer hardware it interacts with.

---

## What is a CPU?

- **CPU (Central Processing Unit)**: The brain of the computer.
- Handles all the **processing tasks** — essentially, it runs programs and makes things work.
- Executes tasks in a cycle:
  1. **Fetch**: Takes an instruction from memory.
  2. **Decode**: Figures out what the instruction means.
  3. **Execute**: Performs the task (e.g., calculations or controlling hardware).
  4. **Repeat**: Moves to the next instruction and starts again.
- Key jobs of the CPU:
  - **Arithmetic/Logic operations**: Performs calculations and comparisons.
  - **Control tasks**: Decides what gets done and in what order.
- Without the CPU, the computer is just a box of parts doing nothing.

## CPU Cores

- A **core** is an independent processing unit within the CPU.
- Each core can:
  - **Fetch**, **decode**, and **execute** instructions on its own.
  - Run a separate thread independently of other cores.
- **Multi-core CPUs** (e.g., dual-core, quad-core) can handle multiple threads simultaneously, providing true parallelism rather than just time-sharing.
- More cores generally mean:
  - **Better multitasking**: Multiple tasks can be processed in parallel.
  - **Improved performance on parallelizable workloads**: Tasks like video editing or gaming can split work across cores.
  - **Energy efficiency**: Several cores running at moderate speeds can be more power-efficient than a single, fast-running core.

## Threads

- A **thread** is a single sequence of instructions executed by the CPU.
- In single-core CPUs: Only one thread runs at a time, but the CPU switches between threads so fast (in nanoseconds) that it feels like multitasking (**time-sharing**).
- In multi-core CPUs: Each core can run one thread independently, enabling **true multitasking**.
- With technologies like **Hyper-Threading** (on Intel CPUs), a single core can handle multiple hardware threads simultaneously, further improving throughput.

### Key Points About Multithreading

- **Multithreading** does **not ensure true concurrency**:
  - Only one thread per core can run at the exact same instant.
  - When fewer cores than threads are available, the CPU switches between threads quickly, creating the illusion of simultaneous execution.

## What is Context Switching?

- **Context switching** is when the CPU pauses one thread, saves its state, and switches to another thread.
- It allows multitasking but comes with overhead:
  - **Performance cost**: Time is spent saving and loading thread states.
  - **Memory overhead**: Thread states must be stored and retrieved from memory during each switch.
