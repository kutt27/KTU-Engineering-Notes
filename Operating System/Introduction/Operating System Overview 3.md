**Interrupt-driven Nature of Operating Systems**
- Events in modern operating systems are signaled by interrupts or traps.
- Traps are software-generated interrupts caused by errors or user program requests.
- Interrupt service routines (ISRs) handle interrupts and determine how to handle them.

**Dual Mode and Multi-Mode Operations**
- Operating systems have two modes: user mode and kernel mode.
- User mode is for executing user applications, while kernel mode is for operating system tasks.
- Transition from user to kernel mode occurs when a user application requests a service.
- Hardware switches between user mode and kernel mode during traps or interrupts.

**Protection and Privileged Instructions**
- Dual mode operation protects the operating system from users and users from each other.
- Privileged instructions, executed only in kernel mode, are designated as potential harm-causing instructions.
- Attempting to execute privileged instructions in user mode results in a trap to the operating system.

**Virtualization and Extended Modes**
- Virtualization allows operating systems to run as applications within other operating systems.
- CPUs supporting virtualization often have a separate mode for the virtual machine manager (VMM).
- CPUs may have multiple privilege levels or use other methods to differentiate operational privileges.

**System Calls**
- System calls allow user programs to request operating system tasks on their behalf.
- Invoked through traps or interrupt vectors, they pass parameters to the operating system.
- System-call service routines in the kernel execute the requested service and return control.

**Timer for CPU Control**
- A timer ensures the operating system maintains control over the CPU.
- It can be set to interrupt the computer after a specified period.
- Timers prevent user programs from running indefinitely by terminating them after a set time limit.

---