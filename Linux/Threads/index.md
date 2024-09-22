- https://stackoverflow.com/questions/5593328/software-threads-vs-hardware-threads
- https://thinkty.net/general/2021/05/03/threads.html

![image_2022_09_06T07_11_14_096Z](https://github.com/user-attachments/assets/7adb4554-a5bc-489d-86e0-890e7fee2c10)

If run to many software threads https://stackoverflow.com/questions/44169993/what-happens-if-you-start-too-many-threads

# Hyper-threading
https://en.wikipedia.org/wiki/Hyper-threading

One physical core is treated as 2 logical cores (each has its own hardware **(logical?)** thread).

## With Hyper-threading, do logical cores work simultaneously or concurrently? 

![image](https://github.com/user-attachments/assets/9a84b45c-9328-4acc-9002-4ff508246e4d)

With **Hyper-Threading** (HT), **logical cores** (also called **threads**) work **concurrently**, not simultaneously. Here's the distinction:

### Hyper-Threading Overview:
**Hyper-Threading** is Intel's technology that allows a single physical CPU core to appear as two **logical cores** to the operating system. The idea is that each physical core can handle **two independent instruction streams** (threads) simultaneously, taking better advantage of underused resources within the core.

### Concurrent vs. Simultaneous Execution:

1. **Concurrent Execution**:
   - **Logical cores** in a hyper-threaded system operate **concurrently**, meaning they share the same physical core and execute instructions **interleaved** with each other. They don’t run completely in parallel because they must share certain core resources (e.g., execution units, caches).
   - When one logical core is stalled (e.g., waiting for data from memory), the other logical core can take advantage of the idle resources. This makes the system more efficient by keeping the CPU busy, but both threads are not fully independent and must share the execution resources of the physical core.

2. **Simultaneous Execution**:
   - **Simultaneous execution** means that two or more operations are being executed **at the exact same time**. Hyper-Threading doesn’t provide true simultaneous execution of threads because the two logical cores are sharing the same physical core. Some parts of their execution overlap, but they’re not completely independent.
   - True simultaneous execution happens on **physical cores** that run independently, whereas with Hyper-Threading, the logical cores must cooperate and share resources.

### How Hyper-Threading Works:

- When a physical core has unused resources (such as execution units), it can execute instructions from a second thread in the gaps. This improves efficiency by using idle parts of the CPU, but both logical cores are still **competing** for the same physical resources.
- For example, if one thread is waiting for memory access, the other thread can utilize the CPU's execution units, making the overall core utilization higher.
  
### Summary:
- **Logical cores** with Hyper-Threading operate **concurrently**, sharing the resources of a single physical core.
- They do not run completely **simultaneously**, as they must share certain parts of the CPU core, like the execution units, so their execution is interleaved.
- While they give the appearance of doubling the number of cores, the actual performance improvement depends on how well the system can utilize the physical core's shared resources.

## Does a Hyper-Threaded physical core have an own thread?

![image](https://github.com/user-attachments/assets/2c7b1581-ffd4-4016-bd69-9886b3b39d76)

A **Hyper-Threaded physical core** does **not** have its own dedicated thread. Instead, it can execute **two threads (logical cores)** concurrently by sharing the core's resources between them. Here's a breakdown of how it works:

### Key Points:

1. **No Dedicated Thread for Physical Core**:
   - In a **Hyper-Threaded core**, there are no "physical core-only" threads. Instead, the core has two **logical cores (threads)** that are treated equally by the CPU's hardware. Both threads share the physical core's resources, such as the execution units, caches, and memory access. 

2. **Sharing Resources**:
   - A single physical core with Hyper-Threading can process instructions from **two separate threads** concurrently. These threads **share** the core's execution resources. If one thread stalls or doesn't fully use the core’s resources, the other thread can utilize the idle capacity.

3. **Logical Cores (Threads)**:
   - **Logical cores** represent the two threads that the operating system sees when Hyper-Threading is enabled. The operating system schedules processes on these logical cores as if they were independent cores, even though they are actually sharing the same physical core's resources.

### How Hyper-Threading Works:
- A **physical core** in a Hyper-Threaded CPU is designed to execute **two independent threads** (logical cores) that share the core's physical resources.
- These logical cores allow the operating system to schedule tasks as if there are more cores available (doubling the number of threads per core).
- The core switches between these threads when resources are available, increasing efficiency by filling in idle cycles.

### Summary:
A Hyper-Threaded physical core doesn't have its own dedicated thread. Instead, it manages **two logical threads** that share its resources, improving CPU utilization but not providing true parallelism like having additional physical cores would.
