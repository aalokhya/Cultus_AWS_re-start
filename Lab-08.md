
# Working with Files in Linux

## Overview
This AWS lab helped me learn how to create a backup of an entire directory structure using the `tar` command, record backup details in a CSV file, and move the backup to another directory.

## Objectives
- Create a backup of an entire folder structure using `tar`.
- Log the backup date, time, and filename.
- Transfer the backup file to another folder.
- Verify the backup and its location.

## Steps Performed

### 1. Connect to the Amazon Linux EC2 Instance
- Started the AWS Vocareum lab.
- Opened the AWS Management Console.
- Downloaded the `labsuser.ppk` SSH key.
- Copied the Public IP address.
- Connected to the EC2 instance using PuTTY and SSH.

### 2. Check the Current Directory

```bash
pwd
```

Verified that the current directory was:

```text
/home/ec2-user
```

### 3. Verify the CompanyA Directory

```bash
ls -R CompanyA
```

Checked the existing folder structure and files inside `CompanyA`.

### 4. Create a Backup Using tar

```bash
tar -csvpzf backup.CompanyA.tar.gz CompanyA
```

Created a compressed backup of the entire `CompanyA` directory.

The backup file created was:

```text
backup.CompanyA.tar.gz
```

### 5. Verify the Backup File

```bash
ls
```

Verified that the backup archive was created successfully.

### 6. Navigate to the CompanyA Directory

```bash
cd /home/ec2-user/CompanyA
```

Checked the current location:

```bash
pwd
```

### 7. Create the Backup Log File

```bash
touch SharedFolders/backups.csv
```

Created an empty CSV file to store backup information.

### 8. Record Backup Details

```bash
echo "25 Aug 25 2021, 16:59, backup.CompanyA.tar.gz" | sudo tee SharedFolders/backups.csv
```

Recorded the backup date, time, and filename in `backups.csv`.

### 9. Verify the Backup Log

```bash
cat SharedFolders/backups.csv
```

Displayed the contents of the backup log file.

### 10. Move the Backup File to IA

```bash
mv ../backup.CompanyA.tar.gz IA/
```

Moved the backup archive from the parent directory into the `IA` folder.

### 11. Verify the Backup Location

```bash
ls . IA
```

Confirmed that `backup.CompanyA.tar.gz` was successfully moved into the `IA` directory.

## Screenshots

### 1. Creating and Verifying the Backup
![Creating and Verifying the Backup](screenshots/Screenshot%202026-11-12%20215606.png)

### 2. Logging and Moving the Backup File
![Logging and Moving the Backup File](screenshots/Screenshot%202026-11-12%20215614.png)

## Important Linux Commands

| Command | Purpose |
|---|---|
| `pwd` | Displays the current directory |
| `ls` | Lists files and directories |
| `ls -R` | Lists directory contents recursively |
| `cd` | Changes the current directory |
| `tar` | Creates an archive |
| `touch` | Creates an empty file |
| `echo` | Displays text |
| `sudo` | Executes a command with elevated privileges |
| `tee` | Writes output into a file |
| `cat` | Displays file contents |
| `mv` | Moves or renames files and directories |


## Conclusion
Successfully completed the Working with Files lab by creating a compressed backup of the `CompanyA` directory, recording backup details in a CSV file, and transferring the backup archive into the `IA` folder.
