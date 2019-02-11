# Modern Operating Systems, 4th Edition
by Andrew S. Tanenbaum, Herbert Bos

`** Notes by Henry Cooksley **`

### 1 INTRODUCTION

operating system, shell, GUI, Graphical User Interface, kernel mode, supervisor mode, user mode, I/O, Input/Output

#### 1.1 WHAT IS AN OPERATING SYSTEM?

##### 1.1.1 The Operating System as an Extended Machine

architecture, SATA, Serial ATA, disk driver

"In this book, we will talk a lot about abstractions. They are one of the keys to understanding operating systems."

multiplexing

#### 1.2 HISTORY OF OPERATING SYSTEMS

##### 1.2.1 The First Generation (1945-55): Vacuum Tubes

##### 1.2.2 The Second Generation (1955-65): Transistors and Batch Systems

mainframes, job, batch system, off line

##### 1.2.3 The Third Generation (1965-1980): ICs and Multiprogramming

ICs, Integrated Circuits, OS/360, multiprogramming, spooling, Simultaneous Peripheral Operation On Line, timesharing, CTSS, Compatible Time Sharing System

"We will use the terms “procedure,” “subroutine,” and “function” interchangeably in this book."

MULTICS, MULTiplexed Information and Computing Service, cloud computing

"Despite its lack of commercial success, MULTICS had a huge influence on subsequent operating systems (especially UNIX and its derivatives, FreeBSD, Linux, iOS, and Android)."

UNIX, System V, BSD, Berkeley Software Distribution, POSIX, MINIX, Linux

##### 1.2.4 The Fourth Generation (1980-Present): Personal Computers

LSI, Large Scale Integration, microcomputers, CP/M, Control Program for Microcomputers, DOS, Disk Operating System, MS-DOS, MicroSoft Disk Operating System, user friendly, Mac OS X, Windows NT, New Technology, Windows Me, Millennium Edition, service packs, Digital Rights Management, x86, x86-32, x86-64, FreeBSD, X Window System, X11, Gnome, KDE, network operating systems, distributed operating systems

##### 1.2.5 The Fifth Generation (1990-Present): Mobile Computers

PDA, Symbian, RIM, iPhone

#### 1.3 COMPUTER HARDWARE REVIEW

##### 1.3.1 Processors

program counter, stack pointer, PSW, Program Status Word, pipeline, superscalar

"Generally, all instructions involving I/O and memory protection are disallowed in user mode."

system call, multithreading, hyperthreading, GPU, Graphics Processing Unit

##### 1.3.2 Memory

cache lines, cache hit, L1 cache, L2 cache, RAM, Random Access Memory, core memory, ROM, Read Only Memory, EEPROM, Electrically Erasable PROM, flash memory

##### 1.3.3 Disks

track, cylinder, SSDs, Solid State Disks, virtual memory, MMU, Memory Management Unit, context switch

##### 1.3.4 I/O Devices

SATA, Serial ATA, ATA, AT Attachment

"In case you are curious what AT stands for, this was IBM's second generation “Personal Computer Advanced Technology” built around the then-extremely-potent 6-MHz 80286 processor that the company introduced in 1984."

device driver, I/O port space, busy waiting, interrupt, interrupt vector, DMA, Direct Memory Access

##### 1.3.5 Buses

PCIe, Peripheral Component Interconnect Express, PCI, ISA, Industry Standard Architecture, shared bus architecture, parallel bus architecture, serial bus architecture, DMI, Direct Media Interface, USB, Universal Serial Bus, SCSI, Small Computer System Interface, plug and play

##### 1.3.6 Booting the Computer

BIOS, Basic Input Output System

#### 1.4 THE OPERATING SYSTEM ZOO

##### 1.4.1 Mainframe Operating System

##### 1.4.2 Server Operating Systems

##### 1.4.3 Multiprocessor Operating Systems

##### 1.4.4 Personal Computer Operating Systems

"Common examples are Linux, FreeBSD, Windows 7, Windows 8, and Apple's OS X."

##### 1.4.5 Handheld Computer Operating Systems

PDA, Personal Digital Assistant, apps

##### 1.4.6 Embedded Operating Systems

"Typical examples are microwave ovens, TV sets, cars, DVD recorders, traditional phones, and MP3 players."

##### 1.4.7 Sensor-Node Operating Systems

##### 1.4.8 Real-Time Operating Systems

hard real-time system

"Many of these are found in industrial process control, avionics, military, and similar application areas."

