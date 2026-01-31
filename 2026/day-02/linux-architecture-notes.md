- Day 02 – Linux Architecture, Processes, and systemd
- Today’s goal is to understand how Linux works under the hood.
- 1. From power button → Linux kernel
Boot sequence (high level)

BIOS / UEFI

Initializes hardware (CPU, RAM, disks)

Finds a bootable device

Bootloader (usually GRUB)

Lets you pick a kernel

Loads the Linux kernel into memory

Passes kernel parameters

Kernel starts

Decompresses itself

Initializes CPU, memory, drivers

Mounts the root filesystem

Starts the first process:
init (PID 1) → usually systemd

At this point, Linux is alive.

- 2. The Linux kernel (the boss)

The kernel is the core of Linux.
It runs in kernel space (full hardware access).

What the kernel actually does

Process management

Memory management

Device drivers

File systems

Networking

Security & permissions

Main point :- User programs never talk to hardware directly.
They go through the kernel.

- 3. User space vs Kernel space
     
🔒 Kernel space

Full access to CPU, memory, devices

One bug = whole system crash

Kernel + drivers live here

🧑‍💻 User space

Your apps, shells, services

Limited permissions

Isolated from each other

Apps request kernel help via system calls.

Example:

ls → open() → read() → write()
        ↑
     system call

- 4. Processes & scheduling
What is a process?

A process is:

Program code

Memory

Open files

Security context

PID

Kernel scheduler

Linux uses a preemptive multitasking scheduler:

Rapidly switches between processes

Gives the illusion of parallelism

Fairly distributes CPU time

Modern Linux uses CFS (Completely Fair Scheduler).

- 5. Memory management (the sneaky genius part)
Virtual memory

Each process thinks it owns:

Its own RAM

Its own address space

Reality:

Kernel maps virtual memory → physical RAM

Uses page tables

Swaps to disk when RAM is full

Key concepts

Pages (usually 4KB)

Page cache (file caching)

Copy-on-write (fork is cheap!)

OOM killer (when memory runs out 😬)

- 6. Filesystem (everything is a file)

Linux follows a huge idea:

Everything is a file

That includes:

Regular files

Directories

Disks (/dev/sda)

Network sockets

Processes (/proc)

VFS (Virtual File System)

Abstract layer inside the kernel

Lets ext4, XFS, Btrfs, NFS all behave the same

- 7. Devices & drivers
Device drivers

Live in kernel space

Translate generic kernel calls → hardware actions

Types:

Character devices (keyboard, serial)

Block devices (disks)

Network devices

Hotplug works via:

udev

sysfs (/sys)

- 8. Networking stack

Linux has a full TCP/IP stack in the kernel.

Flow:

App → socket() → kernel TCP/IP → NIC driver → wire


Supports:

Namespaces (containers!)

iptables / nftables

Routing tables

Load balancing

This is why Linux dominates servers.

- 9. systemd (PID 1)

Once kernel hands control to user space:

systemd handles:

Starting services

Dependency management

Logging (journald)

Timers, mounts, networking

Everything becomes a unit:

service

socket

mount

timer

- 10. Security model
Users & permissions

UID / GID

rwx permissions

capabilities (fine-grained root powers)

Isolation tools

Namespaces (process, network, mount)

cgroups (CPU, memory limits)

SELinux / AppArmor

This is the foundation of containers.

- 11. Why Linux is perfect for DevOps & Cloud

Because under the hood Linux gives you:

Deterministic behavior

Powerful automation

Resource isolation

Transparent observability

Battle-tested networking

Docker, Kubernetes, cloud VMs—all ride on Linux internals.
