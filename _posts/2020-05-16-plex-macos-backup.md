---
layout: post
title:  "Back up your Plex Media Server on Mac OS"
date:   2020-05-16 12:00:00 +0900
author: Adam Spann
categories: [Coding, Bash]
tags: [Plex, Bash, Mac OS, Backup, Automation]
---

## The Challenge:
How to automate the backing up of my [Plex Media Server](https://www.plex.tv)
## Solution:
A Bash Script

I wanted to automate this process. If I didn't, it probably wouldn't get done.

This script was adapted from another GitHub Gist that I found [here](https://gist.github.com/shnhrrsn/7f22abe085a07e250c851d53db55bae2).

{% gist 1e86a002ef5c09644567f496553737e9 %}

You will probably need to modify the following variables.
  - plexDatabase
  - plexPlistFile
  - backupDirectory
  - plexBackupDirectory

Pay attention to lines 17 ~ 21. These refer to the possibility that your script may not
complete if your machine can go to sleep. As it suggests use the 'caffinate' command to prevent
your machine from sleeping during backup. It will be able to sleep after the script completes.

Don't forget to give the script execution permission using 'chmod +x scriptname'

Install a cronjob under your user account using:
```sh
  crontab -e
```

The contents of my cronjob

```sh
SHELL=/bin/bash
06 02 * * Sun /usr/bin/caffeinate $HOME/bin/plexbackup.sh
```
Notes:
  - You need a SHELL set for the cronjob to run the command.
  - The script runs weekly on Sunday from 6:02am
  - It uses caffeinate so that the machine does not sleep during backup. I do not have my sleep value set to 0 on this machine.
  - My backup script is located in my home directory under the folder ***bin***
