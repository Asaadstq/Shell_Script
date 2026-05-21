# Syntax and Script Layout


```bash
#!/bin/bash
 
# -----------------------------------------------
# Script : greet.sh
# Purpose: Demonstrate basic script structure
# -----------------------------------------------
 
# Variables at the top
name="Alice"
 
# Logic in the middle
if [[ -n "${name}" ]]; then
    echo "Hello, ${name}!"
fi
```
 
## Formatting Rules
 
| Rule | Example |
|---|---|
| Comments start with `#` | `# This is a comment` |
| Use 4 spaces for indentation | Inside `if`, `for`, functions |
| Quote all variable expansions | `"${name}"` not `$name` |
| No spaces around `=` in assignments | `name="Alice"` not `name = "Alice"` |
 
---