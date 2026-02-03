# Essential Linux and Java Commands for Codespace Users

## File System Navigation

| **Command**      | **Description**                                                                 | **Example**    |
| ---------------- | ------------------------------------------------------------------------------- | -------------- |
| `pwd`            | **Print Working Directory**: Shows the current directory you're in.             | `pwd`          |
| `ls`             | **List files**: Lists files and directories in the current location.            | `ls`           |
| `ls -l`          | **Detailed list**: Lists files with more info (permissions, owner, size, etc.). | `ls -l`        |
| `ls -a`          | **List all files**: Includes hidden files (those starting with `.`).            | `ls -a`        |
| `cd [directory]` | **Change Directory**: Moves to the specified directory.                         | `cd Documents` |
| `cd ..`          | **Move up**: Goes up one directory level (to the parent directory).             | `cd ..`        |
| `mkdir [folder]` | **Make Directory**: Creates a new folder in the current directory.              | `mkdir HW2`    |

---

## Navigating to Your Java File Folder
- Check your current directory:
  ```bash
  pwd
  ```
  output:
  ```
  /workspaces/Spring2026_ET581
  ```
  it means you are in folder(root of repo) Spring2026_ET581

- Navigate to folder HW1:
```bash
cd HW1
```
- List the files in the HW1 folder:
```bash
ls
```
output
```
Problem1.java Problem2.java Problem3.java
```
it means you have 3 java files in the folder
- Compile Problem1.java
```bash
javac Problem1.java
```
- Run Problem1.java
```bash
java Problem1
```
