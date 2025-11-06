# 🧠 Assembly Language Learning Notes (EMU8086)

Welcome to my **Assembly Language Learning Notes** repository!  
This project contains all my personal notes, codes, and experiments while learning **x86 Assembly Language** using the **EMU8086** simulator.  

---

## ⚙️ About This Repository

This repository is designed to document my step-by-step learning journey of **Assembly Language Programming** — from beginner to advanced topics.  
All examples are written for **Intel 8086 architecture**, and can be run using **EMU8086** software.

---

## 🧩 Topics Covered

| No. | Topic | Description |
|:---:|:------|:-------------|
| 1 | Introduction to Assembly Language | Overview of low-level programming and CPU instructions |
| 2 | EMU8086 Setup | Installing and running EMU8086 IDE |
| 3 | Registers and Memory | AX, BX, CX, DX, Flags, and addressing modes |
| 4 | Data Movement Instructions | `MOV`, `XCHG`, `LEA`, etc. |
| 5 | Arithmetic Instructions | `ADD`, `SUB`, `INC`, `DEC`, `MUL`, `DIV` |
| 6 | Logical & Bitwise Operations | `AND`, `OR`, `XOR`, `NOT`, `SHL`, `SHR` |
| 7 | Control Flow | `JMP`, `JE`, `JNE`, `JG`, `JL`, `LOOP` |
| 8 | Procedures & Macros | Writing reusable code blocks |
| 9 | String Instructions | `MOVS`, `CMPS`, `SCAS`, `LODS`, `STOS` |
| 10 | Interrupts & System Calls | Using DOS and BIOS interrupts (`INT 21h`, etc.) |
| 11 | Input/Output Operations | Keyboard and screen handling |
| 12 | Stack & Memory Management | `PUSH`, `POP`, and stack segment operations |
| 13 | Simple Projects | Basic calculator, string reverse, factorial, etc. |

---

## 💻 Tools and Environment

- **Assembler:** [EMU8086](https://emu8086-microprocessor-emulator.en.softonic.com/)
- **License:** user: `ISHAAN,glaitm` and Key: `27R3VDEFYFX4N0VC3FRTQZX`
- **Architecture:** Intel 8086 (16-bit)
- **Language:** Assembly Language (MASM-style syntax)
- **OS Compatibility:** Windows (Recommended)

---

## 🧪 Example Code

### Hello World in Assembly (EMU8086)
```asm
.model small
.stack 100h
.data
    msg db 'Hello, World!$'
.code
main proc
    mov ax, @data
    mov ds, ax

    mov ah, 09h
    lea dx, msg
    int 21h

    mov ah, 4Ch
    int 21h
main endp
end main
