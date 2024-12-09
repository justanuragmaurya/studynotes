# File Management

## File Concepts

- **Files**: 
  - **Definition**: Organized collections of data, stored in storage devices, managed by the OS.
  - **Attributes**: 
    - **Name**: Identifies the file in the system.
    - **Type**: Indicates the kind of file (e.g., text, binary, executable).
    - **Location**: Path where the file resides in the file system.
    - **Size**: The amount of space the file occupies.
    - **Protection**: Access rights or permissions.
    - **Time**: Creation time, last modification, last access.

- **File Structure**:
  - **Unstructured (Byte Sequence)**: Simpler, used for text files, binaries.
  - **Structured**: Organized into records, fields for databases or specific applications.

- **Operations on Files**:
  - **Create**: Allocate space, initialize attributes.
  - **Open**: Load file into memory for access.
  - **Read/Write**: Perform I/O operations.
  - **Reposition**: Move the file pointer (seek).
  - **Close**: Flush buffers, update attributes, release locks.
  - **Delete**: Free up space, remove directory entry.

## Access Methods

- **Sequential Access**:
  - **Operation**: Read/write data in order from start to end.
  - **Use Cases**: Suitable for tapes and logs.

- **Direct (Random) Access**:
  - **Operation**: Access any record directly by its position or key.
  - **Use Cases**: Essential for databases, large data sets where random access is frequent.

- **Indexed Access**:
  - **Operation**: Use an index table to locate data quickly.
  - **Advantages**: Improves access speed for large files.

## Directory Structure

- **Single-Level Directory**: All files are in one directory; simple but not scalable.
- **Two-Level Directory**: User directories with a common root; better organization.
- **Tree-Structured Directory**: Hierarchical, supports subdirectories, widely used in modern systems.
- **Acyclic-Graph Directory**: Allows shared subdirectories, useful for sharing files.

## File System Mounting and Sharing

- **Mounting**:
  - **Process**: Attaching a file system to the current file name space at a mount point.
  - **Example**: Mounting a USB drive to `/mnt/usb`.

- **Sharing**:
  - **Network File System (NFS)**: Allows remote file access over a network.
  - **SMB/CIFS**: Common in Windows environments for sharing files.

## Protection

- **Access Control Lists (ACLs)**:
  - **Function**: Define permissions for users or groups for each file or directory.

- **User-Based Permissions**: Owner, Group, Others with read/write/execute rights.

- **Capabilities**: Secure tokens that can grant or deny access to system resources.

## Allocation Methods

- **Contiguous Allocation**: 
  - **Pros**: Simple, fast access.
  - **Cons**: External fragmentation, difficult to grow files.

- **Linked Allocation**:
  - **Pros**: No external fragmentation, easy file growth.
  - **Cons**: Inefficient for direct access, extra space for pointers.

- **Indexed Allocation**:
  - **Pros**: Direct access to blocks via index, no external fragmentation.
  - **Cons**: Space overhead for the index.

## Free-Space Management

- **Bit Vector**: Each bit represents a block; 0 for free, 1 for used.
- **Linked List**: Free blocks linked together, only the first block needs to be known.
- **Grouping**: A block contains N free block numbers followed by M pointers to more blocks.

## Directory Implementation

- **Linear List**: Each entry in the directory points to file metadata.
- **Hash Table**: For faster lookup, but requires collision handling.
- **Balanced Tree**: Efficient for very large directories.

# Device Management

## Types of Devices

- **Dedicated Devices**: Exclusive use by one process at a time (e.g., some printers).
- **Shared Devices**: Can serve multiple processes (e.g., network cards).
- **Virtual Devices**: Logical devices which map to physical hardware (e.g., virtual memory).

## Access Methods

- **Serial Access**: Data accessed sequentially, like magnetic tapes.
- **Direct Access**: Random access to data, typical for hard drives.

## Disk Scheduling Methods

- **FCFS**: First process to request is served first; simple but potentially inefficient.
- **SSTF**: Serve the request closest to the current head position; reduces seek times but can lead to starvation.
- **SCAN**: Elevator algorithm; head moves to one end, servicing requests, then reverses.
- **C-SCAN**: Like SCAN but only serves requests in one direction, then jumps back to the start.

## Direct Access Storage Devices (DASD)

- **Channels**: Pathways for data transfer between device and memory.
- **Control Units**: Manages device operations, error correction, and command execution.

# Inter-Process Communication (IPC)

## Introduction to IPC

- **Purpose**: Allow processes to exchange data, synchronize actions.

## Pipes

- **Named Pipes**: Persist in the file system, allowing unrelated processes to communicate.
- **Unnamed Pipes**: For related processes, typically parent-child.

  - **Functions**:
    - `popen()`: Opens a process by creating a pipe, fork, and exec.
    - `pclose()`: Closes the pipe and waits for the associated process to terminate.

## Shared Memory

- **Concept**: A memory region shared between processes for fast communication.
- **Implementation**: Requires synchronization mechanisms to prevent race conditions.

## FIFOs (First In First Out)

- **Usage**: Similar to named pipes but stored in the file system, allowing inter-process communication even if processes are not related.

## Message Queues

- **Mechanism**: Allows processes to send messages to a queue from which others can retrieve them.
- **Advantages**: Control over message sequence, can be used for broadcast communication.

  - **Operations**:
    - **Send**: Add messages to the queue.
    - **Receive**: Retrieve messages, with options for blocking or non-blocking calls.

These notes provide a comprehensive overview suitable for students or professionals studying or working in system administration, computer science, or related fields. Each topic includes practical considerations and potential use cases to understand their application in real-world scenarios.
