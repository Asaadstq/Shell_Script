# Error Handling
 
### Exit Codes
 
Every command returns an exit code when it finishes:
 
| Code | Meaning |
|---|---|
| `0` | Success |
| Non-zero | An error occurred |
 
Use `$?` to read the exit code of the last command:
 
```bash
#!/bin/bash
 
ls /tmp > /dev/null 2>&1
echo "ls /tmp exit code     : $?"   # 0
 
ls /fakepath > /dev/null 2>&1
echo "ls /fakepath exit code: $?"   # non-zero
```
 
---
 
### Exiting with a Code
 
Use `exit N` to stop the script and return a code.
 
```bash
#!/bin/bash
 
read -p "Enter a number greater than 0: " num
 
if [[ ${num} -le 0 ]]; then
    echo "ERROR: Number must be greater than 0."
    exit 1
fi
 
echo "You entered: ${num}"
exit 0
```
 
---
 
### `set -e` and `set -u`
 
```bash
#!/bin/bash
set -e   # stop the script if any command fails
set -u   # stop the script if an unset variable is used
 
echo "This runs."
cat /nonexistent_file   # script stops here
echo "This won't run."
```
 
---