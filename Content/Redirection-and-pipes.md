# Redirection and Pipes
 
## Standard Streams
 
| Stream | Meaning | File Descriptor |
|---|---|---|
| `stdin` | Input | `0` |
| `stdout` | Normal output | `1` |
| `stderr` | Error output | `2` |
 
---
 
## Output Redirection
 
```bash
#!/bin/bash
 
# Write to a file (overwrite)
echo "Hello" > output.txt
 
# Append to a file
echo "World" >> output.txt
 
# Redirect errors to a file
ls /fakepath 2> errors.txt
 
# Redirect both output and errors to the same file
ls /tmp /fakepath > all.txt 2>&1
```
 
---
 
## Input Redirection
 
```bash
#!/bin/bash
 
# Use a file as input instead of the keyboard
sort < names.txt
```
 
---
 
## Pipes (`|`)
 
A pipe sends the output of one command as the input to the next.
 
```bash
#!/bin/bash
 
# Count the number of files in /etc
ls /etc | wc -l
 
# Show only lines containing "bash" from /etc/passwd
cat /etc/passwd | grep "bash"
 
# Show the 3 largest files in the current directory
ls -lS | head -4
```
 
---
 