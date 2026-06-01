# Presenting Data
 
## `echo` — Simple Output
 
```bash
#!/bin/bash
 
name="Ahmad"
score=95
 
echo "Name  : ${name}"
echo "Score : ${score}"
```
 
---
 
## `printf` — Formatted Output
 
`printf` gives you control over column width and alignment, making tabular output clean and readable.
 
| Specifier | Meaning |
|---|---|
| `%s` | String |
| `%d` | Integer |
| `%-Ns` | Left-aligned string in N-wide column |
| `\n` | New line |
 
```bash
#!/bin/bash
 
printf "%-15s %-10s %-6s\n" "NAME" "GRADE" "SCORE"
printf "%-15s %-10s %-6s\n" "---------------" "----------" "------"
printf "%-15s %-10s %-6d\n" "Ahmad"   "A" 95
printf "%-15s %-10s %-6d\n" "Fahad"     "B" 82
printf "%-15s %-10s %-6d\n" "Saad" "C" 74
```
 
**Output:**
```
NAME            GRADE      SCORE
--------------- ---------- ------
Ahmad           A          95
Fahad           B          82
Saad            C          74
```
 
---
 
