# Arrays
 
## Creating and Accessing
 
```bash
#!/bin/bash
 
colors=("red" "green" "blue")
 
echo "First  : ${colors[0]}"
echo "Second : ${colors[1]}"
echo "All    : ${colors[@]}"
echo "Count  : ${#colors[@]}"
```
 
**Output:**
```
First  : red
Second : green
All    : red green blue
Count  : 3
```
 
---
 
## Looping Through an Array
 
```bash
#!/bin/bash
 
languages=("Bash" "Python" "JavaScript" "Go")
 
for lang in "${languages[@]}"; do
    echo "- ${lang}"
done
```
 
**Output:**
```
- Bash
- Python
- JavaScript
- Go
```
 
---
 
## Adding and Removing Elements
 
```bash
#!/bin/bash
 
items=("a" "b" "c")
 
# Add an element
items+=("d")
echo "After add    : ${items[@]}"
 
# Remove element at index 1
unset 'items[1]'
items=("${items[@]}")   # re-index
echo "After remove : ${items[@]}"
```
 
**Output:**
```
After add    : a b c d
After remove : a c d
```
 
---