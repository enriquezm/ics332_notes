#Basic Concepts

###Objective of multiprogramming is to have some process running at all times, to maximize CPU utilization.

A process is executed until it has to wait, usually because of I/O requests. All this wait time is a waste of time for other processes that need to be executed. With multiprogramming, several processes are kept in memory at one time and when one process has to wait, the CPU is taken away and given to another process that is ready to run.

##6.1.1 CPU-I/O Burst Cycle

Process execution consists of a ```cycle``` of CPU execution and I/O wait. Processes alternate between these two states. Essentially the execution will start with a ```CPU Burst``` that is followed by an ```I/O Burst``` and so on.

- An I/O-bound program typically has many short CPU bursts.
- A CPU bound program might have a few long CPU bursts.

###6.1.2 CPU Scheduler

The ```short-term scheduler```, a selection process, selects a process from the processes in memory that are ready to execute.

A ready queue is not always a FIFO queue.

It could also be implemented as a priority queue, a tree, or an unordered linked list. The records in the queues are generally process control blocks (PCBs) of the processes.

###6.1.3 Preemptive Scheduling

CPU-scheduling can take place under the following 4 circumstances:

1. When a process switches from the running state to the waiting state.
2. When a process switches from the running state to the ready state.
3. When a process switches from the waiting state to the ready state.
4. When a process terminates.

For situations 1 and 4 there is no choice in terms of scheduling. A new process must be selected for execution.

For situations 2 and 3 there is a choice.

Nonpreemptive scheduling:

Once the CPU has beeen allocated to a process, the process keeps the CPU until it releases the CPU either by ```terminating``` or by ```switching``` to the waiting state.