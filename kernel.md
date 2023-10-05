
# Operating System Kernel

Operating system implements two basic functions below :
- It must be simply use as extension machine 
- It must manage and distribute all kinds of resources reasonably as the manager of the computer system.

Some operating system also takes charge of the computer system’s safety and provides application-specific services, such as networking, graphic interface etc.

The kernel is the most important part of the operating system. It is the primary interface between the hardware and the processes of a computer. The kernel connects these two in order to adjust resources as effectively as possible.

Linux and Windows family operating systems that are based on NT are most typical operating systems at the moment, but Linux focus on executing efficiency while Windows family pay more attention to convenient use.
..

### Linux Kernel Architecture
<img src="/images/Kernel/LinuxKernelArchitecture.jpg"/>

As to kernel architecture, Linux is a monolithic kernel operating system, and the whole kernel is very compact. Maintaining for this type of kernel is difficult, and the kernel takes up more memory space in running time.


### Windows Kernel Architecture
<img src="/images/Kernel/WindowsKernelArchitecture.jpg"/>

Windows is a microkernel operating system. As a result, it makes many operating system functions modularity and is easy for maintaining and extension for operating system. However, the system running efficiency is lower than monolithic kernel. It is worth noting that the graphics drivers of Windows operating system are directly running on the hardware, thus Windows have better graphics capabilities, which makes up for the lower running efficiency. 

Actually, it is difficult to distinguish between monolithic kernel and microkernel because there is one trend of kernel development :
-  The services provided by operating system that has a monolithic kernel are more modular, that is to say, this kind of operating system allow dynamic loading, 
- while the services provided by operating system that has a microkernel are more integrated into kernel. 

So, the kernel architectures of almost all the current operating systems are hybrid kernels that are between monolithic kernels and microkernels.