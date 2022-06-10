## Processes Exploration
### Volatility - plugins
* [pslist - walks the doubly-linked list pointed to by PsActiveProcessHead](https://github.com/volatilityfoundation/volatility/wiki/Command-Reference#pslist)
* [pstree - print process tress](https://github.com/volatilityfoundation/volatility/wiki/Command-Reference#pstree)
* [psscan - enumerate processes using pool tag scanning](https://github.com/volatilityfoundation/volatility/wiki/Command-Reference#psscan)
* [psdispscan - enumerates processes by scanning for DISPATCHER_HEADER](https://github.com/volatilityfoundation/volatility/wiki/Command-Reference#psdispscan)
* [psxview - Detect hidden processes](https://github.com/volatilityfoundation/volatility/wiki/Command-Reference-Mal#psxview)      
### Rekall   
* [pslist - list processes using all methods by default.](https://rekall.readthedocs.io/en/latest/plugins.html#pslist-winpslist)
* [pstree - walk the task_struct.children and task_struct.sibling members to print process tress.](https://rekall.readthedocs.io/en/latest/plugins.html#pstree-linpstree)
* [psscan - Scan Physical memory for \_EPROCESS pool allocations.](https://rekall.readthedocs.io/en/latest/pluins.html#psscan-psscan)
* [psxview - Find hidden processes with various process listings](https://rekall.readthedocs.io/en/latest/plugins.html#psxview-windowspsxview)      
### [volatility - volshell](https://github.com/volatilityfoundation/volatility/wiki/Command-Reference#volshell)   
* ps() -> List processes
* dt("[_EPROCESS](https://web.archive.org/web/20210302232116/https://www.geoffchappell.com/studies/windows/km/ntoskrnl/inc/ntos/ps/eprocess/index.htm)", 0xvirtualadderss, space=addrspace) -> Expand the EPROCEES structure using virtual address
* dt("[_EPROCESS](https://web.archive.org/web/20210302232116/https://www.geoffchappell.com/studies/windows/km/ntoskrnl/inc/ntos/ps/eprocess/index.htm)", 0xphysicaladderss, space=addrspace) -> Expand the EPROCEES structure using physical address
### Notes
* Providing KDBG virtual offsets to volatility with '-g' will speed up the process.