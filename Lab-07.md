# Working with the File System in Linux

## Overview
This lab helped me understand Linux file system operations, including creating directories, creating files, copying, moving, and deleting files and directories.

## Objectives
- Navigate through Linux directories.
- Create directories and files.
- Copy files and directories.
- Move files and directories.
- Delete files and directories.
- View directory structures.

## Steps Performed

### 1. Check the Current Directory

```bash
pwd
```

Navigated to the home directory if required:

```bash
cd /home/ec2-user
```

### 2. Create Directories

Created the main directory:

```bash
mkdir CompanyA
cd CompanyA
```

Created three subdirectories:

```bash
mkdir Finance HR Management
```

### 3. Create Files in HR

```bash
cd HR
touch Assessments.csv TrialPeriod.csv
```

### 4. Create Files in Finance

```bash
cd ../Finance
touch Salary.csv ProfitAndLossStatements.csv
```

### 5. Create Files in Management

```bash
cd ..
touch Management/Managers.csv Management/Schedule.csv
```

### 6. View the Directory Structure

```bash
ls -laR
```

### 7. Copy a Directory

Copied the Finance directory into HR:

```bash
cp -r Finance HR
```

Verified the copied files:

```bash
ls HR/Finance
```

### 8. Delete Original Finance Files

```bash
rm Finance/ProfitAndLossStatements.csv Finance/Salary.csv
```

Checked the directory:

```bash
ls Finance
```

Removed the empty Finance directory:

```bash
rmdir Finance
```

### 9. Move the Management Directory

Moved Management into HR:

```bash
mv Management HR
```

Verified the directory structure:

```bash
ls . HR/Management
```

### 10. Move HR Files into Employees

Navigated into HR:

```bash
cd HR
```

Created Employees directory:

```bash
mkdir Employees
```

Moved the files:

```bash
mv Assessments.csv TrialPeriod.csv Employees
```

Verified the files:

```bash
ls . Employees
```

## Final Directory Structure

```text
CompanyA/
└── HR/
    ├── Employees/
    │   ├── Assessments.csv
    │   └── TrialPeriod.csv
    ├── Finance/
    │   ├── ProfitAndLossStatements.csv
    │   └── Salary.csv
    └── Management/
        ├── Managers.csv
        └── Schedule.csv
```

## Important Linux Commands

| Command | Purpose |
|---|---|
| `pwd` | Display current directory |
| `ls` | List files and directories |
| `ls -laR` | Display detailed directory structure |
| `cd` | Change directory |
| `cd ..` | Move to parent directory |
| `mkdir` | Create a directory |
| `touch` | Create an empty file |
| `cp -r` | Copy a directory recursively |
| `mv` | Move or rename files/directories |
| `rm` | Delete files |
| `rmdir` | Remove an empty directory |

## Screenshots

### 1. Creating Directories and Files
![Creating Directories and Files](../screenshots/Screenshot%202026-11-12%20202513.png)

### 2. Copying, Moving, and Managing Files
![Copying, Moving, and Managing Files](../screenshots/Screenshot%202026-11-12%20202521.png)

## Conclusion
Successfully practiced Linux file system operations and learned how to organize, copy, move, and delete files and directories using command-line instructions.
