# AWS Lab: Managing Users and Groups

## Overview
This lab demonstrates Linux user and group management on an Amazon Linux EC2 instance using SSH.

## Objectives
- Connect to an Amazon Linux EC2 instance using SSH (PuTTY).
- Create Linux users and set default passwords.
- Create groups and assign users to appropriate groups.
- Switch between users using `su`.
- Understand Linux file permissions and sudo privileges.
- View security logs in `/var/log/secure`.

## AWS Services and Tools
- Amazon EC2
- Amazon Linux
- PuTTY
- SSH
- Linux Command Line

## Task 1: Connect to EC2 Instance

1. Started the AWS Academy lab.
2. Opened the AWS Management Console.
3. Downloaded the `.ppk` SSH key.
4. Copied the EC2 Public IP address.
5. Connected to the EC2 instance using PuTTY.
6. Logged in as `ec2-user`.

Verified the current directory:

```bash
pwd
```

Output:
```text
/home/ec2-user
```

## Task 2: Create Linux Users

Created the following users using `useradd`:

| User ID | Name | Job Role |
|---|---|---|
| arosalez | Alejandro Rosalez | Sales Manager |
| eowusu | Efua Owusu | Shipping |
| jdoe | Jane Doe | Shipping |
| ljuan | Li Juan | HR Manager |
| mmajor | Mary Major | Finance Manager |
| mjackson | Mateo Jackson | CEO |
| nwolf | Nikki Wolf | Sales Representative |
| psantos | Paulo Santos | Shipping |
| smartinez | Sofia Martinez | HR Specialist |
| ssarkar | Saanvi Sarkar | Finance Specialist |

Created users using:

```bash
sudo useradd <username>
```

Set passwords using:

```bash
sudo passwd <username>
```

Used the default lab password for all users.

Verified user creation:

```bash
sudo cat /etc/passwd | cut -d: -f1
```

## Task 3: Create Linux Groups

Created the following groups:

```bash
sudo groupadd Sales
sudo groupadd HR
sudo groupadd Finance
sudo groupadd Personnel
sudo groupadd Shipping
sudo groupadd Managers
sudo groupadd CEO
```

### Assign Users to Groups

Added users to their respective groups using `usermod`.

**Sales**
```bash
sudo usermod -a -G Sales arosalez
sudo usermod -a -G Sales nwolf
```

**HR**
```bash
sudo usermod -a -G HR ljuan
sudo usermod -a -G HR smartinez
```

**Finance**
```bash
sudo usermod -a -G Finance mmajor
sudo usermod -a -G Finance ssarkar
```

**Shipping**
```bash
sudo usermod -a -G Shipping eowusu
sudo usermod -a -G Shipping jdoe
sudo usermod -a -G Shipping psantos
```

**Managers**
```bash
sudo usermod -a -G Managers arosalez
sudo usermod -a -G Managers ljuan
sudo usermod -a -G Managers mmajor
```

**CEO**
```bash
sudo usermod -a -G CEO mjackson
```

Added `ec2-user` to all groups:

```bash
sudo usermod -a -G Sales,HR,Finance,Shipping,Managers,CEO,Personnel ec2-user
```

Verified group membership:

```bash
sudo cat /etc/group
```

## Task 4: Login Using Different Users

Switched to the Sales Manager account:

```bash
su arosalez
```

Checked the current directory:

```bash
pwd
```

Tried creating a file:

```bash
touch myFile.txt
```

Received a permission denied error because `arosalez` did not have permission to write in `/home/ec2-user`.

Tried executing the command with sudo:

```bash
sudo touch myFile.txt
```

Received the following error:

```text
arosalez is not in the sudoers file.
```

This demonstrated that regular users do not automatically have administrator privileges.

Returned to the original user:

```bash
exit
```

## Task 5: Verify Security Logs

Viewed the security log:

```bash
sudo cat /var/log/secure
```

Observed the failed sudo attempt:

```text
user NOT in sudoers
```

The security log records sudo-related activities, including unauthorized attempts to execute privileged commands.

## Important Linux Commands Learned

| Command | Purpose |
|---|---|
| `useradd` | Create a new user |
| `passwd` | Set or change a user's password |
| `userdel` | Delete a user |
| `groupadd` | Create a group |
| `usermod` | Modify user account settings |
| `id` | Display user and group information |
| `su` | Switch to another user |
| `sudo` | Execute commands with elevated privileges |
| `pwd` | Display current directory |
| `touch` | Create an empty file |
| `cat` | Display file contents |
| `exit` | Exit the current user session |



Practised Linux user and group administration on an Amazon Linux EC2 instance.