soft real-time system

"Smartphones are also soft real-time systems."

##### 1.4.9 Smart Card Operating Systems

#### 1.5 OPERATING SYSTEM CONCEPTS

##### 1.5.1 Processes

process, address space, process table, core image, command interpreter, child processes, interprocess communication, alarm signal

"Signals are the software analog of hardware interrupts and can be generated by a variety of causes in addition to timers expiring."

UID, User IDentification, GID, Group IDentification, superuser, Administrator

##### 1.5.2 Address Spaces

"The address space is decoupled from the machine's physical memory and may be either larger or smaller than the physical memory."

##### 1.5.3 Files

directory, path name, root directory, working directory, file descriptor, root file system, special file, block special files, character special files, pipes

"Thus, communication between processes in UNIX looks very much like ordinary file reads and writes."

##### 1.5.4 Input/Output

##### 1.5.5 Protection

"Files in UNIX are protected by assigning each one a 9-bit binary protection code."

rwx bits, read, write, execute

##### 1.5.6 The Shell

"Although it is not part of the operating system, it makes heavy use of many operating system features and thus serves as a good example of how the system calls are used."

"Many shells exist, including sh, csh, ksh, and bash."

prompt

"If a user puts an ampersand after a command, the shell does not wait for it to complete."

##### 1.5.7 Ontogeny Recapitulates Phylogeny

"Each new species (mainframe, minicomputer, personal computer, handheld, embedded computer, smart card, etc.) seems to go through the development that its ancestors did, both in hardware and in software."

Large Memories, Protection Hardware, Disks, Virtual Memory

#### 1.6 SYSTEM CALLS

"We have seen that operating systems have two main functions: providing abstractions to user programs and managing the computer's resources."

##### 1.6.1 System Calls for Process Management

PID, Process IDentifier, text segment, data segment, stack segment

##### 1.6.2 System Calls for File Management

##### 1.6.3 System Calls for Directory Management

i-nodes, partitions, minor devices

##### 1.6.4 Miscellaneous System Calls

"The chmod system call makes it possible to change the mode of a file."

"Windows and UNIX differ in a fundamental way in their respective programming models."

Win32 API, Application Programming Interface

"The number of Win32 API calls is extremely large, numbering in the thousands."

#### 1.7 OPERATING SYSTEM STRUCTURE

##### 1.7.1 Monolithic Systems

"The operating system is written as a collection of procedures, linked together into a single large executable binary program."

shared libraries, DLLs, Dynamic-Link-Libraries

##### 1.7.2 Layered Systems

##### 1.7.3 Microkernels

"In fact, a strong case can be made for putting as little as possible in kernel mode because bugs in the kernel can bring down the system instantly."

reincarnation server, mechanism, policy

##### 1.7.4 Client-Server Model

servers, clients, client-server

"To obtain a service, a client process constructs a message saying what it wants and sends it to the appropriate service."

##### 1.7.5 Virtual Machines

z/VM, VM/370, virtual machine monitor, CMS, Conversational Monitor System, Virtual Machines Rediscovered, shared hosting

"When a Web hosting company offers virtual machines for rent, a single physical machine can run many virtual machines, each of which appears to be a complete machine."

type 1 hypervisor, machine simulators, binary translation, type 2 hypervisors, host operating system, guest operating system, paravirtualization, The Java Virtual Machine, JVM, Java Virtual Machine

##### 1.7.6 Exokernels

exokernel

"Its job is to allocate resources to virtual machines and then check attempts to use them to make sure no machine is trying to use somebody else's resources."

#### 1.8 THE WORLD ACCORDING TO C

"The environment used for developing operating systems is very different from what individuals (such as students) are used to when writing small Java programs."

##### 1.8.1 The C Language

"This is not a guide to C, but a short summary of some of the key differences between C and languages like Python and especially Java."

pointer

"Pointers are a very powerful construct, but also a great source of errors when used carelessly."

"Some things that C does not have include built-in strings, threads, packages, classes, objects, type safety, and garbage collection."

##### 1.8.2 Header Files

macros

##### 1.8.3 Large Programming Projects

object file, C preprocessor

"Keeping track of which object files depend on which header files is completely unmanageable without help."

linker

##### The Model of Run Time

"Once running, it may dynamically load pieces that were not statically included in the binary such as device drivers and file systems."

#### 1.9 RESEARCH ON OPERATING SYSTEMS

