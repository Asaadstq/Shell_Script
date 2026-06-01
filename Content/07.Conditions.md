# Conditions
 
### `if` / `elif` / `else`
 
```bash
#!/bin/bash
 
read -p "Enter a number: " num
 
if [[ ${num} -gt 0 ]]; then
    echo "Positive"
elif [[ ${num} -lt 0 ]]; then
    echo "Negative"
else
    echo "Zero"
fi
```
 
---
 
### Comparison Operators
 
**Integer comparisons:**
 
| Operator | Meaning |
|---|---|
| `-eq` | Equal |
| `-ne` | Not equal |
| `-gt` | Greater than |
| `-lt` | Less than |
| `-ge` | Greater than or equal |
| `-le` | Less than or equal |
 
**String comparisons:**
 
| Operator | Meaning |
|---|---|
| `==` | Equal |
| `!=` | Not equal |
| `-z` | Empty string |
| `-n` | Non-empty string |
 
```bash
#!/bin/bash
 
read -p "Enter your name: " name
 
if [[ -z "${name}" ]]; then
    echo "You didn't enter a name."
elif [[ "${name}" == "Admin" ]]; then
    echo "Welcome, administrator."
else
    echo "Hello, ${name}."
fi
```
 
---
 
### `case` Statement
 
A cleaner alternative to multiple `if-elif` checks when matching a single variable against fixed values.
 
```bash
#!/bin/bash
 
read -p "Choose a day (mon/tue/wed): " day
 
case "${day}" in
    mon)
        echo "Monday — Start of the week"
        ;;
    tue)
        echo "Tuesday"
        ;;
    wed)
        echo "Wednesday — Midweek"
        ;;
    *)
        echo "Unknown day: ${day}"
        ;;
esac
```
 
---