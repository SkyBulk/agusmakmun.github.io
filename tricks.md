---
layout: page
title: Handy Commands for Vulnerability Research
permalink: /tricks/
---

## mona

### set mona working folder
`!mona config -set workingfolder c:\logs\%p`

### Generate unique pattern of 20000 where pc(pattern_create)
`!mona pc 20000`

### Finds the offset of unique or cyclic pattern in memory
`!mona findmsp`

### Finds the offset of 4bytes within the pattern where po(pattern_offset)
`!mona po <overwritten-bytes>`

### Find instructions with jump to esp like jmp esp, call esp etc.
`!mona jmp -r esp`

### Create bytearray from '00' to 'ff', used for bad character analysis
`!mona bytearray`

### Generate bytearray without bad bytes "\x00\x0a\x0d"
`!mona bytearray -b "\x00\x0a\x0d"`

### Generates rop gadgets from the selected Modules , ignore os modules , and those that includes nullbytes
`!mona rop -o -m "audconv.exe,audconv.dll" -cp nonull`

### Gives you pop pop ret to get to seh, and including bypassing safeseh modules
`!mona seh -all`

### Analyze bytes from 001254c1
`!mona compare -f C:\logs\something\bytearray.bin -a 001254c1`

### Converts given assembly instructions into opcode
```asm
nasm > jmp esp
00000000  FFE4  jmp esp
```

### Find ASCII string 'w00t' in memory
`!mona find -type asc -s "w00t"`

# windbg

### run 

`0:001> g`

### force to load modules

```0:001> !sym noisy
0:002> .reload -f
```

### find main windbg
```u $exentry
bp program!main
```

# IDA 
```
__p___argc
__p___argv
```

### list loaded modules from application 
`lm`

###  list a specific module with path location 
`lm m ntll`

### Search For -> All Sequences In All Modules
`s 0 L?0x7fffffff {ff e4} opcodes`

### memory map 
`!address` 

### view Stack Trace 
`knL`

### add breakpoint
`bp address`

### list breakpoint

` bl`

### remove breakpoint

` bc 0 `

### Windows internals
```
dt ntdll!_TEB or !teb # thread environment block
dt ntdll!_PEB !peb # process environment block
!exchain # view seh chain
d fs:[0] # view seh chain
```

### find a string in memory
`s -a 0x00000000 L?7fffffff "blackleitus"`

### Information about a register , and modules
`!address @eip`

### unassemble 
`0:005> u 715b9b02-7`

### memory display
`0:005> d ebx`

### Follow reference for the given pointer (handle) address
`0:005> d poi(ebx)`

### shows all heap usage for the process being debugged
`0:007> !heap -stat`

### view details on the heap 
`!heap -a 00140000`

### view the allocation statistics
`!heap -stat -h 00140000`

### View the memory size
`!heap -flt s 7ffe0`

### display a summary of all of the current heaps
`!heap -s`

###  display information on a particular heap allocation
`!heap -p -a`

### List heaps with index and range
`!heap -h 5a0000 `

### List heaps with index and HeapAddr
`!heap`


### Tracing API calls on Windows

- drstrace DynamoRIO
- Dependency Walker
