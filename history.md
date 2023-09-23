## What is an Operating System?
An operating system (OS) manages all other applications and programs in a computer, and it is loaded into the computer by a boot program. It enables applications to interact with a computer’s hardware. Through a designated application programme interface, the application programmes request services from the operating system (API). The kernel is the software that contains the operating system’s core components. To run other programmes, every computer has to have at least one operating system installed.

<img src="/images/OS.png"/>

Windows, Linux, and Android are examples of operating systems that enable the user to use programs like MS Office, Notepad, and games on the computer or mobile phone. It is necessary to have at least one operating system installed in the computer to run basic programs like browsers.

#### The core functions of an operating system include:
-<b> Managing hardware resources</b>: An operating system manages resources such as CPU, memory, and disk space, and assigns these resources to running applications.
-<b> Running applications</b>: An operating system provides an environment in which applications can run and interact with the user.
-<b> Providing a user interface</b>: An operating system provides a graphical user interface (GUI) that allows users to interact with the computer.

Examples of popular operating systems include:
- <b>Windows</b>: Microsoft Windows is the most popular desktop operating system, used by over 1 billion users worldwide. It has a wide range of features and applications, including the Office suite, gaming, and productivity tools.
-<b> macOS</b>: macOS is the desktop operating system used by Apple Mac computers. It is known for its clean, user-friendly interface, and is popular among creative professionals.
- <b> Linux</b>: Linux is an open-source operating system that is available for free and can be customized to meet specific needs. It is used by developers and businesses, as well as individuals who prefer an open-source, customizable operating system.


## History of Operating Systems

- The first computer, Z1, was made in 1936 – 1938. Unfortunately, this computer ran without an operating system.
- Twenty years later, the first-ever operating system was made in 1956.
- In the 1960s, bell labs started working on building UNIX, the first multitasking operating system.
- In 1977 the apple series came into existence. Apple Dos 3.3 was the first disk operating system.
- In 1981, Microsoft built the first operating system called DOS by purchasing 86 – DOS software from a Seattle company.
- The most famous Microsoft windows came into existence in 1985 when MS-DOS was paired with GUI, a graphics environment. 

## Functions of Operating System

- <b>Processor Management</b>: An operating system manages the processor’s work by allocating various jobs to it and ensuring that each process receives enough time from the processor to function properly.
- <b>Memory Management</b>: An operating system manages the allocation and deallocation of the memory to various processes and ensures that the other process does not consume the memory allocated to one process.
-<b> Device Management</b>: There are various input and output devices. An OS controls the working of these input-output devices. It receives the requests from these devices, performs a specific task, and communicates back to the requesting process.
-<b> File Management</b>: An operating system keeps track of information regarding the creation, deletion, transfer, copy, and storage of files in an organized way. It also maintains the integrity of the data stored in these files, including the file directory structure, by protecting against unauthorized access.
-<b> Security</b>: The operating system provides various techniques which assure the integrity and confidentiality of user data. Following security measures are used to protect user data:
    - Protection against unauthorized access through login.
    - Protection against intrusion by keeping Firefall active.
    - Protecting the system memory against malicious access.
    - Displaying messages related to system vulnerabilities.
    - Error Detection: From time to time, the operating system checks the system for any external threat or malicious software activity. It also checks the hardware for any type of damage. This process displays several alerts to the user so that the appropriate action can be taken against any damage caused to the system. 
- Job Scheduling: In a multitasking OS where multiple programs run simultaneously, the operating system determines which applications should run in which order and how time should be allocated to each application. 


## Features of Operating Systems
Here is a list of some important features of operating systems:

1. Provides a platform for running applications
1. Handles memory management and CPU scheduling
1. Provides file system abstraction
1. Provides networking support
1. Provides security features
1. Provides user interface
1. Provides utilities and system services
1. Supports application development


## Components of Operating System
Now to perform the functions mentioned above, the operating system has two components:

- Shell
- Kernel

## What is Shell?

Shell handles user interactions. It is the outermost layer of the OS and manages the interaction between user and operating system by:

- Prompting the user to give input
- Interpreting the input for the operating system
- Handling the output from the operating system.

Shell provides a way to communicate with the OS by either taking the input from the user or the shell script. A shell script is a sequence of system commands that are stored in a file.

