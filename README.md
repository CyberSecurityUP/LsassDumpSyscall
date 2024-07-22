# LsassDumpSyscall

## Overview
LsassDumpSyscall is a specialized utility designed to securely dump the memory contents of the `lsass.exe` process, which is crucial for managing security policies and storing security information on Windows operating systems. The primary objective of this tool is to facilitate security research and testing by enabling the analysis of `lsass.exe` without leveraging high-profile tools like Mimikatz that are commonly detected by antivirus software.

## Features
- **Direct System Calls**: The tool bypasses the Windows API layer by utilizing direct system calls to interact with the operating system. This method minimizes the tool's footprint and avoids common API hooking techniques used by malware detection systems.
- **Elevated Privilege Checks**: It ensures that it is run with elevated privileges (administrator rights), which are necessary for accessing `lsass.exe` memory.
- **Debug Privilege Enabling**: The utility attempts to enable debug privileges for the process to ensure it can access sensitive processes like `lsass.exe`.
- **Memory Dumping**: Utilizes the `MiniDumpWriteDump` function to create a complete memory dump of `lsass.exe`, which can be useful for forensic analysis and security research.

## System Requirements
- Windows operating system with administrative privileges.
- Proper configuration to allow for direct system calls (may require adjustments on different versions of Windows).

Use this table for Syscall Numbers (https://j00ru.vexillium.org/syscalls/nt/64/)


