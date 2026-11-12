# Editing Files in Linux

## Overview
This lab helped me learn how to create, edit, save, and manage files using Linux text editors such as Vim and Nano.

## Objectives
- Understand basic Vim commands.
- Create and edit files using Vim.
- Save and exit files.
- Create and edit files using Nano.

## Steps Performed

### 1. Connect to the EC2 Instance
- Opened the AWS Management Console through Vocareum.
- Accessed the EC2 Command Host instance.
- Connected to the instance using PuTTY and the provided PPK key.

### 2. Practice Vim
Started the Vim tutorial:

```bash
vimtutor
```

Completed lessons 1–3 and exited using:

```vim
:q!
```

### 3. Create and Edit a File Using Vim

Created a file:

```bash
vim helloworld
```

Pressed `i` to enter insert mode and added:

```text
Hello World!
This is my first file in Linux and I am editing it in Vim!
```

Pressed `Esc` and saved the file using:

```vim
:wq
```

### 4. Practice Saving and Exiting
Reopened the file:

```bash
vim helloworld
```

Added another line:

```text
I learned how to create a file, edit and save them too!
```

Exited without saving using:

```vim
:q!
```

Reopened the file to verify that the unsaved changes were not retained.

### 5. Practice Basic Vim Commands

| Command | Purpose |
|---|---|
| `i` | Enter insert mode |
| `Esc` | Exit insert mode |
| `dd` | Delete a line |
| `u` | Undo changes |
| `:w` | Save the file |
| `:wq` | Save and quit |
| `:q!` | Quit without saving |

### 6. Create and Edit a File Using Nano

Created a file:

```bash
nano cloudworld
```

Entered the following text:

```text
We are using nano this time! We can simply start typing! No insert mode needed.
```

Saved the file using `Ctrl + O`, pressed `Enter`, and exited using `Ctrl + X`.

Reopened the file to verify the saved content.

## Key Learnings
- Practiced the Vim text editor.
- Learned how to create and edit files in Linux.
- Understood the difference between saving and exiting without saving.
- Practiced basic Nano editor commands.

## Conclusion
Successfully learned how to create, edit, save, and manage text files using Vim and Nano in a Linux environment.