## What is Kernel?
The kernel is the core component of an operating system for a computer (OS). All other components of the OS rely on the core to supply them with essential services. It serves as the primary interface between the OS and the hardware and aids in the control of devices, networking, file systems, and process and memory management.

<img src="/images/OSKernel.png"/>

## Functions of kernel
The kernel is the core component of an operating system which acts as an interface between applications, and the data is processed at the hardware level.

When an OS is loaded into memory, the kernel is loaded first and remains in memory until the OS is shut down. After that, the kernel provides and manages the computer resources and allows other programs to run and use these resources. The kernel also sets up the memory address space for applications, loads the files with application code into memory, and sets up the execution stack for programs.


The kernel is responsible for performing the following tasks:

- Input-Output management 
- Memory Management 
- Process Management for application execution. 
- Device Management 
- System calls control 


Earlier, all the basic system services like process and memory management, interrupt handling, etc., were packaged into a single module in the kernel space. This type of kernel was called the Monolithic Kernel. The problem with this approach was that the whole kernel had to be recompiled for even a small change.

In a modern-day approach to monolithic architecture, a microkernel contains different modules like device management, file management, etc. It is dynamically loaded and unloaded. With this modern-day approach, the kernel code size was reduced while its stability increased. 

## Types of Kernel

Linus Torvalds introduced the concept of a monolithic kernel in 1991 as a part of the Linux kernel. A monolithic kernel is a single large program that contains all operating system components. However, the Linux kernel evolved over the years and now consists of different types of kernels, as listed below.


1. <b>Monolithic Kernel</b> As the name suggests, a monolithic kernel is a single large program that contains all operating system components. The entire kernel executes in the processor’s privileged mode and provides full access to the system’s hardware. Monolithic kernels are faster than microkernels because they don’t have the overhead of message passing. This type of kernel is generally used in embedded systems and real-time operating systems.

2.<b> Microkernel </b>A microkernel is a kernel that contains only the essential components required for the basic functioning of the operating system. All other components are removed from the kernel and implemented as user-space processes. The microkernel approach provides better modularity, flexibility, and extensibility. It is also more stable and secure than monolithic kernels.

3.<b> Hybrid Kernel</b> A hybrid kernel is a kernel that combines the best features of both monolithic kernels and microkernels. It contains a small microkernel that provides the essential components for the basic functioning of the OS. The remaining components are implemented as user-space processes or as loadable kernel modules. This approach provides the best of both worlds, namely, the performance of monolithic kernels and the modularity of microkernels.

4. <b>Exokernel</b> An exokernel is a kernel that provides the bare minimum components required for the basic functioning of the operating system. All other components are removed from the kernel and implemented as user-space processes. The exokernel approach provides the best possible performance because there is no kernel overhead. However, it is also the most difficult to implement and is not widely used.



## Types of Operating Systems
There are several different types of operating systems present. In this section, we will discuss the advantages and disadvantages of these types of OS.

- Batch OS
- Distributed OS
- Multitasking OS
- Network OS
- Real-OS
- Mobile OS

## Batch OS
Batch OS is the first operating system for second-generation computers. This OS does not directly interact with the computer. Instead, an operator takes up similar jobs and groups them together into a batch, and then these batches are executed one by one based on the first-come, first, serve principle.

<b>Advantages of Batch OS</b>

- Execution time taken for similar jobs is higher.
- Multiple users can share batch systems.
- Managing large works becomes easy in batch systems.
- The idle time for a single batch is very less.

<b>Disadvantages of OS</b>

- It is hard to debug batch systems.
- If a job fails, then the other jobs have to wait for an unknown time till the issue is resolved.
- Batch systems are sometimes costly.


<b>Examples of Batch OS</b>: payroll system, bank statements, data entry, etc.

## Distributed OS
A distributed OS is a recent advancement in the field of computer technology and is utilized all over the world that too with great pace. In a distributed OS, various computers are connected through a single communication channel. These independent computers have their memory unit and CPU and are known as loosely coupled systems. The system processes can be of different sizes and can perform different functions. The major benefit of such a type of operating system is that a user can access files that are not present on his system but in another connected system. In addition, remote access is available to the systems connected to this network.


<b>Advantages of Distributed OS</b>

- Failure of one system will not affect the other systems because all the computers are independent of each other.
- The load on the host system is reduced.
- The size of the network is easily scalable as many computers can be added to the network.
- As the workload and resources are shared therefore the calculations are performed at a higher speed.
- Data exchange speed is increased with the help of electronic mail.

