# Arithmetic Operations
 
Use `$(( ))` for integer math.
 
```bash
#!/bin/bash
 
a=10
b=3
 
echo "Addition       : $(( a + b ))"
echo "Subtraction    : $(( a - b ))"
echo "Multiplication : $(( a * b ))"
echo "Division       : $(( a / b ))"
echo "Modulo         : $(( a % b ))"
echo "Exponentiation : $(( a ** 2 ))"
```
 
**Output:**
```
Addition       : 13
Subtraction    : 7
Multiplication : 30
Division       : 3
Modulo         : 1
Exponentiation : 100
```
 
> Division truncates decimals. For floating-point results, use `bc`:
> ```bash
> result=$(echo "scale=2; 10 / 3" | bc)
> echo ${result}   # 3.33
> ```
 
---