"Virtually all operating systems researchers realize that current operating systems are massive, inflexible, unreliable, insecure, and loaded with bugs, certain ones more than others (names withheld here to protect the guilty)."

#### 1.10 OUTLINE OF THE REST OF THIS BOOK

"As mentioned already, from the programmer's point of view, the primary purpose of an operating system is to provide some key abstractions, the most important of which are processes and threads, address spaces, and files."

#### 1.11 METRIC UNITS

"Thus a 1-KB memory contains 1024 bytes, not 1000 bytes."

#### 1.12 SUMMARY

"Operating systems can be viewed from two viewpoints: resource managers and extended machines."

"In the resource-manager view, the operating system's job is to manage the different parts of the system efficiently."

"In the extended-machine view, the job of the system is to provide the users with abstractions that are more convenient to use than the actual machine."

"These include processes, address spaces, and files."

"The heart of any operating system is the set of system calls that it can handle."

"The first group of system calls relates to process creation and termination."

"The second group is for reading and writing files."

"The third group is for directory management."

"The fourth group contains miscellaneous calls."

### 2 PROCESSES AND THREADS

"The most central concept in any operating system is the process: an abstraction of a running program."

"Without the process abstraction, modern computing could not exist."

#### 2.1 PROCESSES

pseudoparallelism, multiprocessor

##### 2.1.1 The Process Model

sequential processes, processes, multiprogramming

##### 2.1.2 Process Creation

daemons, copy-on-write

##### 2.1.3 Process Termination

##### 2.1.4 Process Hierarchies

"In UNIX, a process and all of its children and further descendants together form a process group."

handle

##### 2.1.5 Process States

"When a process blocks, it does so because logically it cannot continue, typically because it is waiting for input that is not yet available."

##### 2.1.6 Implementation of Processes

process table, process control blocks, interrupt vector

##### 2.1.7 Modeling Multiprogramming

"When multiprogramming is used, the CPU utilization can be improved."

degree of multiprogramming

#### 2.2 THREADS

##### 2.2.1 Thread Usage

threads

"By decomposing such an application into multiple sequential threads that run in quasi-parallel, the programming model becomes simpler."

"Instead, of thinking about interrupts, timers, and context switches, we can think about parallel processes."

"Only now with threads we add a new element: the ability for the parallel entities to share an address space and all of its data among themselves."

"This ability is essential for certain applications, which is why having multiple processes (with their separate address spaces) will not work."

cache, dispatcher, worker thread, finite-state machine

##### 2.2.2 The Classical Thread Model

thread, lightweight processes, multithreading

"Since every thread can access every memory address within the process' address space, one thread can read, write, or even wipe out another thread's stack."

"There is no protection between threads because (1) it is impossible, and (2) it should not be necessary."

##### 2.2.3 POSIX Threads

Pthreads

##### 2.2.4 Implementing Threads in User Space

"There are two main places to implement threads: user space and the kernel."

thread table, jacket, wrapper

"Another, and really the most devastating, argument against user-level threads is that programmers generally want threads precisely in applications where the threads block often, as, for example, in a multithreaded Web server."

##### 2.2.5 Implementing Threads in the Kernel

"When a thread wants to create a new thread or destroy an existing thread, it makes a kernel call, which then does the creation or destruction by updating the kernel thread table."

##### 2.2.6 Hybrid Implementations

##### 2.2.7 Scheduler Activations

scheduler activations, upcall

##### 2.2.8 Pop-Up Threads

pop-up thread

##### 2.2.9 Making Single-Threaded Code Multithreaded

"Local variables and parameters do not cause any trouble, but variables that are global to a thread but not global to the entire program are a problem."

#### 2.3 INTERPROCESS COMMUNICATION

InterProcess Communication, IPC

##### 2.3.1 Race Conditions

spooler directory, printer daemon

"Situations like this, where two or more processes are reading or writing some shared data and the final result depends on who runs precisely when, are called race conditions."

##### 2.3.2 Critical Regions

mutual exclusion, critical region, critical section

##### 2.3.3 Mutual Exclusion with Busy Waiting

Disabling Interrupts

"On a single-processor system, the simplest solution is to have each process disable all interrupts just after entering its critical region and re-enable them just before leaving it."

"This approach is generally unattractive because it is unwise to give user processes the power to turn off interrupts."

Lock Variables

"Unfortunately, this idea contains exactly the same fatal flaw that we saw in the spooler directory."

Strict Alternation

"C is powerful, efficient, and predictable, characteristics critical for writing operating systems."

