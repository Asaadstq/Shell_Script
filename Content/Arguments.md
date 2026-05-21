# Arguments
 
Arguments are values passed to the script when running it from the terminal.
 
| Parameter | Value |
|---|---|
| `$0` | Script name |
| `$1`, `$2` | First and second arguments |
| `$#` | Total number of arguments |
| `$@` | All arguments |
 
```bash
#!/bin/bash
# Usage: ./greet.sh <name> <age>
 
echo "Script name : $0"
echo "Name        : $1"
echo "Age         : $2"
echo "Total args  : $#"
echo "All args    : $@"
```
 
**Running:**
```bash
./greet.sh Alice 25
```
 
**Output:**
```
Script name : ./greet.sh
Name        : Alice
Age         : 25
Total args  : 2
All args    : Alice 25
```
 
---