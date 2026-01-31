- Explain process states (running, sleeping, zombie, etc.)

A process state describes what a process is currently doing from the kernel’s point of view — whether it’s executing, waiting, stopped, or finished.

Linux process states are visible via tools like:

ps aux

top

htop

- Primary Linux process states :-

R — Running / Runnable --> The process is: Actively executing on a CPU or ready to run and waiting in the run queue

S — Interruptible Sleeping --> Waiting for an event to occur , Can be woken up by:I/O completion , Signals , Timers . its very common and normal . some examples :- Waiting for user input , Network requests

D — Uninterruptible Sleeping

  Waiting on kernel I/O , Cannot be interrupted by signals (even SIGKILL) , Process resumes only when the kernel operation finishes , Usually indicates problems if persistent.
  Common causes :- Disk I/O stalls , NFS hangs , Hardware or driver issues

T — Stopped:- Process execution is paused , Still loaded in memory . 
Caused by :- Ctrl + Z , Debugger breakpoints , SIGSTOP / SIGTSTP
=> Resumed using: fg

kill -CONT <pid>

Z — Zombie --> Process has terminated , Parent process has not yet read its exit status

Important facts --> Uses no CPU , Uses no memory , Exists only as a process table entry 

Why zombies exist --> Parent must call wait() to clean up , Kernel retains exit code temporarily 

X — Dead --> Process is fully removed from the system , Rarely visible to users

- Process state lifecycle

  New--> Running (R)--> Sleeping (S / D)--> Stopped (T)--> Zombie (Z)-->Dead (X)

  - Why process states matter :- Many R → CPU saturation , Many S → healthy waiting , Persistent D → I/O or storage issue , Many Z → bad process management

