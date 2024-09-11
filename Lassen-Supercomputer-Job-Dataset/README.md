### Dataset Overview:

This dataset is associated with our publication titled 
"Monitoring Large Scale Supercomputers: A Case Study with the Lassen Supercomputer", 
which was published at the IEEE Cluster conference in 2021 (DOI:10.1109/Cluster48925.2021.00057). 
Please cite this paper when using this dataset. 

The dataset contains logs from 1.4 million jobs over multiple years from the Lassen supercomputer 
at Lawrence Livermore National Laboratory, obtained through IBM's Cluster System Management (CSM) framework. 

The three files are:

- `final_csm_allocation_history.csv`: Contains job-level information about node allocations.
- `final_csm_allocation_node_history.csv`: Contains node-level information about jobs.
- `final_csm_step_history.csv`: Contains the final disposition of jobs.

The fields of each table are described as part of the documentation for the IBM CSM 
framework (https://cast.readthedocs.io/en/latest/csm/csmdb/csm_db_appendix.html#tables). 

All identifying information has been stripped from this dataset. 


### Table Descriptions:

The `csm_allocation_history` table contains job-level
information such as the ID for the allocation; the details
of the user, the application script and the account associated
with the job. It also contains the number of nodes and GPUs
requested; the submission, begin and end times; and its exit
status (e.g., complete or failed). For this table,
the number of GPUs were always reported as zero by IBM CSM, and these were
captured as part of the `csm_step_history` table instead.

The `csm_allocation_node_history` table contains
per-node details for each job allocation. This data includes
the energy values for the node and the GPUs, GPFS reads
and writes, InfiniBand transactions transmitted and received,
power cap, power shifting ratio, CPU/memory usage, etc.


The `csm_step_history` table contains details for job
steps for allocations that have designated steps. The attributes
in this table include the ID of the step within an allocation, the
step-level processor count and GPU usage, OpenMP threads, projected memory, and time for each job step. 

The specific headers that are included in the dataset are shown below. 

```
==> final_csm_allocation_history.csv <==
allocation_id,primary_job_id,launch_node_name,isolated_cores,user_flags,system_flags,ssd_min,
ssd_max,num_nodes,num_processors,num_gpus,projected_memory,type,job_type,hashed_user_id,hashed_user_group_id,
begin_time,end_time,exit_status,job_submit_time,queue,requeue,time_limit,smt_mode,core_blink

==> final_csm_allocation_node_history.csv <==
allocation_id,node_name,shared,energy,gpfs_read,gpfs_write,ib_tx,ib_rx,power_cap,power_shifting_ratio,
power_cap_hit,gpu_usage,gpu_energy,cpu_usage,memory_usage_max

==> final_csm_step_history.csv <==
allocation_id,step_id,begin_time,end_time,num_nodes,num_processors,num_gpus,num_tasks,
projected_memory,user_flags,exit_status,total_u_time,total_s_time,omp_thread_limit
```

### License
Creative Commons Attribution 4.0 International Public License

Release Number: LLNL-MI-861648

