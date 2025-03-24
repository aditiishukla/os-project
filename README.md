This is our group project of Operating Systems, in which we have made Intelligent CPU Scheduler Simulator.
In this project, we have develop a simulator for CPU scheduling algorithms (FCFS, SJF, Round Robin, Priority Scheduling) with real-time visualizations. 
This simulator allow users to input processes with arrival times, burst times, and priorities and visualize Gantt charts and performance metrics like average waiting time and turnaround time.

Introduction:
The Intelligent CPU Scheduler Simulator is designed to simulate different CPU scheduling algorithms (FCFS, SJF, Round Robin, and Priority Scheduling) with real-time visualizations. The simulator takes process details as input (arrival time, burst time, priority) and generates a Gantt chart while calculating essential performance metrics such as waiting time, turnaround time, and response time.

Steps in which our simulator is working:

Step 1: User Input Handling
The user enters process details such as Process ID, Arrival Time(when the process arrives in the ready queue), Burst Time(total execution time required),Priority (only for priority scheduling),Time Quantum(applicable only for Round Robin scheduling).
The input is validated to ensure correct values (e.g., arrival times are non-negative, burst times are positive).

Step 2: Choosing the Scheduling Algorithm
The user selects one of the following CPU scheduling algorithms:
1)First Come First Serve (FCFS)- Processes are executed in the order they arrive.
 Non-preemptive (once a process starts, it cannot be interrupted).
2)Shortest Job First (SJF)- The process with the shortest burst time is executed first.
 It can be both preemptive (SRTF) or non-preemptive.
3)Round Robin (RR)- Each process is assigned a fixed time quantum.
If a process does not finish within the quantum, it is moved to the back of the queue.
It is only preemptive (processes are interrupted after each quantum).
4)Priority Scheduling- The process with the highest priority is executed first.
It can be both preemptive or non-preemptive.

Step 3: Process Scheduling and Execution
Based on the chosen algorithm, the processes are arranged in a queue for execution.
The CPU executes processes in order, updating the system clock and calculating turnaround times, waiting times, and response times.
In case of preemptive scheduling (SRTF, Priority, or Round Robin), the scheduler constantly checks for new processes or time quantum expirations.

Step 4: Gantt Chart Generation A Gantt chart is dynamically created, showing when each process starts and ends.
This provides a visual representation of process execution.

Step 5: Performance Metrics Calculation The simulator computes the following performance metrics:
Turnaround Time (TAT): TAT=CompletionTime−ArrivalTime Measures how long each process takes from arrival to completion.
Waiting Time (WT): WT=TurnaroundTime−BurstTime Measures the total time a process spends waiting in the ready queue.
Response Time (RT): RT=FirstCPUExecutionTime−ArrivalTime Time taken for the CPU to start executing a process for the first time.
CPU Utilization:=(Total CPU Time / Simulation Time) × 100 Measures how effectively the CPU is utilized.

Step 6: Displaying Results and Visualization
The final output consists of:
Gantt chart (Graphical representation of execution order).
Performance metrics table (TAT, WT, RT for each process).
Comparison of algorithms (for better decision-making).

Example Output Table:
Process	Arrival Time	Burst Time	Completion Time	Turnaround Time	Waiting Time	Response Time
P1	        0	              5	            10	            10	          5	            0
P2	        1	              3	            13	            12	          9	            3

3. Features of the Simulator
1) Real-Time Visualization:- Gantt charts are dynamically updated as the processes execute.
2) User-Friendly Interface:- Simple input fields for process details.
3) Performance Analysis:- Also provides efficiency metrics to compare scheduling algorithms.
4) Supports Preemptive & Non-Preemptive Scheduling:- It allows a realistic simulation of different scenarios.

5. Future Enhancements
1)Dynamic process addition (Add new processes at runtime).
2)Multi-core CPU scheduling (Simulate modern processor behavior).
3)AI-based algorithm selection (Choose the best algorithm dynamically based on workload).
4)Cloud-based deployment (Run simulations online without installation).

6. Conclusion
The Intelligent CPU Scheduler Simulator provides a powerful interactive learning experience for understanding CPU scheduling. By implementing various algorithms and offering real-time insights, the project helps users visualize scheduling behavior and compare algorithm efficiency. Future enhancements can make it even more dynamic and applicable in real-world systems.
