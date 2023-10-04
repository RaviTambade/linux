## Process
A process is a running program that serves as the foundation for all computation. The procedure is not the same as computer code, although it is very similar. In contrast to the program, which is often regarded as some ‘passive’ entity, a process is an ‘active’ entity. Hardware status, RAM, CPU, and other attributes are among the attributes held by the process.

A process is essentially running software. The execution of any process must occur in a specific order. A process refers to an entity that helps in representing the fundamental unit of work that must be implemented in any system.

In other words, we write the computer programs in the form of a text file, thus when we run them, these turn into processes that complete all of the duties specified in the program.

A program can be segregated into four pieces when put into memory to become a process: stack, heap, text, and data. The diagram below depicts a simplified representation of a process in the main memory.


Components of a Process
It is divided into the following four sections:
 <img src="/images/process-in-operating-system.png"/>
tack
Temporary data like method or function parameters, return address, and local variables are stored in the process stack.

Heap
This is the memory that is dynamically allocated to a process during its execution.

Text
This comprises the contents present in the processor’s registers as well as the current activity reflected by the value of the program counter.

Data
The global as well as static variables are included in this section.


Process Life Cycle
When a process runs, it goes through many states. Distinct operating systems have different stages, and the names of these states are not standardised. In general, a process can be in one of the five states listed below at any given time.

Start
When a process is started/created first, it is in this state.

Ready
Here, the process is waiting for a processor to be assigned to it. Ready processes are waiting for the operating system to assign them a processor so that they can run. The process may enter this state after starting or while running, but the scheduler may interrupt it to assign the CPU to another process.

Running
When the OS scheduler assigns a processor to a process, the process state gets set to running, and the processor executes the process instructions.

Waiting
If a process needs to wait for any resource, such as for user input or for a file to become available, it enters the waiting state.

Terminated or Exit
The process is relocated to the terminated state, where it waits for removal from the main memory once it has completed its execution or been terminated by the operating system.

 <img src="/images/process-in-operating-system1.png"/>

### Process Control Block (PCB)
Every process has a process control block, which is a data structure managed by the operating system. An integer process ID (or PID) is used to identify the PCB. As shown below, PCB stores all of the information required to maintain track of a process.

- Process state
The process’s present state, such as whether it’s ready, waiting, running, or whatever.

- Process privileges
This is required in order to grant or deny access to system resources.

- Process ID
Each process in the OS has its own unique identifier.

- Pointer
It refers to a pointer that points to the parent process.

- Program counter
The program counter refers to a pointer that points to the address of the process’s next instruction.

- CPU registers
Processes must be stored in various CPU registers for execution in the running state.

- CPU scheduling information
Process priority and additional scheduling information are required for the process to be scheduled.

- Memory management information
This includes information from the page table, memory limitations, and segment table, all of which are dependent on the amount of memory used by the OS.

- Accounting information
This comprises CPU use for process execution, time constraints, and execution ID, among other things.

- IO status information
This section includes a list of the process’s I/O devices.

 <img src="/images/process-in-operating-system2.png"/>
The PCB architecture is fully dependent on the operating system, and different operating systems may include different information. A simplified diagram of a PCB is shown below.



### The Different Process States
The operating system’s processes can be in one of the following states:

NEW – The creation of the process.
READY – The waiting for the process that is to be assigned to any processor.
RUNNING – Execution of the instructions.
WAITING – The waiting of the process for some event that is about to occur (like an I/O completion, a signal reception, etc.).
TERMINATED – A process has completed execution.
 <img src="/images/process-in-operating-system3.png"/>

### Process vs Program
A program is a piece of code that can be as simple as a single line or as complex as millions of lines. A computer program is usually developed in a programming language by a programmer. The process, on the other hand, is essentially a representation of the computer program that is now running. It has a comparatively shorter lifetime.

Here is a basic program created in the C programming language as an example:

#include <stdio.h>

int main() {

printf(“Hi, Subhadip! \n”);

return 0;

}

A computer program refers to a set of instructions that, when executed by a computer, perform a certain purpose. We can deduce that a process refers to a dynamic instance of a computer program when we compare a program to a process. An algorithm is an element of a computer program that performs a certain task. A software package is a collection of computer programs, libraries, and related data.

### Process Scheduling
When there are several or more runnable processes, the operating system chooses which one to run first; this is known as process scheduling.

A scheduler is a program that uses a scheduling algorithm to make choices. The following are characteristics of a good scheduling algorithm:

- For users, response time should be kept to a bare minimum.
- The total number of jobs processed every hour should be as high as possible, implying that a good scheduling system should provide the highest possible throughput.
- The CPU should be used to its full potential.
- Each process should be given an equal amount of CPU time.



## What is Preemptive Scheduling?
Preemptive Scheduling is a technique where the assignments are allotted with their preferences or priorities. In the case of preemptive scheduling, it is crucial to execute a higher preference assignment even if the task with a lower priority is still in the running stage. When it comes to executing the higher priority job, the task with lower priority waits for some time and continues its executing process when the first priority job gets completed.


## What is Non-Preemptive Scheduling?
Non-preemptive Scheduling is a CPU scheduling method in which a procedure takes the resource, and holds it till it gets terminated or changes to the waiting condition.



##Difference between Preemptive and Non-Preemptive Scheduling
<table>
<tbody>
<tr>
<td><strong>S.No.</strong></td>
<td><strong>Preemptive Scheduling</strong></td>
<td><strong>Non-Preemptive Scheduling</strong></td>
</tr>
<tr>
<td>1</td>
<td>In preemptive scheduling, the bits of help or resources are allotted to a procedure for a fixed time.</td>
<td>In non-preemptive scheduling, once the bits of help or resources are allotted to a procedure, the process carries it until it satisfies or shifts to the waiting state.</td>
</tr>
<tr>
<td>2</td>
<td>Here, interruption can occur between the processes.</td>
<td>Here, the process cannot be interrupted.</td>
</tr>
<tr>
<td>4</td>
<td>It includes overheads of organising the procedures.</td>
<td>It does not include overheads.</td>
</tr>
<tr>
<td>5</td>
<td>It is adaptable in nature.</td>
<td>It is not flexible in nature.</td>
</tr>
<tr>
<td>6</td>
<td>It is cost-oriented.</td>
<td>Non-preemptive scheduling is not cost oriented.</td>
</tr>
<tr>
<td>7</td>
<td>CPU utilisation is high here.</td>
<td>CPU utilisation is low here.</td>
</tr>
</tbody>
</table>
