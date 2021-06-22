## How to extract file name from file path

1. Use the `Basename` command

To extract the file name from the file path, we can use the basename command.
The basename command works by looking for slashes and printing the thing that comes after the last slash.

```bash
basename PATH [suffix]
```

Example usage:

```bash
basename /home/usr/documents/filename.txt
filename.txt #output
```

To remove the file extension from the output, pass the extension value as the suffix.

```bash
basename /home/usr/documents/filename.txt .txt
filename #output
```
