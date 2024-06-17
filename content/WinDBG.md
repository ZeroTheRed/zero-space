A debugger for Microsoft Windows. [WinDbg](https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/) can be used to locate and resolve errors caused in a system 

Use WinDBG and obtain mini-dumps to find out what's wrong with the system that's causing BSoDs 

You can find the mini-dumps at `C:\WINDOWS\Minidump` (Run WinDBG as admin or configure the minidumps to be saved elsewhere outside of the WINDOWS folder)

Open the minidump and run the `analyze` command on it. An example of a possible error that can be analysed using WinDBG is the `nvlddmkm.sys` problem

### Sources 
1. https://www.nvidia.com/en-us/geforce/forums/game-ready-drivers/13/54045/the-nvlddmkm-error-what-is-it-an-fyi-for-those-s/