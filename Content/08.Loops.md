# Loops
 
### `for` Loop
 
**Iterating over a list:**
 
```bash
#!/bin/bash
 
fruits=("apple" "banana" "cherry")
 
for fruit in "${fruits[@]}"; do
    echo "Fruit: ${fruit}"
done
```
 
**Iterating over a range:**
 
```bash
#!/bin/bash
 
for i in {1..5}; do
    echo "Number: ${i}"
done
```
 
---
 
### `while` Loop
 
Runs as long as the condition is true.
 
```bash
#!/bin/bash
 
count=1
 
while [[ ${count} -le 5 ]]; do
    echo "Count: ${count}"
    (( count++ ))
done
```
 
**Output:**
```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```
 
---