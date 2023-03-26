---
title: Submit jobs to computation nodes
keywords: midway2
last_updated: March 8, 2023
tags: [midway]
summary: "This is an introduction to the HPC at UChicago, midway2."
sidebar: sidebar_1
permalink: midway2_submit.html
folder: mydoc
---

## Why you need this
As Pan lab produce tons of sequencing data, there is heavy demand of analyzing NGS and TGS data. Computation intensive jobs are supposed to run on computation nodes on midway2 and midway3.

## Scrpits
Here is an example to submit your job to midway2 computation nodes.
```
#!/bin/bash
#SBATCH --time=00:10:00
#SBATCH --account=pi-taopan
#SBATCH --nodes=1
#SBATCH --ntasks-per-node=1
#SBATCH --partition=broadwl
#SBATCH --mem-per-cpu=2000
#SBATCH --job-name=MyJob
#SBATCH --output=run1.out
#SBATCH --error=run1.err

echo “Hello”
```
And here is an example for midway3.
```
#!/bin/bash
#SBATCH --time=00:10:00
#SBATCH --account=pi-taopan
#SBATCH --nodes=1
#SBATCH --ntasks-per-node=1
#SBATCH --partition=caslake
#SBATCH --mem-per-cpu=2000
#SBATCH --job-name=MyJob
#SBATCH --output=run1.out
#SBATCH --error=run1.err

echo “Hello”
```
For the heading of the script, you could add, delete and adjust the items needed. I often include the following two lines in the heading so that you could get an email notification when your job starts to run and ends running. However, this function sometimes doesn't work when RCC is repairing the cluster.
```
#SBATCH --mail-user=cnetID@uchicago.edu
#SBATCH --mail-type=ALL
```
### explanation of the items
`account`, the account that pays for your jobs.

`partition`, the type of nodes you would like to run your job. Notice that the names of the nodes are different on midway2 and midway3. There is a list showing the names and meanings of all partitions [here](https://rcc-uchicago.github.io/user-guide/midway23/midway_partitions/) under the subtitle "Shared Partitions".


## Submit

To submit the job, save the script above to a file like `example.sbatch` and then run the following command
```
sbatch example.sbatch
```

## Monitoring your jobs

You could use commands to check if your jobs are queueing or running and evaluate how long they will take.

To check the state, run
```
squeue | grep cnetID
```
Here is a script to automatically monitor your jobs and print the states on your screen in real-time.
```
# will put it here later, ask me directly if you want it
```


To know more, go to the [RCC website](https://rcc-uchicago.github.io/user-guide/)

{% include links.html %}
