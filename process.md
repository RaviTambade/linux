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

### Process Scheduling
When there are several or more runnable processes, the operating system chooses which one to run first; this is known as process scheduling.

A scheduler is a program that uses a scheduling algorithm to make choices. The following are characteristics of a good scheduling algorithm:

- For users, response time should be kept to a bare minimum.
- The total number of jobs processed every hour should be as high as possible, implying that a good scheduling system should provide the highest possible throughput.
- The CPU should be used to its full potential.
- Each process should be given an equal amount of CPU time.


### Process Scheduling Algorithms
Process Scheduling Algorithms are given below:

#### 1.First Come First Serve (FCFS) Scheduling
- It is a non-preemptive scheduling algorithm.
- The process which arrives first gets executed first or the process which requests the CPU first gets the CPU allocated first.
- First Come First Serve, is just like FIFO (First in First out) Queue data structure, where the data element which is added to the queue first, is the one who leaves the queue first.
- A perfect real-life example of FCFS scheduling is buying tickets at the ticket counter.

###### Advantages
- FCFS algorithm doesn’t include any complex logic, it just puts the process requests in a queue and executes it one by one. Hence, FCFS is pretty simple and easy to implement.
- Eventually, every process will get a chance to run, so starvation doesn’t occur.

###### Disadvantages
- There is no option for pre-emption of a process. If a process is started, then the CPU executes the process until it ends.
- Because there is no pre-emption, if a process executes for a long time, the processes in the back of the queue will have to wait for a long time before they get a chance to be executed.

#### 2.Shortest Job First (SJF) Scheduling
- It is a non-preemptive scheduling algorithm.
- It is also known as the shortest job next (SJN)
- It is a scheduling policy that selects the waiting process with the smallest execution time to execute next.

###### Advantages.
- The throughput is increased because more processes can be executed in less amount of time.
- Having minimum average waiting time among all scheduling algorithms.

###### Disadvantages:
- It is practically infeasible as Operating System may not know burst time and therefore may not sort them.
- Longer processes will have a more waiting time, eventually, they’ll suffer starvation.

#### 3.Shortest Remaining Time (SRT) Scheduling
- It is a preemptive scheduling algorithm.
- It is also called Preemptive shortest job first or Shortest remaining time next or Shortest remaining time first.
- In this scheduling algorithm, the process with the smallest amount of time remaining until completion is selected to execute. Since the currently executing process is the one with the shortest amount of time remaining by definition, and since that time should only reduce as execution progresses, processes will always run until they complete or a new process is added that requires a smaller amount of time.

###### Advantage:
- Short processes are handled very quickly.
- The system also requires very little overhead since it only makes a decision when a process completes or a new process is added.
- When a new process is added the algorithm only needs to compare the currently executing process with the new process, ignoring all other processes currently waiting to execute.

###### Disadvantage:
- Like the shortest job first, it has the potential for process starvation.
- Long processes may be held off indefinitely if short processes are continually added.

#### 4.Priority Scheduling
- In this scheduling, Priority is assigned for each process.
- The process with the highest priority is executed first and so on.
- Processes with the same priority are executed in the FCFS manner.
- Priority can be decided based on memory requirements, time requirements or any other resource requirement.

###### Advantages of Priority Scheduling:
- The priority of a process can be selected based on memory requirement, time requirement or user preference.
- For example, a high-end game will have better graphics, which means the process which updates the screen in a game will have higher priority so as to achieve better graphics performance.

###### Disadvantages:

- A second scheduling algorithm is required to schedule the processes which have the same priority.
- In preemptive priority scheduling, a higher priority process can execute ahead of an already executing lower priority process. If the lower priority process keeps waiting for higher-priority processes, starvation occurs.
Priority scheduling is of both types: preemptive and non-preemptive.

###### a. Non-Preemptive Priority Scheduling:

- In the Non Preemptive Priority scheduling, The Processes are scheduled according to the priority number assigned to them.
- Once the process gets scheduled, it will run till the completion.
- Generally, the lower the priority number, the higher is the priority of the process.

###### b. Preemptive Priority Scheduling:

Preemptive Scheduling is a technique where the assignments are allotted with their preferences or priorities. In the case of preemptive scheduling, it is crucial to execute a higher preference assignment even if the task with a lower priority is still in the running stage. When it comes to executing the higher priority job, the task with lower priority waits for some time and continues its executing process when the first priority job gets completed.

######  Difference between Preemptive and Non-Preemptive Scheduling
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

####  Round Robin Scheduling:
- CPU is assigned to the process for a fixed amount of time.
- This fixed amount of time is called time quantum or time slice.
- After the time quantum expires, the running process is preempted and sent to the ready queue.
- Then, the processor is assigned to the next arrived process.
- It is always preemptive scheduling algorithm

Advantages
- It gives the best performance in terms of average response time.
- It is best suited for the time-sharing system, client-server architecture, and interactive system.

###### Disadvantages
- It leads to starvation for processes with larger burst time as they have to repeat the cycle many times.
- Its performance heavily depends on time quantum.
- Priorities cannot be set for the processes.


####  Real-Time Scheduling
- A real-time system is one in which time plays an essential role since processing should be done within the defined time limit otherwise the system will fail.
- Generally, in this type of system, one or more physical devices external to the computer generate the real-time data (stimuli) and the computer must react appropriately to them within a fixed amount of time.
- The algorithm that is used to schedule such a real-time system periodically is known as Real-Time Scheduling Algorithm.
- E.g. the computer attached with Compact Disc Player gets the bits as they come off the drive and must start converting them into music with a very tight time interval.
- If the calculation takes too long the music sounds peculiar.
- Other example includes Autopilot aircraft, Robot control in automated factory, Patient monitoring factory(ICU), etc.
- Real-Time scheduling algorithm includes:

###### a. Rate Monotonic Algorithm (RM)
This is a fixed priority algorithm and follows the philosophy that higher priority is given to tasks with the higher frequencies. Likewise, the lower priority is assigned to tasks with the lower frequencies. The scheduler at any time always chooses the highest priority task for execution. By approximating a reliable degree the execution times and the time that it takes for system handling functions, the behavior of the system can be determined apriority.

###### b. Earliest Deadline First Algorithm(EDF)
This algorithm takes the approach that tasks with the closest deadlines should be meted out the highest priorities. Likewise, the task with the latest deadline has the lowest priority. Due to this approach, the processor idle time is zero and so 100% utilization can be achieved.
