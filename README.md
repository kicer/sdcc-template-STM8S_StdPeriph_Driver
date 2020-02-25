# sdcc-template-STM8S_StdPeriph_Driver
sdcc template which use STM8S_StdPeriph_Driver(v2.3.1) in macOSx.

Thanks for [STM8-SPL_SDCC_patch](https://github.com/gicking/STM8-SPL_SDCC_patch), [spl-splitter](https://github.com/tenbaht/spl-splitter).


## Install

1. path of compiler config in Makefile
```
CC = /Developer/sdcc/bin/sdcc
PROGRAMMER = stlinkv2
FLASHER = /Developer/sdcc/bin/stm8flash
FACTORYOPT = /Developer/sdcc/stm8s103_opt_factory_defaults.bin
```
2. install [sdcc](http://sdcc.sourceforge.net/)
3. install [stm8flash](https://github.com/vdudouyt/stm8flash)
4. touch `stm8s103f3_opt_factory_defaults.bin`
```
echo "00 00 ff 00 ff 00 ff 00 ff 00 ff" | xxd -r -p > /Developer/sdcc/stm8s103f3_opt_factory_defaults.bin
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