<b>Disadvantages of Distributed OS</b>

- The setup cost is high.
- Software used for such systems is highly complex.
- Failure of the main network will lead to the failure of the whole system.

<b>Examples of Distributed OS</b>: LOCUS, etc.


## Multitasking OS
The multitasking OS is also known as the time-sharing operating system as each task is given some time so that all the tasks work efficiently.  This system provides access to a large number of users, and each user gets the time of CPU as they get in a single system. The tasks performed are given by a single user or by different users. The time allotted to execute one task is called a quantum, and as soon as the time to execute one task is completed, the system switches over to another task.


<b>Advantages of Multitasking OS</b>

- Each task gets equal time for execution.
- The idle time for the CPU will be the lowest.
- There are very few chances for the duplication of the software.

<b>Disadvantages of Multitasking OS</b>

- Processes with higher priority cannot be executed first as equal priority is given to each process or task.
- Various user data is needed to be taken care of from unauthorized access.
- Sometimes there is a data communication problem.

<b>Examples of Multitasking OS</b>: UNIX, etc.


## Network OS
Network operating systems are the systems that run on a server and manage all the networking functions. They allow sharing of various files, applications, printers, security, and other networking functions over a small network of computers like LAN or any other private network. In the network OS, all the users are aware of the configurations of every other user within the network, which is why network operating systems are also known as tightly coupled systems.

<b>Advantages of Network OS</b>

- New technologies and hardware can easily upgrade the systems.
- Security of the system is managed over servers.
- Servers can be accessed remotely from different locations and systems.
- The centralized servers are stable.

<b>Disadvantages of Network OS</b>

- Server costs are high.
- Regular updates and maintenance are required.
- Users are dependent on the central location for the maximum number of operations.
<b>Examples of Network OS</b>: Microsoft Windows server 2008, LINUX, etc.


## Real-Time OS
Real-Time operating systems serve real-time systems. These operating systems are useful when many events occur in a short time or within certain deadlines, such as real-time simulations.

Types of the real-time OS are:

- Hard real-time OS
The hard real-time OS is the operating system for mainly the applications in which the slightest delay is also unacceptable. The time constraints of such applications are very strict. Such systems are built for life-saving equipment like parachutes and airbags, which immediately need to be in action if an accident happens.

- Soft real-time OS
The soft real-time OS is the operating system for applications where time constraint is not very strict.

In a soft real-time system, an important task is prioritized over less important tasks, and this priority remains active until the completion of the task. Furthermore, a time limit is always set for a specific job, enabling short time delays for future tasks, which is acceptable. For Example, virtual reality, reservation systems, etc.  


<b>Advantages of Real-Time OS</b>

- It provides more output from all the resources as there is maximum utilization of systems.
- It provides the best management of memory allocation.
- These systems are always error-free.
- These operating systems focus more on running applications than those in the queue.
- Shifting from one task to another takes very little time.


<b>Disadvantages of Real-Time OS</b>

- System resources are extremely expensive and are not so good.
- The algorithms used are very complex.
- Only limited tasks can run at a single time.
- In such systems, we cannot set thread priority as these systems cannot switch tasks easily.

<b>Examples of Real-Time OS</b>: Medical imaging systems, robots, etc.


## Mobile OS
A mobile OS is an operating system for smartphones, tablets, and PDA’s. It is a platform on which other applications can run on mobile devices.

Advantages of Mobile OS

- It provides ease to users.

<b>Disadvantages of Mobile OS</b>

- Some of mobile operating systems give poor battery quality to users.
- Some of the mobile operating systems are not user-friendly.

<b>Examples of Mobile OS</b>: Android OS, ios, Symbian OS, and Windows mobile OS. 

## Operating system differences

- Single-tasking vs. multi-tasking operating systems: Single-tasking operating systems allow only one program to run at a time, while multi-tasking operating systems allow multiple programs to run simultaneously.
- Desktop vs. mobile operating systems: Desktop operating systems, such as Windows and macOS, are designed for use on desktop and laptop computers, while mobile operating systems, such as iOS and Android, are designed for use on smartphones and tablets.
- Open-source vs. proprietary operating systems: Open-source operating systems are developed by a community of developers and are available for free, while proprietary operating systems are developed by a single company and must be purchased.


