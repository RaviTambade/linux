# Memory Management

Memory management in OS is a technique of managing the functionality of primary memory, used for achieving better concurrency, system performance, and memory utilization. Memory management keeps track of the status of each memory location, whether it is allocated or free.


## Paging
In an operating system, memory management refers to dividing the memory among the various processes. The fundamental goal of memory management is to make optimal use of memory by minimizing internal and external fragmentation. One such algorithm for memory management techniques is paging.

Operating systems utilize paging as a memory management strategy to manage memory and assign memory to programs, so it eliminates the requirement for contiguous physical memory allocation. Paging is the procedure of transferring operations in the form of pages from the secondary storage into the primary memory. Memory is split into fixed-size units called pages in paging, and processes are given memory allotments based on these pages. Paging is a logical idea that is utilized to provide quicker access to data.

###What is Paging?
Paging is a static memory allocation method that allows a process's physical address space to be of a non-contiguous type. It's a memory management scheme or storage mechanism that lets the operating system fetch processes from secondary memory in the form of pages and place them in the main memory. The paging hardware and operating system are integrated to implement the paging process.

A page is a logical memory unit in a program. Logical memory is organized into equal-sized pages or equal-sized blocks. A frame is a type of physical memory unit. In the concept of paging, physical memory (main memory) is organized into frames, which are equally sized memory blocks. The memory size of a new process is determined when it arrives. If a process has n pages in local memory, there must be n frames available in the system.

To get maximum utilization of the main memory and minimize external fragmentation, the size of a frame should be the same as the size of a page. Paging is mostly used to store non-contiguous portions of a single process. To make the paging method easier, the operating system decides:

- The program's total page count.
- Finds a sufficient number of empty page frames to assist.
- All pages must be contiguous to be loaded into memory.


### Characteristics of Paging in OS

Paging in OS has five key characteristics: 

- External fragmentation is not present.
- By procedure, any frame may be employed.
- Only on the last page of a process, internal fragmentation may occur.
- A process's physical memory is no longer contiguous.
- A process' logical memory is still contiguous.

Example of Paging
Here is an example. Let’s say the main memory size is 64B and the frame size is 4B then, the number of frames would be 64/4 = 16. There are 4 processes. The size of each process is 16B and the page size is also 4B then, the number of pages in each process = 16/4 = 4. These pages may be stored in the main memory frames in a non-contiguous form, depending on their availability.

#### Understanding Paging In Operating System In Detail

Paging in OS: Page Table
If we speak of paging in the operating system, the logical and physical memory addresses are separated. As a result, an address translation mechanism is required to convert the logical address into a physical address. The physical address is the actual address of the frame where each page will be placed, whereas the logical address space is the address created by the CPU for each page.

The CPU generates a logical address that is made up of two parts-

Page Number (p): Determines which page of the process the CPU wishes to read the data from.
Page Offset (d): Defines which word on the page the CPU wants to read.
When the CPU generates a page number, the page table displays the relevant frame number (frame base address) for each page in the main memory.

The required physical address is formed by multiplying the frame number by the page offset. The frame number identifies the frame in which the required page is stored. Page Offset provides the precise word from that page that must be read.

#### Understanding Paging In Operating System In Detail

Every new process creates a separate page table (stored in physical memory). A page table entry contains a variety of page-related information. The information contained in the page table item differs from one operating system to another. PTE has the following information:

Frame Number: It is the most crucial piece of information in a page table entry. The frame number identifies the memory frames in the paging in which the page is stored. The size of the frame number is determined by the number of frames in the main memory.
The number of bits for frame = Size of Physical memory/Frame size.

Present/Absent Bit: This is also referred to as the valid/invalid bit. This bit indicates whether or not the page is in the main memory space. This bit is set to 0 if the page is not available in the main memory; otherwise, it is set to 1.

Protection bit: This bit is also known as the 'Read / Write bit.' This bit is about page security. It determines whether or not the user has permission to read and write to the page. This bit is set to 0 if only read operations are allowed and no writing operations are allowed. If both read and write operations are permitted, this bit will be set to 1.

Reference bit: The reference bit indicates whether or not the page was referred to in the previous clock cycle. If the page has recently been referenced, this bit is set to 1, otherwise, it is set to 0.

Caching Enabled/Disabled: The reference bit indicates whether or not the page was referred to in the previous clock cycle. If the page has recently been referenced, this bit is set to 1, otherwise, it is set to 0.

Dirty bit: This bit is also known as the "Modified bit." This bit indicates whether or not the page has been changed. This bit is set to 1 if the page has been updated; otherwise, it is set to 0.


### Understanding Paging In Operating System In Detail

##### Page Table Types

Following are the two most used Page Table types:

1. Single Level Page Table
Only single-page tables are used in this procedure. Page tables are made up of a linear array of page table entries (PTEs). Each PTE holds information on the page, such as its physical page number and status bits, such as whether the page is valid or not, as well as any other bits.

Every memory reference will have its address translated. The size of the page table might vary greatly depending on the page size. The loading of larger page tables takes longer.

Drawback: The main downside of this strategy is that managing these big page tables as a single entity is problematic. Because of the additional memory reference for the page table, mapping from virtual to physical address is delayed.

2. Multi-Level Page Table

A multilevel page table is split into two or more levels. Page tables are stored in multi-level tables, which have a tree-like structure.

The level-0 page table's entries are pointers to a level-1 page table.
The level-1 page table's entries are pointers to a level-2 page table.
Actual page information will be stored in the entries of the final level page table.

