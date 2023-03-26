---
title: Midway2 usage
keywords: documentation theme, jekyll, technical writers, help authoring tools, hat replacements
last_updated: March 8, 2023
tags: [midway]
summary: "This is an introduction to the HPC at UChicago, midway2."
sidebar: sidebar_1
permalink: midway2_overview.html
folder: mydoc
---

## Why you need this
You don't want to explode your laptop, which has 8G RAM and 500G storage, while you find that your sequencing data is 700G. That's why you need the High Performance Computing (HPC). UChicago has its own server, which is called **Midway**. Of course, we have the second generation **midway2** and the newest one **midway3**. We store our raw data and some processed data on it, fetch the data and run computation intensive jobs on the computation nodes.

## Log in and log out
In order to log into midway2, open a terminal on your macbook and type
```
ssh your_cnet_ID@midway2.rcc.uchicago.edu
```
For midway3, it's similar
```
ssh your_cnet_ID@midway3.rcc.uchicago.edu
```
To log out, just type
```
exit
```
After you log in, you are on the login node. There are two types of nodes: **login node** and **computation node**.
{% include warning.html content="Never run computation intensive jobs on login nodes. Otherwise the job may be killed by the administrator halfway. The correct way is to submit it submit it to the computation node. Check [this page](midway2_submit.html) for how to do it." %}

## check account state
### midway2
Check which group belongs to
```
group
```
To check storage
```
quota
```
Check the remaining SU
```
rcchelp balance
rcchelp balance -user cnetID
```
Check SU usage
```
rcchelp usage -account pi-taopan
rcchelp usage
rcchelp usage -user cnetID
rcchelp usage -byuser
rcchelp usage -all
rcchelp usage -byjob

rcchelp allocations 
rcchelp group-members pi-taopan
```

### midway3
```
rcchelp allocations
rcchelp balance -a pi-taopan
rcchelp usage -a pi-taopan
quota
```





To know more, feel free to go to the [RCC website](https://rcc-uchicago.github.io/user-guide/)

{% include links.html %}