## Functions of an Operating System
An operating system performs several functions, including:

- Resource allocation and management: An operating system manages hardware resources such as CPU, memory, and disk space, and assigns these resources to running applications based on their priority.
- Memory management: An operating system manages memory usage, including virtual memory and memory allocation. It also ensures that memory is shared efficiently among running programs.
- Device management: An operating system manages input and output devices such as printers, scanners, and keyboards. It ensures that these devices are compatible with the system and can be used by applications.
- User interface management: An operating system provides a graphical user interface (GUI) that allows users to interact with the computer. It manages windows, menus, and other graphical elements.
- Security management: An operating system manages security features such as user authentication, firewalls, and antivirus software. It also ensures that applications and data are protected from unauthorized access.



<h2 class="wp-block-heading" id="32-bit-os-versus-64-bit-os"><strong>32-bit OS versus 64-bit OS</strong></h2>



<figure class="wp-block-table is-style-stripes"><table><tbody><tr><td><strong>Parameter</strong></td><td><strong>32-Bit OS</strong></td><td><strong>64-Bit OS</strong></td></tr><tr><td>Data and Storage</td><td>The 32 bit OS can store and manage less data than the 64 bit OS, as its name would imply. It addresses a maximum of 4,294,967,296 bytes (4 GB) of RAM in more detail.</td><td>In contrast, the 64 bit OS has a larger data handling capacity than the 32 bit OS. It indicates that a total of 264 memory addresses, or 18 quintillion gigabytes of RAM, can be addressed.</td></tr><tr><td>Compatibility of System</td><td>A 32-bit processor system will run only on 32-bit OS and not on 64 bit OS.</td><td>A 64-bit processor system can run either a 32-bit or 64-bit OS</td></tr><tr><td>Application Support</td><td>The 32-bit OS support applications with no hassle.</td><td>The 64-bit OS do not support applications.</td></tr><tr><td>Performance</td><td>Performance of 32- bit OS is less efficient.</td><td>Higher performance than the 32-bit processor.</td></tr><tr><td>Systems Available</td><td>These support Windows 7, Windows XP, Windows Vista, Windows 8, and Linux.</td><td>These support Windows XP Professional, Windows 7, Windows 8, Windows 10, Windows Vista, Linux, and Mac OS X.</td></tr></tbody></table></figure>



<h2 class="wp-block-heading" class="wp-block-heading" id="popular-operating-systems"><strong>Popular Operating Systems</strong></h2>



<p>Some of the most popular operating systems in use today include:</p>



<ul>
<li><strong>Windows: </strong>Windows is the most popular desktop operating system, used by over 1 billion users worldwide. It has a wide range of features and applications, including the Office suite, gaming, and productivity tools.</li>



<li><strong>macOS:</strong> macOS is the desktop operating system used by Apple Mac computers. It is known for its clean, user-friendly interface and is popular among creative professionals.</li>



<li><strong>Linux: </strong>Linux is an open-source operating system that is available for free and can be customized to meet specific needs. It is used by developers, businesses, and individuals who prefer an open-source, customizable operating system.</li>



<li><strong>iOS: </strong>iOS is the mobile operating system used by Apple iPhones and iPads. It is known for its user-friendly interface, tight integration with Apple&#8217;s hardware and software, and robust security features.</li>



<li><strong>Android:</strong> Android is the most popular mobile operating system, used by over 2 billion users worldwide. It is known for its open-source nature, customization options, and compatibility with a wide range of devices.</li>
</ul>




<h2 class="wp-block-heading" class="wp-block-heading" id="choosing-the-right-operating-system"><strong>Choosing the Right Operating System</strong></h2>

<p>When choosing an operating system, there are several factors to consider, including:</p>
<ul>
<li><strong>Cost:</strong> Some operating systems, such as Linux, are free, while others, such as Windows and macOS, must be purchased.</li>
<li><strong>Compatibility:</strong> Some software and hardware may only work with certain operating systems, so choosing an operating system compatible with your needs is important.</li>
<li><strong>Ease of use:</strong> Some operating systems, such as macOS and iOS, are known for their user-friendly interfaces, while others, such as Linux, may have a steeper learning curve.</li>
<li><strong>Security: </strong>Some operating systems, such as macOS and iOS, are known for their robust security features, while others, such as Windows, may be more vulnerable to security threats.</li>
</ul>


