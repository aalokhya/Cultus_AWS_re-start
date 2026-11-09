# Introduction to Amazon Linux AMI – SSH Access and Linux Man Pages

## Objective
- Understand Amazon Machine Images (AMI).
- Connect to an Amazon Linux EC2 instance using SSH.
- Configure PuTTY for remote Linux access.
- Explore Linux manual pages using the `man` command.
- Practice basic Linux commands.

## AWS Services and Tools Used
- Amazon EC2
- Amazon Linux AMI
- Amazon VPC
- Vocareum AWS Lab Environment
- PuTTY
- SSH (Secure Shell)

## Steps Performed

### Step 1: Start the AWS Lab
- Started the lab in Vocareum.
- Waited until the lab status changed to Ready.
- Opened the AWS Management Console.

### Step 2: Download SSH Credentials
- Opened Details → Show in Vocareum.
- Downloaded the `labsuser.ppk` private key.
- Copied the EC2 instance's Public IP address.

### Step 3: Configure PuTTY
- Opened PuTTY on Windows.
- Entered the EC2 Public IP address.
- Selected SSH as the connection type.
- Configured port 22.
- Navigated to Connection → SSH → Auth → Credentials.
- Selected the downloaded `labsuser.ppk` file.

### Step 4: Connect to Amazon Linux Using SSH
- Opened the PuTTY session.
- Accepted the host key confirmation.
- Connected to the Amazon Linux EC2 instance using the `ec2-user` account.

### Step 5: Explore Linux Manual Pages
Executed the following command:

```bash
man man
```

Explored the important sections of Linux manual pages:

- NAME
- SYNOPSIS
- DESCRIPTION
- OVERVIEW
- EXAMPLES
- FILES
- OPTIONS
- SEE ALSO

Pressed `q` to exit the manual page.

### Step 6: Practice Basic Linux Commands

| Command | Description |
|---|---|
| `pwd` | Display current working directory |
| `ls` | List files and directories |
| `whoami` | Display current username |
| `date` | Display system date and time |
| `hostname` | Display system hostname |
| `uname -a` | Display system information |
| `clear` | Clear terminal screen |
| `man ls` | View the manual page for ls |

## Key Learnings
- Understood Amazon Machine Images (AMI).
- Learned how to connect to a Linux EC2 instance remotely using SSH.
- Understood SSH authentication using private keys.
- Learned PuTTY configuration on Windows.
- Explored Linux manual pages.
- Practiced basic Linux commands.

## Outcome
Learned to access an Amazon Linux EC2 instance using SSH through PuTTY and explore Linux command documentation using the `man` command.

## Screenshots
![Linux man command](screenshots/Screenshot%202026-11-09%20203157.png)


