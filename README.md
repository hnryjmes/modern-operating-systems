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