## Operating System Generations 
<p>Operating systems have evolved over time through different generations, each marked by distinct characteristics and advancements. Let&#8217;s explore these generations along with real-time examples:</p>

<p><strong>1. First Generation:</strong></p>
<ul>
<li>Time Period: 1940s to early 1950s</li>
<li>Characteristics: Vacuum tubes and machine language programming.</li>
<li>Example: ENIAC (Electronic Numerical Integrator and Computer) &#8211; One of the earliest computers that used vacuum tubes for calculations.</li>
</ul>

<p><strong>2. Second Generation:</strong></p>
<ul>
<li>Time Period: Late 1950s to mid-1960s</li>
<li>Characteristics: Transistors and assembly language programming.</li>
<li>Example: IBM 1401 &#8211; Used transistors, enabling faster and more reliable processing than vacuum tubes.</li>
</ul>

<p><strong>3. Third Generation:</strong></p>
<ul>
<li>Time Period: Mid-1960s to mid-1970s</li>
<li>Characteristics: Integrated circuits (ICs) and high-level programming languages.</li>
<li>Example: IBM System/360 &#8211; Introduced a family of computers using compatible software and peripheral devices.</li>
</ul>

<p><strong>4. Fourth Generation:</strong></p>
<ul>
<li>Time Period: Late 1970s to 1990s</li>
<li>Characteristics: Microprocessors, personal computers, and graphical user interfaces (GUI).</li>

<li>Example: Apple Macintosh &#8211; Introduced GUI and mouse-driven interface, making computers more user-friendly.</li>
</ul>

<p><strong>5. Fifth Generation:</strong></p>
<ul>
<li>Time Period: 1990s to present (continuing)</li>
<li>Characteristics: Artificial Intelligence (AI), natural language processing, and parallel processing.</li>
<li>Example: IBM&#8217;s Deep Blue &#8211; Defeated world chess champion Garry Kasparov in 1997, showcasing the power of AI in complex decision-making.</li>
</ul>
<p><strong>6. Sixth Generation (Speculative):</strong></p>
<ul>
<li>Characteristics: Advanced AI, quantum computing, brain-computer interfaces.</li>
<li>Example: Quantum computers being developed by companies like IBM and Google, potentially revolutionizing complex calculations.</li>
</ul>
<p><strong>7. Future Generations (Hypothetical):</strong></p>
<ul>
<li>Characteristics: Even more advanced AI, integration with human cognition, new computing paradigms.</li>
<li>Example: A future generation could involve computers that seamlessly interface with the human brain, enabling direct thought-based interactions.</li>
</ul>

<p>These generations demonstrate how operating systems have evolved from basic machine-level instructions to sophisticated systems that can handle complex tasks and interactions with users. Each generation builds upon the achievements of the previous one, incorporating new technologies and capabilities.</p>

### Advantages of Operating System

<p>There are several advantages of operating systems. We have listed some of them below: </p>
- Ensuring correct and efficient use of the computer&#8217;s hardware.
- Allowing different applications to run concurrently.
- Managing files and folders.
- Providing a user interface.
- Managing security.
- Managing resources.
- Managing printing.
- Providing a platform for software development.

### Disadvantages of Operating System

<p>There are several disadvantages of operating systems. We have listed some of them below:</p>
- They can be complex and difficult to use. </li>
- They can be expensive to purchase and maintain. </li>
- They can be vulnerable to attacks from malicious users.</li>




## Real-Time Operating System</strong></h2>
# What is RTOS?
<p>An operating system that can execute multi-threaded programmes and adhere to real-time deadlines is known as a &#8220;RTOS.&#8221; The majority of RTOSes incorporate device drivers, resource management, and schedulers. Remember that we don&#8217;t always mean &#8220;quick&#8221; when we talk about &#8220;deadlines.&#8221; Instead, this means that we can foresee when specific jobs will run before runtime.</p>

<p>If you&#8217;re writing intricate embedded applications, an RTOS can be a great tool. They support task isolation and enable concurrent operation.</p>

### Applications of Real-Time Operating System

- Defence application systems like RADAR.</span></li>
- Airlines reservation system.
- Systems that provide immediate updating.
- Networked Multimedia Systems.
- Air traffic control system.
- Command Control Systems.