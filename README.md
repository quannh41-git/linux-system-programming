# linux-system-programming

## 1.System programming concepts
- A system call can be considered as an interface through which the user application code enters kernel mode
- System call can be invoked from user app in 2 ways
  - Directly calling the system call
  - The user code calls the library function and this calls corresponding system call

- Example: System call working
  
|USER MODE|KERNEL MODE|
|:-------:|:---------:|
|1.write()||
|2.Standard lib wrapper for write() - libc/glibc||
||3.Interrupt handler start - system call table call sys_write()|
||4.Interrupt handler end|
||5.Interrupt handler return to user space|
|6.libc/glibc return write() to user code||

## 2.File Operations
## 3. Advanced I/O
- Race condition
- Atomicity is a condition in which the code is written in such a way that code cannot be run by other process/thread at the same time while it is being executed/running by first process/thread
- All system calls in Linux are executed atomically. By this, we mean that the kernel guarantees that all of the steps in a system call are completed as a single operation.
## 4.Intro to Process
## 5.Virtual Memory of Process
## 6.Memory Allocation
## 7.Process Programming
## 8.Process Monitor
## 9.Advanced Process Programming
## 10.Signals
## 11.Threads
## 12.Thread synchronisation
## 13.IPC
## 14.PIPES and FIFO - Inter Process Communication
## 15.POSIX - Message Queue
## 16.Semaphore
## 17.Shared memory