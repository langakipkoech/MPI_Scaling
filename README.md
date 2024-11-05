# MPI_Scaling
Amdahls law -- Strong scaling/ Weak scaling
Strong Scaling and Weak Scaling are two important concepts in parallel computing that describe how performance and efficiency change when adjusting the workload and the number of processors.
Strong Scaling

Definition: In strong scaling, the total problem size (i.e., the amount of work) remains constant while the number of processors increases. The goal is to see how much faster the same problem can be solved with more computing resources.

    Objective: To reduce the time required to solve a fixed-size problem by increasing the number of processors.

    Ideal Outcome: If the workload is split perfectly, doubling the processors should ideally halve the computation time.

    Limitations: As the number of processors increases, the benefit of adding more processors starts to diminish due to factors like communication overhead, synchronization, and load balancing. This diminishing return is often described by Amdahl’s Law.

    Example: Imagine simulating the weather over a fixed grid size for a single day. By increasing the number of processors, we aim to reduce the time needed for this simulation, but the workload (grid size) remains the same.

Weak Scaling

Definition: In weak scaling, the problem size increases proportionally with the number of processors. The goal is to see if the computing time remains constant as both the workload and the number of processors increase together.

    Objective: To keep the execution time constant while increasing the problem size and number of processors proportionally.

    Ideal Outcome: The computation time should ideally remain the same as we increase both the workload and the processors. This scaling scenario is often limited by Gustafson’s Law.

    Limitations: Communication and synchronization overhead may still increase with the number of processors, but it tends to be less impactful in weak scaling than in strong scaling.

    Example: Imagine simulating the weather for a larger region (say, doubling the grid size) as you double the number of processors. If the simulation time remains roughly constant, then the system exhibits good weak scaling.

Summary Comparison
Scaling Type	Fixed Variable	Variable Increase	Goal
Strong	Problem size (workload)	Number of processors	Reduce time for fixed workload
Weak	Workload per processor	Problem size & processors	Keep time constant with larger workload
Key Points

    Strong Scaling is about doing the same amount of work faster by using more processors.
    Weak Scaling is about handling a proportionally larger problem size with more processors without increasing the time.

Both types of scaling are crucial for understanding and optimizing performance in parallel computing systems, and they help guide how to best utilize additional computational resourc
