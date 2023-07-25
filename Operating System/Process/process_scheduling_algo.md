
**Comprehensive Guide to Scheduling Algorithms and Examples**

Scheduling algorithms are an essential part of operating systems, responsible for efficiently managing the execution of processes on the CPU. In this guide, we'll explore four common scheduling algorithms: First-Come-First-Serve (FCFS), Shortest Job First (SJF), Priority Scheduling, and Round Robin Scheduling. We'll cover both preemptive and non-preemptive versions of these algorithms. Let's begin!

**1. First-Come-First-Serve (FCFS) Scheduling:**
- FCFS is one of the simplest scheduling algorithms. It schedules processes in the order they arrive in the ready queue.
- Non-preemptive FCFS: Once a process starts executing, it continues until it completes its burst time.
- Preemptive FCFS: Not applicable as FCFS is inherently non-preemptive.

**Example with Quantum Time (Non-Preemptive):**
Let's consider five processes with their arrival times and burst times:

| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1      | 0            | 6          |
| P2      | 1            | 3          |
| P3      | 2            | 8          |
| P4      | 3            | 4          |
| P5      | 4            | 5          |

1. Arrange the processes based on their arrival time: P1, P2, P3, P4, P5.
2. Calculate waiting time and turnaround time for each process:
   - Waiting Time (WT): Time spent waiting in the ready queue.
   - Turnaround Time (TAT): Time taken from arrival to completion.

| Process | Burst Time | Arrival Time | Completion Time | TAT | WT |
|---------|------------|--------------|-----------------|-----|----|
| P1      | 6          | 0            | 6               | 6   | 0  |
| P2      | 3          | 1            | 9               | 8   | 5  |
| P3      | 8          | 2            | 17              | 15  | 7  |
| P4      | 4          | 3            | 21              | 18  | 14 |
| P5      | 5          | 4            | 26              | 22  | 17 |

3. Calculate the average turnaround time and waiting time:
   - Average Turnaround Time = (TAT_P1 + TAT_P2 + TAT_P3 + TAT_P4 + TAT_P5) / Number of Processes
   - Average Waiting Time = (WT_P1 + WT_P2 + WT_P3 + WT_P4 + WT_P5) / Number of Processes

   - Average Turnaround Time = (6 + 8 + 15 + 18 + 22) / 5 = 13.8 units
   - Average Waiting Time = (0 + 5 + 7 + 14 + 17) / 5 = 8.6 units

**2. Shortest Job First (SJF) Scheduling:**
- SJF schedules processes based on their burst time, choosing the shortest job first.
- Non-preemptive SJF: Once a process starts executing, it continues until it completes its burst time.
- Preemptive SJF: If a new process with a shorter burst time arrives, it preempts the currently running process.

**Example with Quantum Time (Non-Preemptive):**
Let's consider the same five processes with their arrival times and burst times:

| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1      | 0            | 6          |
| P2      | 1            | 3          |
| P3      | 2            | 8          |
| P4      | 3            | 4          |
| P5      | 4            | 5          |

1. Arrange the processes based on their arrival time: P1, P2, P3, P4, P5.
2. Calculate waiting time and turnaround time for each process:
   - Waiting Time (WT): Time spent waiting in the ready queue.
   - Turnaround Time (TAT): Time taken from arrival to completion.

| Process | Burst Time | Arrival Time | Completion Time | TAT | WT |
|---------|------------|--------------|-----------------|-----|----|
| P1      | 6          | 0            | 6               | 6   | 0  |
| P2      | 3          | 1            | 9               | 8   | 5  |
| P4      | 4          | 3            | 13              | 10  | 6  |
| P5      | 5          | 4            | 18              | 14  | 9  |
| P3      | 8          | 2            | 26              | 24  | 16 |

3. Calculate the average turnaround time and waiting time:
   - Average Turnaround Time = (TAT_P1 + TAT_P2 + TAT_P3 + TAT_P4 + TAT_P5) / Number of Processes
   - Average Waiting Time = (WT_P1 + WT_P2 + WT_P3 + WT_P4 + WT_P5) / Number of Processes

   - Average Turnaround Time = (6 + 8 + 24 + 10 + 14) / 5 = 12.4 units
   - Average Waiting Time = (0 + 5 + 16 + 6 + 9) / 5 = 7.2 units

**3. Priority Scheduling:**
- Priority Scheduling assigns priorities to processes based on factors like priority numbers, age, etc.
- Non-preemptive Priority Scheduling: Once a process starts executing, it continues until it completes its burst time.
- Preemptive Priority Scheduling: If a new process with a higher priority arrives, it preempts the currently running process.

**Example with Quantum Time (Non-Preemptive):**
Let's consider the same five processes with their arrival times, burst times, and priorities:

