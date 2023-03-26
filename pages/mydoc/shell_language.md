---
title: Basic shell commands
keywords: midway2
last_updated: March 22, 2023
tags: [midway]
summary: "This is an introduction to the HPC at UChicago, midway2."
sidebar: sidebar_1
permalink: shell_language.html
folder: mydoc
---

## Why you need this
Unlike windows system, unix/linux system is widely used in scientific computation research. The midway2/3 at UChicago is based on linux system so if you want to navigate our data stored on midway2/3 and run your analysis by using the terminal, then you need to know the basic shell "commands" to navigate the linux system computer. 

## The first task: Open a terminal
If you are a macOS user, congratulations, you could directly open a terminal as macOS is based on unix. See [here](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac) for the instructions.

If you are a windows user, I would recommend you to install a **GitBash** so that you could use the terminal. (Sorry I don't have a windows device but if anyone knows the correct way to install it please edit here, but anyway, Google it and there will be some solutions.)

## Basic commands
### Go to a place
Know where you are
```
pwd
```
It will show you your current path.

Go to a directory
```
cd /the/path/you/are/going/to
```
Go to the last layer
```
cd ..
```
### Check what's in a folder
List all the directories and files in current path
```
ls
ls -a  # include hidden files
ls -l  # show the access permissions, file sizes, edit dates
ls /specific/path  # list the directories and file within the given path
```
### Create new folders and files, rename
To create a new folder in current path
```
mkdir /folder/name
```
To create a text file (including .txt, .sh, .sbatch, .csv, .tsv, .yml, .json and any text format files), there are multiple ways. I recommend to use this one
```
vim file_name.txt
```
Then you will open an empty file and you could insert content to it. To insert text, press `i`. To exit from it, press `esc`. to save and exit the file, type
```
:wq
```
If you want to rename a folder or file
```
mv /old/name /new/name
```

### Copy and paste, cut and paste








{% include links.html %}