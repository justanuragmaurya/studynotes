# Unit I: Introduction to Operating System and Process Management

## **1.1 Introduction to Operating System**

### **Operating System Meaning**
- **Definition**: Software that manages hardware resources and provides common services for computer programs.
- **Role**: Acts as an intermediary between hardware and user programs, managing system resources.

### **Supervisor & User Mode**
- **Supervisor Mode**: Also known as kernel mode, allows unrestricted access to hardware, privileged instructions.
- **User Mode**: Restricted; cannot execute privileged instructions, must request OS services via system calls.

### **Multiprogramming and Multiprocessing System**
- **Multiprogramming**: Allows multiple programs to run concurrently on a single CPU, increasing CPU utilization through context switching.
- **Multiprocessing**: Utilizes multiple CPUs or cores to execute multiple processes simultaneously, enhancing system throughput.

### **OS Structure**
- **Monolithic**: All OS services run as a single program in kernel space.
- **Layered**: OS is divided into layers, each building on the one below, with the kernel at the bottom.
- **Microkernel**: Only essential functions in kernel space; other services in user space for modularity.

### **System Calls**
- **Definition**: Interface between user programs and the OS, allowing programs to request services from the kernel.
- **Examples**: Process control, file management, device management, information maintenance.

### **Functions of OS**
- **Resource Management**: CPU, memory, I/O devices, file systems.
- **Process Management**: Process creation, scheduling, termination.
- **Security and Protection**: Ensuring safe interaction among processes and with hardware.
- **Error Detection and Response**: Handling system faults gracefully.

### **Evolution of OSs**
- **Batch Systems**: Early systems where jobs were batched for efficiency.
- **Interactive Systems**: With time-sharing, allowing multiple users to interact with the computer simultaneously.
- **Distributed Systems**: Sharing resources across multiple computer systems.
- **Real-Time Systems**: OS designed to serve real-time applications with stringent time constraints.

## **1.2 Process Management**

### **Process States**
- **New**: Process being created.
- **Ready**: Process waiting to be assigned to a processor.
- **Running**: Instructions being executed.
- **Waiting**: Waiting for some event or resource.
- **Terminated**: Process has finished execution.

### **Operations on Processes**
- **Creation**: Starts a new process, allocating resources.
- **Scheduling**: Determining which process runs next.
- **Synchronization**: Coordinating processes to prevent race conditions.
- **Communication**: Exchanging data between processes via IPC mechanisms.
- **Termination**: Freeing resources allocated to the process.

### **Process Management in UNIX**
- **Fork**: Creates a child process by duplicating the calling process.
- **Exec**: Replaces the calling process's memory with a new program.
- **Wait**: Parent waits for child process to terminate.

### **Process Control Block (PCB)**
- **Structure**: Contains information about the process state, program counter, CPU registers, memory management info, etc.
- **Purpose**: Facilitates context switching, keeping track of process state.

### **Process Concept**
- **Definition**: A program in execution; a unit of work within the system.
- **Attributes**: Process ID, state, program counter, registers, memory pointers.

### **Life Cycle of a Process**
- **States Transition**: From New to Ready, Ready to Running, Running to Waiting, back to Ready or Terminated.

### **PCB - Process Control Block**
- **Details**: Includes process state, program counter, CPU registers, CPU-scheduling information, memory-management information, accounting information, I/O status information.

### **Operations on Processes**
- **Creation**: Parent process creates children.
- **Interruption**: Signals or events causing a process to stop.
- **Execution**: Process runs on the CPU.
- **Suspension**: Process temporarily stops, commonly for I/O or waiting for resources.

### **Co-operating and Independent Processes**
- **Independent**: Executes independently without affecting or being affected by other processes.
- **Co-operating**: Processes that can affect or be affected by other processes, typically through shared memory or message passing.

### **Key Takeaways**
- The operating system's primary role is to manage hardware resources, abstracting them for ease of use by user programs.
- Process management is central to OS functionality, dealing with process lifecycle, scheduling, and resource allocation.
- Understanding the difference between supervisor and user mode is crucial for security and system stability.
- System calls bridge the gap between user-level applications and kernel-level operations, ensuring secure and controlled access to system resources.

## **References**
- **"Operating System Concepts" by Abraham Silberschatz, Peter B. Galvin, Greg Gagne** - For detailed theoretical and practical insights on OS functionality and process management.

This completes the comprehensive notes for Unit I. Ensure you understand these concepts well, as they form the foundation for all subsequent units in the course.
