# DLLHiding
Hiding x32/x64 Modules using PEB

##Summary
A simple command-line application to Hide DLLs in any Windows Process. Works on both x32 and x64 Processes.

It should work on all platforms from Windows XP to Windows 8. Currently only tested on Windows 7.

Every Process maintains internal set of loaded Modules/DLLs in the form of three linked lists within the PE Block.
- Load Order List
- Memory Order List
- Initialization Order List
 
##Limitations
Should effectively hide modules from all user mode applications. Application with Kernel mode access can enumerate the hidden modules such applications include Process Explorer. Additionally user mode applications can enumerate the memory of an application and based on some size analyzation determine that there maybe a hidden module. 

##Motivation
I could not find any source code or support for x64 processes to test some internal software solutions so I developed this application. 
