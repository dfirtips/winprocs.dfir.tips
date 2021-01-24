---
description: |
  The process for running DLL's on Windows. In normal usage the rundll32 process wil execute specific functions of DLL's via the following format  `rundll32.exe <DLL>, <EntryPoint>`. Some DLL's contain special function for running specific files. For example, rundll32 can be used to run `.CPL` files via the `shell32.dll` DLL and the `Control_RunDLL` function. Malware author often abuse this by creating malicious `.CPL` files and running them via the `rundll32` utility.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\rundll32.exe'
  parentprocess:
    short: explorer.exe
    long: Depends from where the action was requested if a user clicks on something in the control panel, you'll see it running as a child of explorer.exe. If the user clicked the network settings from a browser like chrome or IE, you'll see it running as a child of those processes.
  numberofinstances:
    short: 0+
    long: Zero or more
  useraccount:
    short: Multiple
    long: Multiple.
  starttime:
    short: Varies
    long: Start times vary greatly
---
