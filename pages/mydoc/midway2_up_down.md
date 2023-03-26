---
title: Upload and download data
keywords: midway2
last_updated: March 22, 2023
tags: [midway]
summary: "This is an introduction to the HPC at UChicago, midway2."
sidebar: sidebar_1
permalink: midway2_up_down.html
folder: mydoc
---

## Why you need this
You may want to upload data from your local device to the cluster. You may want to download the processed data from the cluster to your own device for further analysis. You may want to download huge amount of data from public database to midway2 directly, without booming your local storage.

## Between your device and midway2
**Run the commands on a local terminal. Do NOT log into midway2/3 to run this.**

To download data from midway2 to your device
```
rsync -azP cnetID@midway2.rcc.uchicago.edu:/path/to/your/file /path/you/want/to/download/to/
```
To upload data from your device to midway2
```
rsync -azP /path/you/want/to/download/to/ cnetID@midway2.rcc.uchicago.edu:/path/to/your/file
```

The logo
{% include image.html file="company_logo.png" url="http://www.google.com" alt="Jekyll" caption="This is a sample caption" %}

{% include links.html %}