| Process | Arrival Time | Burst Time | Priority |
|---------|--------------|------------|----------|
| P1      | 0            | 6          | 3        |
| P2      | 1            | 3          | 1        |
| P3      | 2            | 8          | 4        |
| P4      | 3            | 4          | 2        |
| P5      | 4            | 5          | 5        |

1. Arrange the processes based on their priorities (lower value indicates higher priority): P2, P4, P1, P3, P5.
2. Calculate waiting time and turnaround time for each process:
   - Waiting Time (WT): Time spent waiting in the ready queue.
   - Turnaround Time (TAT): Time taken from arrival to completion.

| Process | Burst Time | Arrival Time | Completion Time | TAT | WT |
|---------|------------|--------------|-----------------|-----|----|
| P2      | 3          | 1            | 4               | 3   | 0  |
| P4      | 4          | 3            | 8               | 5   | 1  |
| P1      | 6          | 0            | 14              | 14  | 8  |
| P3      | 8          | 2            | 22              | 20  | 12 |
| P5      | 5          | 4            | 27              | 23  | 18 |

3. Calculate the average turnaround time and waiting time:
   - Average Turnaround Time = (TAT_P2 + TAT_P4 + TAT_P1 + TAT_P3 + TAT_P5) / Number of Processes
   - Average Waiting Time = (WT_P2 + WT_P4 + WT_P1 + WT_P3 + WT_P5) / Number of Processes

   - Average Turnaround Time = (3 + 5 + 14 + 20 + 23) / 5 = 13.0 units
   - Average Waiting Time = (0 + 1 + 8 + 12 + 18) / 5 = 7.8 units

**4. Round Robin Scheduling:**
- Round Robin Scheduling assigns a fixed time slice (quantum time) to each process in the ready queue.
- Non-preemptive Round Robin: Not applicable as Round Robin is inherently preemptive.
- Preemptive Round Robin: If a process doesn't complete its execution in the quantum time, it's preempted and placed back in the ready queue.

**Example with Quantum Time (Preemptive):**
Let's consider the same five processes with their arrival times and burst times. Assume a quantum time of 4 seconds.

| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1      | 0            | 6          |
| P2      | 1            | 3          |
| P3      | 2            | 8          |
| P4      | 3            | 4          |
| P5      | 4            | 5          |

1. Arrange the processes based on their arrival time: P1, P2, P3, P4, P5.
2. Apply Round Robin with a quantum time of 4 seconds:

| Time     | Process | Remaining Burst Time |
|----------|---------|----------------------|
| 0 - 4    | P1      | 2                    |
| 4 - 7    | P2      | 0 (Completed)        |
| 7 - 11   | P3      | 5                    |
| 11 - 15  | P4      | 0 (Completed)        |
| 15 - 19  | P5      | 1                    |
| 19 - 23  | P1      | 0 (Completed)        |
| 23 - 27  | P3      | 1                    |
| 27 - 31  | P5      | 0 (Completed)        |
| 31 - 32  | P3      | 0 (Completed)        |

3. Calculate waiting time and turnaround time for each process:
   - Waiting Time (WT): Time spent waiting in the ready queue.
   - Turnaround Time (TAT): Time taken from arrival to completion.

| Process | Burst Time | Arrival Time | Completion Time | TAT | WT |
|---------|------------|--------------|-----------------|-----|----|
| P1      | 6          | 0            | 19              | 19  | 13 |
| P2      | 3          | 1            | 4               | 3   | 0  |
| P3      | 8          | 2            | 32              | 30  | 22 |
| P4      | 4          | 3            | 11              | 8   | 4  |
| P5      | 5          | 4            | 31              | 27  | 22 |

4. Calculate the average turnaround time and waiting time:
   - Average Turnaround Time = (TAT_P1 + TAT_P2 + TAT_P3 + TAT_P4 + TAT_P5) / Number of Processes
   - Average Waiting Time = (WT_P1 + WT_P2 + WT_P3 + WT_P4 + WT_P5) / Number of Processes

   - Average Turnaround Time = (19 + 3 + 30 + 8 + 27) / 5 = 17.4 units
   - Average Waiting Time = (13 + 0 + 22 + 4 + 22) / 5 = 12.2 units

**Calculating Average Turnaround Time and Waiting Time:**
To calculate the average turnaround time and waiting time for any scheduling algorithm, follow these steps:
1. Calculate the turnaround time (TAT) for each process: TAT = Completion Time - Arrival Time
2. Calculate the waiting time (WT) for each process: WT = TAT - Burst Time
3. Sum up the turnaround times and waiting times for all processes.
4. Divide the sums by the total number of processes to get the average turnaround time and average waiting time.

**Final Thoughts:**
Scheduling algorithms play a crucial role in ensuring efficient resource utilization in operating systems. Each algorithm has its strengths and weaknesses, and the choice of the appropriate algorithm depends on the system's requirements and workload characteristics. By understanding how these algorithms work and calculating their performance metrics, you can make informed decisions when designing or optimizing systems for better process scheduling.
