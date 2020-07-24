---
description: |
  At its core, Explorer provides users access to files. Functionally, though, it is both a file browser
  via Windows Explorer (though still `explorer.exe`) and a user interface providing features such as the user’s
  Desktop, the Start Menu, the Taskbar, the Control Panel, and application launching via file extension associations
  and shortcut files. `Explorer.exe` is the default user interface specified in the Registry value `HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon\Shell`, though Windows can alternatively function with
  another interface such as `cmd.exe` or `powershell.exe`. Notice that the legitimate explorer.exe resides in the
  `%SystemRoot%` directory rather than `%SystemRoot%\System32`. Multiple instances per user can occur, such as
  when the option "Launch folder windows in a separate process" is enabled.
characteristics:
  imagepath:
    short: '%SystemRoot%'
    long: '%SystemRoot%\explorer.exe'
  parentprocess:
    short: None
    long: Created by an instance of userinit.exe that exits, so analysis tools usually do not provide the parent process name.
  numberofinstances:
    short: 1+
    long: One or more per interactively logged-on user
  useraccount:
    short: User's
    long: '<logged-on user(s)>'
  starttime:
    short: Interactive logon
    long: First instance starts when the owner’s interactive logon begins
---