busy waiting, spin lock

"This situation violates condition 3 set out above: process 0 is being blocked by a process not in its critical region."

Peterson's Solution

"By combining the idea of taking turns with the idea of lock variables and warning variables, a Dutch mathematician, T. Dekker, was the first one to devise a software solution to the mutual exclusion problem that does not require strict alternation."

The TSL Instruction

"It is important to note that locking the memory bus is very different from disabling interrupts."

"In other words, critical regions work only if the processes cooperate."

##### 2.3.4 Sleep and Wakeup

priority inversion problem, The Producer-Consumer Problem, producer-consumer, bounded-buffer, wakeup waiting bit

##### 2.3.5 Semaphores

semaphore, atomic action

"This atomicity is absolutely essential to solving synchronization problems and avoiding race conditions."

Solving the Producer-Consumer Problem Using Semaphores

"This solution uses three semaphores: one called full for counting the number of slots that are full, one called empty for counting the number of slots that are empty, and one called mutex to make sure the producer and consumer do not access the buffer at the same time."

binary semaphores

"The mutex semaphore is used for mutual exclusion."

synchronization

##### 2.3.6 Mutexes

"Mutexes are good only for managing mutual exclusion to some shared resource or piece of code."

mutex, Futexes, futex

"A futex consists of two parts: a kernel service and a user library."

Mutexes in Pthreads, condition variables

##### 2.3.7 Monitors

monitor, condition variables

"The conclusion is that semaphores are too low level and monitors are not usable except in a few programming languages."

##### 2.3.8 Message Passing

message passing, Design Issues for Message-Passing Systems, acknowledgement

"It is essential that the receiver be able to distinguish a new message from the retransmission of an old one."

Authentication, The Producer-Consumer Problem with Message Passing, mailbox, rendezvous

"Message passing is commonly used in parallel programming systems."

MPI, Message-Passing Interface

##### 2.3.9 Barriers

barrier

"When all of them are done, the new matrix (the input to the next iteration) will be finished, and all processes will be simultaneously released to start the next iteration."

##### 2.3.10 Avoiding Locks: Read-Copy-Update

RCU, Read-Copy-Update, read-side critical section, grace period

#### 2.4 SCHEDULING

scheduler, scheduling algorithm

"Many of the same issues that apply to process scheduling also apply to thread scheduling, although some are different."

##### 2.4.1 Introduction to Scheduling

"In addition to picking the right process to run, the scheduler also has to worry about making efficient use of the CPU because process switching is expensive."

Process Behavior, compute-bound, CPU-bound, I/O-bound

"Compute-bound processes typically have long CPU bursts and thus infrequent I/O waits, whereas I/O-bound processes have short CPU bursts and thus frequent I/O waits."

"It is worth noting that as CPUs get faster, processes tend to get more I/O-bound."

When to Schedule, nonpreemptive, preemptive, Categories of Scheduling Algorithms, Scheduling Algorithm Goals, Throughput, Turnaround time, response time, proportionality

##### 2.4.2 Scheduling in Batch Systems

First-Come, First-Served, first-come, first-served

"It is also fair in the same sense that allocating scarce concert tickets or brand-new iPhones to people who are willing to stand on line starting at 2 A.M. is fair."

Shortest Job First, shortest job first

"It is worth pointing out that shortest job first is optimal only when all the jobs are available simultaneously."

Shortest Remaining Time Next, shortest remaining time next

##### 2.4.3 Scheduling in Interactive Systems

Round-Robin Scheduling, round robin, quantum, process switch, context switch, Priority Scheduling, priority scheduling

"To prevent high-priority processes from running indefinitely, the scheduler may decrease the priority of the currently running process at each clock tick (i.e., at each clock interrupt)."

Multiple Queues, Shortest Process Next, aging, Guaranteed Scheduling, Lottery Scheduling, lottery scheduling, Fair-Share Scheduling

##### 2.4.4 Scheduling in Real-Time Systems

real-time, hard real time, soft real time, periodic, aperiodic, schedulable

"Static scheduling works only when there is perfect information available in advance about the work to be done and the deadlines that have to be met."

##### 2.4.5 Policy Versus Mechanism

scheduling mechanism, scheduling policy

##### 2.4.6 Thread Scheduling

"In practice, round-robin scheduling and priority scheduling are most common."

#### 2.4 CLASSICAL IPC PROBLEMS

##### 2.5.1 The Dining Philosophers Problem

dining philosophers problem