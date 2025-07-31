# PAI-LAB-ASSIGNMENT
# 🛠️ First Lab Assignment - Assembly Language

Welcome to my repository for the **1st Lab Assignment** of our Assembly Language course. This repository contains basic assembly programs along with GDB usage for debugging.

---

## Contents

1. **hello_world.asm**  
   → A simple program to print `Hello, World!` on the console using Assembly.

2. **gdb_demo.asm**  
   → Demonstrates the use of **GDB (GNU Debugger)** to debug Assembly code step-by-step.

3. **name_surname.asm**  
   → Prints your **first name** on the first line and your **surname** on the second line using Assembly instructions.

---

##  Tools Used

- **NASM (Netwide Assembler)**  
- **GDB (GNU Debugger)**  
- **Linux Terminal** for compiling and running assembly files

---

##  How to Run Hello world

### Step 1: Assemble the `.asm` file using NASM
```bash
nasm -f elf32 hello.asm
```
### Step 2: Link the object file
```bash
ld -m elf_i386 -s -o hello hello.o
```
### Step 3: Run the program
```bash
./hello
```

### Debugging part 

## How to Compile
```bash
nasm -f elf32 hello.asm          # Assemble
ld -m elf_i386 -o hello hello.o  # Link
```
## How to Debug with GDB
```bash
gdb ./hello
```
### GDB Command Flow
```bash
(gdb) break _start                  # Set breakpoint at program start
(gdb) run                           # Run the program
(gdb) set disassembly-flavor intel # Use Intel syntax for better clarity
(gdb) disassemble _start           # View disassembled instructions
(gdb) layout asm                   # Open assembly layout view
(gdb) layout regs                  # Show register view
(gdb) nexti                        # Execute next instruction
(gdb) quit                         # Exit GDB
```

## Print Name and Surname in Assembly

This Assembly program (`myname.asm`) prints your **first name** on the first line and your **surname** on the second line

### How to Compile & Run
```bash
nasm -f elf32 myname.asm         # Assemble the code
ld -m elf_i386 -o myname myname.o   # Link the object file
./myname                         # Run the program
```

