Etiquette for using shared computational resources
==================================================

If you've never used a shared high performance computing (HPC) resource before, you may have some general questions about what is appropriate that is not already covered in the [TACC usage policy](https://portal.tacc.utexas.edu/tacc-usage-policy). Here are a few frequently asked questions:

###What type of jobs should I run on the cluster?
Reasons you may be motivated to use a remote computational resource include the following:
* The software you would like to use is only available on a cluster, or is difficult to install on your own computer.
* The jobs you would like to run require large amounts of computational processing power and/or disk space, and your desktop computers cannot meet these needs.
* You need to analyze data that is protected by [HIPPA](http://www.dhcs.ca.gov/formsandpubs/laws/hipaa/Pages/1.00WhatisHIPAA.aspx) and your own computer is not secure.

Examples of jobs that may require the use of a cluster include (but are not limited to): genome assembly, phylogenetics, simulation, modeling.

###How do I decide how to run programs?
After [logging on](logon.md) to Stampede, you will see "login" listed in your command prompt. This means the commands you run will occur on the login nodes. These are shared by everyone, so you should not run memory intensive jobs on the login node. Examples of acceptable use on login nodes include:
* compressing/uncompressing: `tar`, `zip`
* data transfer: `cp`, `mv`, `scp`
* software compilation and installation

Please note that these tasks should be run one at a time, so as to not overwhelm the processor with your jobs.

For all other jobs, you can run a job on a single or multiple compute nodes:
* submit a job via a queue using `slurm` (see below)
* run an interactive job using `idev`

###Which queue should I use?
There are multiple [queues](https://portal.tacc.utexas.edu/user-guides/stampede#running-slurm-queue) available on Stampede, and choice of a queue depends on your job. Here is a general description for using a few queues:
* development: Use this queue to test whether your scripts are working properly. There are generally many fewer jobs in this queue, so your job should start running fairly soon after submission. However, you can only have one job submitted to the development queue at a time, and a job can only run a few hours. 
* normal: Use this queue for most jobs. Depending on how many others are using this queue, your job may start running within a few minutes, or may wait several hours in the queue. You can have up to 50 jobs in the normal queue at a time, and each job can run for a few days.
* largemem: Use this queue for memory-intensive tasks (like genome assembly). Job run time is similar to the normal queue, but you can only have a few jobs in the largemem queue at once. Note that jobs run in this queue have a higher charge rate (i.e., jobs use more SUs, see [account.md](https://portal.tacc.utexas.edu/user-guides/stampede#running-slurm-queue) for more information) than other queues.
