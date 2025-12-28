# Family BASIC V2 disassembler/assembler/monitor typeins

These are Family BASIC V2 typein programs for a native disassembler, assembler, and monitor archived from ファミコン改造マニュアル (Famicom Hacking/Modding Manual) Vol. 3. 

This repository contains the typein sources as `.bas` files. Please refer to the `.md` file found in each directory for instructions on how to use each program. 

Example screenshots mimicking the original magazine screenshots are also included.

## Loading into emulators

Nintaco has many useful Family BASIC features but suffers from the following issues:
- Keyboard bindings were broken on the Linux device used during the process, thus only controller bindings and Type Paste could be used in Family BASIC.
- The save data and tape data exports use proprietary formats.
- Family BASIC save RAM mirroring is not emulated, which could impact program behaviour.

The following process was used to test/debug the transcribed programs instead:
1. Load Family BASIC V2 in Nintaco and reach GAME BASIC.
2. Load the program: "Machine -> Family BASIC -> Load Program" or "Machine -> Family BASIC -> Paste Program/Type Paste"
3. Enter `SYSTEM` then press 3 to exit. This sets up the save data for future startups.
4. Extract the save data. Saving a CPU memory dump using the Hex Editor, then extracting the 2048 bytes from 0x7000-0x77FF is probably the most consistent method.
5. Use the save data in other emulators running Family BASIC V2.
6. For repeat usage, `SAVE` the program to the tape data format used by the emulator to `LOAD` later.

This approach should also work for flashcarts running Family BASIC V2.

The typeins and tape data should work with [Disk BASIC](https://github.com/TakuikaNinja/FC-DiskBASIC), though they have not been thoroughly tested.

## Attributions

Family BASIC/NS-HUBASIC (C) 1984 Nintendo/Sharp/Hudson. 

ファミコン改造マニュアル Vol.3 Family BASIC disassembler/assembler/monitor
- Article Author: 牛島憲人 (Norihito Ushijima)
- Editor: 丹治佐一 (Saichi Tanji)
- Published: 1988-07
- Publisher: 三才ブックス (Sansai Books)

This project is purely for preservation, demonstration, and educational purposes.

## Acknowledgements

- Thanks to forple, who scanned the typein pages.
- Forum discussion: 
- [Nintaco](https://nintaco.com/) was used to load BASIC programs from source files.
- [Mesen2](https://www.mesen.ca/) was used for program testing/debugging.

