Multiprogramming increases CPU utilization by ensuring that the CPU always has a job to execute. The operating system keeps multiple jobs in memory simultaneously. Initially, these jobs are stored on the disk in the job pool because main memory cannot accommodate all of them.

In a multi-programmed system, the operating system selects and starts executing one of the jobs in memory. If a job needs to wait for an I/O operation or any other task, the CPU switches to another job. This process continues, and when the first job finishes waiting, it regains the CPU. As long as there is at least one job to execute, the CPU remains busy and never sits idle.

Time sharing, also known as multitasking, is an extension of multiprogramming. In time-sharing systems, the CPU switches among multiple jobs, allowing users to interact with each program while it is running. It requires an interactive computer system that enables direct communication between the user and the system.

A time-shared operating system facilitates many users sharing the computer simultaneously. Since actions or commands in a time-shared system are typically short, each user requires only a small portion of CPU time. The system rapidly switches between users, giving each user the impression that they have dedicated use of the entire computer system.

Time sharing and multiprogramming necessitate keeping several jobs in memory. If there are more jobs ready to be brought into memory than available space, the system must choose among them. This decision-making process is known as job scheduling. Additionally, if multiple jobs are ready to run simultaneously, the system must determine which job will run first, which involves CPU scheduling.

[[Operating System Overview 3]]

---