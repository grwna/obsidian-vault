
# ToC
- [Debugger](#debugger)
- [PWNTools](#pwntools)
# Debugger
## PWNDBG

# PWNTools
## Disabling ASLR
`pwn.process("./program", aslr=False)`

## Finding Offsets
In order to make it work, you need to make sure that the program **actually crashes**, and on top of that, the core-dump files is created inside the current working directory. 

## ELF Syntax
`exe = './{binary_path}'`
`elf = context.binary = ELF(exe, checksec=False)`

- `elf.symbols['{symbol_name}']` - used to find address of symbol
