[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Daf--GaW)
# Non-Preemptive Priority CPU Scheduling (Higher Value = Higher Priority)

## Overview

This project implements the **Non-Preemptive Priority Scheduling algorithm** using the C programming language. The program simulates how an operating system schedules processes based on their priority values.

In this implementation, **a higher priority value means higher priority**. The CPU selects the process with the highest priority among the processes that have already arrived.

Once a process starts executing, it runs **until completion** because the scheduling is **non-preemptive**.

---

## Features

* Accepts multiple processes as input
* Uses **priority scheduling**
* Calculates:

  * Waiting Time (WT)
  * Turnaround Time (TAT)
  * Average Waiting Time
  * Average Turnaround Time
* Simulates CPU execution order

---

## Process Structure

```c
struct process{
    char pid[10];
    int at, bt, pr;
    int ct, wt, tat;
    int done;
};
```

Where:

* **pid** → Process ID
* **at** → Arrival Time
* **bt** → Burst Time
* **pr** → Priority
* **ct** → Completion Time
* **wt** → Waiting Time
* **tat** → Turnaround Time
* **done** → Process completion status

---

## Input Format

First enter the **number of processes**, followed by each process detail.

```
n
PID ArrivalTime BurstTime Priority
```

Example:

```
3
P1 0 5 2
P2 1 3 1
P3 2 4 3
```

---

## Output

The program prints:

* Waiting time for each process
* Turnaround time for each process
* Average waiting time
* Average turnaround time

Example:

```
Waiting Time:
P1 0
P2 8
P3 3

Turnaround Time:
P1 5
P2 11
P3 7

Average Waiting Time: 3.67
Average Turnaround Time: 7.67
```

---

## How to Compile

```bash
gcc priority.c -o priority
```

---

## How to Run

Windows:

```bash
priority.exe
```

Linux / Mac:

```bash
./priority
```

---

## Concepts Used

* CPU Scheduling
* Non-Preemptive Scheduling
* Priority Scheduling
* Waiting Time Calculation
* Turnaround Time Calculation

---

## Author

Allen Saji
