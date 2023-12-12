## Goal 2 find the number of instructions:
## count instructions run by 
```
chmod +x get_instructions.sh
./get_instructions.sh
```
## output: 
check "Collected" number

## or mannually run in the terminal
```
gcc -g count_instructions_tool.c -o count_instructions_tool
valgrind --tool=callgrind ./count_instructions_tool
kcachegrind callgrind.out.<pid>
callgrind_annotate callgrind.out.<pid>
callgrind_annotate callgrind.out.<pid>.1 | grep -i "TOTALS" | awk '{print $1}'
```
