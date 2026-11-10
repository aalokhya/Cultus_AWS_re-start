## 1. Lab name

Linux Command Line – Basic Linux Commands and Bash History

## Overview

This lab focuses on understanding basic Linux command-line operations and improving workflow by using Bash command history and search features.

The lab was performed using an Amazon Linux EC2 instance accessed through SSH.

## Tasks Performed

### Task 1: Connect to EC2 using SSH

- Started the AWS lab environment.
- Downloaded the SSH private key.
- Connected to the Amazon Linux EC2 instance using SSH.
- Logged in as `ec2-user`.

### Task 2: Execute Basic Linux Commands

| Command                       | Purpose                                         |
| ----------------------------- | ----------------------------------------------- |
| `whoami`                      | Displays the current username.                  |
| `hostname -s`                 | Displays the short hostname.                    |
| `uptime -p`                   | Displays system uptime in a readable format.    |
| `who -H -a`                   | Displays logged-in user information.            |
| `TZ=America/New_York date`    | Displays New York date and time.                |
| `TZ=America/Los_Angeles date` | Displays Los Angeles date and time.             |
| `cal -j`                      | Displays the calendar using Julian day numbers. |
| `cal -s`                      | Displays the calendar starting on Sunday.       |
| `cal -m`                      | Displays the calendar starting on Monday.       |
| `id ec2-user`                 | Displays user ID and group information.         |

### Task 3: Bash History and Command Search

| Command / Shortcut | Purpose                                |
| ------------------ | -------------------------------------- |
| `history`          | Displays previously executed commands. |
| `Ctrl + R`         | Searches command history in reverse.   |
| `!!`               | Executes the previous command again.   |
| `Tab`              | Provides command auto-completion.      |


## Screenshots

Screenshots captured during the lab execution are available in the `screenshots/` folder.





Once uploaded, your GitHub repository will demonstrate practical Linux command-line experience alongside your EC2 lab.

We can use the same README + screenshots format for every upcoming AWS lab.
