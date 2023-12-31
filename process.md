## Process
A process is a running program that serves as the foundation for all computation. The procedure is not the same as computer code, although it is very similar. In contrast to the program, which is often regarded as some ‘passive’ entity, a process is an ‘active’ entity. Hardware status, RAM, CPU, and other attributes are among the attributes held by the process.

A process is essentially running software. The execution of any process must occur in a specific order. A process refers to an entity that helps in representing the fundamental unit of work that must be implemented in any system.

In other words, we write the computer programs in the form of a text file, thus when we run them, these turn into processes that complete all of the duties specified in the program.

A program can be segregated into four pieces when put into memory to become a process: stack, heap, text, and data. The diagram below depicts a simplified representation of a process in the main memory.


### Components of a Process
It is divided into the following four sections:
 <img src="/images/process-in-operating-system.png"/>

- Stack
Temporary data like method or function parameters, return address, and local variables are stored in the process stack.

- Heap
This is the memory that is dynamically allocated to a process during its execution.

- Text
This comprises the contents present in the processor’s registers as well as the current activity reflected by the value of the program counter.

- Data
The global as well as static variables are included in this section.


### Process Life Cycle
When a process runs, it goes through many states. Distinct operating systems have different stages, and the names of these states are not standardised. In general, a process can be in one of the five states listed below at any given time.

- <b>Start</b>
When a process is started/created first, it is in this state.

- <b>Ready</b>
Here, the process is waiting for a processor to be assigned to it. Ready processes are waiting for the operating system to assign them a processor so that they can run. The process may enter this state after starting or while running, but the scheduler may interrupt it to assign the CPU to another process.

- <b>Running</b>
When the OS scheduler assigns a processor to a process, the process state gets set to running, and the processor executes the process instructions.

- <b>Waiting</b>
If a process needs to wait for any resource, such as for user input or for a file to become available, it enters the waiting state.

- <b>Terminated or Exit</b>
The process is relocated to the terminated state, where it waits for removal from the main memory once it has completed its execution or been terminated by the operating system.

 <img src="/images/process-in-operating-system1.png"/>

### Process Control Block (PCB)
Every process has a process control block, which is a data structure managed by the operating system. An integer process ID (or PID) is used to identify the PCB. As shown below, PCB stores all of the information required to maintain track of a process.

- <b>Process state</b>
The process’s present state, such as whether it’s ready, waiting, running, or whatever.

- <b>Process privileges</b>
This is required in order to grant or deny access to system resources.

- <b>Process ID</b>
Each process in the OS has its own unique identifier.

- <b>Pointer</b>
It refers to a pointer that points to the parent process.

- <b>Program counter</b>
The program counter refers to a pointer that points to the address of the process’s next instruction.

- <b>CPU registers</b>
Processes must be stored in various CPU registers for execution in the running state.

- <b>CPU scheduling information</b>
Process priority and additional scheduling information are required for the process to be scheduled.

- <b>Memory management information</b>
This includes information from the page table, memory limitations, and segment table, all of which are dependent on the amount of memory used by the OS.

- <b>Accounting information</b>
This comprises CPU use for process execution, time constraints, and execution ID, among other things.

- <b>IO status information</b>
This section includes a list of the process’s I/O devices.

 <img src="/images/process-in-operating-system2.png"/>
The PCB architecture is fully dependent on the operating system, and different operating systems may include different information. A simplified diagram of a PCB is shown below.



### The Different Process States
The operating system’s processes can be in one of the following states:

- NEW – The creation of the process.
- READY – The waiting for the process that is to be assigned to any processor.
- RUNNING – Execution of the instructions.
- WAITING – The waiting of the process for some event that is about to occur (like an I/O completion, a signal reception, etc.).
- TERMINATED – A process has completed execution.
 <img src="/images/process-in-operating-system3.png"/>

### Process vs Program
A program is a piece of code that can be as simple as a single line or as complex as millions of lines. A computer program is usually developed in a programming language by a programmer. The process, on the other hand, is essentially a representation of the computer program that is now running. It has a comparatively shorter lifetime.

Here is a basic program created in the C programming language as an example:

```
#include <stdio.h>

int main() {

printf(“Hi, Ramesh! \n”);

return 0;

}

```
A computer program refers to a set of instructions that, when executed by a computer, perform a certain purpose. We can deduce that a process refers to a dynamic instance of a computer program when we compare a program to a process. An algorithm is an element of a computer program that performs a certain task. A software package is a collection of computer programs, libraries, and related data.
