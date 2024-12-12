**Real-Time Task Scheduling in Embedded Linux**

***Project Overview***

This project demonstrates real-time task scheduling in an embedded Linux environment using pthreads. Three tasks are executed with different periodic intervals and priorities to simulate real-time operations. The code implements features such as periodic task execution, deadline checking, and mutex-based resource locking.

***Features***

Real-time scheduling policies (Rate Monotonic and Priority Inversion).

Support for single-core and multi-core configurations.

Tasks simulate workload and manage deadlines with periodic execution.

System Requirements

Simulated Hardware: Raspberry Pi machine (simulated).

***Software:***

GCC Compiler.

Real-time enabled Linux kernel (PREEMPT_RT patch preferred).

**Getting Started**

***Prerequisites***

Ensure the following tools are installed on your simulated Raspberry Pi environment:

gcc (GNU Compiler Collection)

make (Optional for automated builds)

Install required tools using:

sudo apt update
sudo apt install gcc make

Cloning the Repository

Clone the project repository (if hosted online) or transfer the code file (embeddedlinux.c) to your simulated environment.

Compiling the Code

Open a terminal in your simulated environment.

Navigate to the directory containing the embeddedlinux.c file.

Compile the code using the following command:

gcc -pthread -o embeddedlinux embeddedlinux.c

Running the Code

Ensure you have real-time scheduling permissions. Run:

sudo su

to switch to the root user or use sudo before executing the program.

Execute the compiled program:

sudo ./embeddedlinux

Observe the task logs in the terminal, including deadline compliance and resource access.

Explanation of Configuration Options

The program is configurable via macros defined in embeddedlinux.c:

Scheduling Policy:

RATE_MONOTONIC: Default scheduling policy.

PRIORITY_INVERSION: Enables resource locking.

Core Affinity:

SINGLE_CORE or MULTIPLE_CORES.

Task Periods: Configurable via TASK1_INTERVAL_US, TASK2_INTERVAL_US, and TASK3_INTERVAL_US.

Workload: Adjusted by changing INNER_LOOP_COUNT_FIXED or INNER_LOOP_COUNT_VARIABLE.

Stopping the Program

To terminate the program, press Ctrl + C in the terminal.

Troubleshooting

Permission Denied Errors: Ensure you are running the program as a root user (sudo).

***Real-Time Performance Issues:***

Verify if the Linux kernel has real-time support (uname -a).

Use tools like htop to monitor CPU usage and core affinity.

Compilation Errors: Ensure all dependencies are installed and the gcc version supports pthreads.

**Author**

Ahmed Osama Saad Yassin
