# sdcc-template-STM8S_StdPeriph_Driver
sdcc template which use STM8S_StdPeriph_Driver(v2.3.1) in macOSx.

Thanks for [STM8-SPL_SDCC_patch](https://github.com/gicking/STM8-SPL_SDCC_patch), [spl-splitter](https://github.com/tenbaht/spl-splitter).


## Install

1. install [sdcc](http://sdcc.sourceforge.net/)
2. install [stm8flash](https://github.com/vdudouyt/stm8flash)
3. path of compiler config in Makefile
```
CC = /Developer/sdcc/bin/sdcc
FLASHER = /Developer/sdcc/bin/stm8flash
PROGRAMMER = stlinkv2
```


## Usage
1. Set DEVICE in Makefile
```
DEVICE=stm8s103f3
CPU=STM8S103
```
2. Build ihex: `make`
3. Program: `make flash`
4. Clean: `make clean`
5. Factory of Option-Bytes: `make factory`
5. Unlock Device: `make unlock`
