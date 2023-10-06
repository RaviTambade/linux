## Process Scheduling
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