When paging is implemented on the page table in multilevel paging, the base address of the first-level page entry will be the base address of the second-level page table entry, and the second-level page table entry will be the base address of the third-level page table entry, and so on.

The frame number of actual pages will be displayed in the final level page table item. In multilevel paging, regardless of the level of paging, all the PT will be stored in the main memory and all PT entries carry simply the frame number.

Drawback: All of the page tables are kept in memory. As a result, getting the physical address of the page frame needs more than one memory access, one for each level required. Extra memory references to access address translation can slow down a program in memory by a factor of two or more, which is a considerable drawback.

### Understanding Paging In Operating System In Detail

Paging with TLB (Translation Look-aside Buffer)
To access a byte in paging, the first-page table item must be visited, followed by the bytes.
As a result, two memory accesses will be required. Memory access is slowed by a factor of two as a result. In most cases, this delay would be intolerable.

The above issue can be remedied by employing a fast-searching hardware cache called a translation look-aside buffer. The TLB is a type of associative fast memory.

Every table entry is broken into two parts: one is the key, and the other is the value. When an object is introduced to the associative memory, it is compared to all keys at the same time. If there is a match, the value field for that match is returned.

Despite the high cost of the technology, the search mechanism that is enabled in this way is extremely quick. TLB typically stores a limited amount of entries, usually between 64 and 1024.

### Understanding Paging In Operating System In Detail

Advantages of Paging in OS
- Memory management is effective.
- Simplicity in partitioning (non-contiguous memory allocation).
- Allocating memory is simple and inexpensive.
- Pages are simple to share.
- No compaction is necessary.
- No external fragmentation.
- More efficient swapping.


Disadvantages of Paging in OS
- Internal fragmentation (only at the last page of the process).
- Address translation necessitates the use of specialized hardware.
- Page Table is stored in the main memory.
- Address translation lengthens memory cycle times.
- Memory reference overhead is caused by multi-level paging.
 -Memory access time is longer.

Paging allows you to save a process in memory in a non-contiguous manner and it is invisible to programmers. Although paging in operating system is a storage strategy that allows the OS to retrieve processes from secondary storage into main memory in the form of pages, it might result in internal fragmentation.

### Frequently Asked Questions

- Q. Describe the paging technique.
Paging is a memory management employed by operating systems to organize memory and assign memory to processes. Processes are allotted memory in terms of pages. Pages are fixed-size blocks of memory used in paging. Paging includes transferring operations in the form of pages from the secondary storage into the primary memory.

- Q. What are the logical pages in paging?
In paging, logical pages are fixed-sized blocks of logical or secondary memory. Logical pages represent a unit of information transfer between main memory and secondary storage. The logical memory is divided into blocks of the same size called pages. When a process is about to run, its pages are loaded from the backup store into any free memory frames. The page table, which is utilized by the memory management unit to convert logical addresses into physical addresses, keeps the mapping between logical pages and physical page frames.

- Q. How does paging contribute to memory protection in a computer system?
Paging contributes to memory protection in a computer system in the following ways:

Protection bits: Through the association of protection bits with each page, paging enables memory protection and these bits identify the protection on the appropriate page and are linked to each item in the page table. The protection bits can be used to control access to pages and prevent unauthorized access to memory.

Valid/Invalid bit: The paging process should be protected by using the concept of insertion of an additional bit called Valid/Invalid bit. This bit is used to indicate whether a page is currently in memory or not. If the bit is set to valid, the page is in memory, and if it is set to invalid, the page is not in memory.

Easy-to-use memory management algorithm: External fragmentation is unnecessary because of the simple-to-use memory management mechanism of paging. It is a sensible idea and enables quicker access to data.

- Q. Mention some advantages of paging.
Some advantages of paging are:

Easy-to-use memory management algorithm: Paging is an easy-to-use memory management algorithm that allows for faster access to data and is a logical concept.
Protection and sharing of memory: Paging allows for the protection and sharing of memory between processes, as each process has its page table that maps its logical address.
Swapping is easy between equal-sized pages and page frames: As pages and frames are of equal size, swapping between them becomes very easy.

- Q. What is the role of a page table in the paging technique?
An essential part of the operating system paging method is the page table. The mapping between virtual addresses used by a process and physical addresses utilized by the hardware is stored in this data structure, which is used by the operating system. The page table maintains the mapping between logical page numbers and physical page frames and the memory management unit converts logical addresses into physical addresses using the page table. The page table's function in the paging technique is to supply the base address of the frame (matching frame number) where that page is placed in the main memory.

- Q. When does a page fault occur, and what does it signify?
An attempt by a program to access data or code that is in its address space but is not currently available in the system RAM results in a page fault. It signifies that the data or code being accessed is not present in the physical memory or RAM and must be retrieved from secondary storage, such as a hard disk or solid-state drive. When a page fault occurs, the computer hardware traps the kernel, and the program counter (PC) is saved on the stack. The operating system then finds out which virtual page is needed and retrieves it from secondary storage.

- Q. Mention some important characteristics of paging.
Some characteristics of paging are:

- Fixed-size blocks: Paging divides the main memory into fixed-size blocks called frames, and the process is divided into pages of the same size as frames.
- Non-contiguous allocation of physical memory: Paging does not need contiguous allocation of physical memory since it supports non-contiguous allocation.
- Memory protection: Through the association of protection bits with each page, paging offers memory protection and these bits, which determine protection on the relevant page, are connected to each item in the page table.