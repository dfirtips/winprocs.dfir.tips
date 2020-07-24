---
description: |
  The generic host process for Windows Tasks. Upon initialization,
  taskhostw.exe runs a continuous loop listening for trigger events. Example
  trigger events that can initiate a task include a defined schedule, user logon,
  system startup, idle CPU time, a Windows log event, workstation lock, or
  workstation unlock.
  There are more than 160 tasks preconfigured on a default installation of
  Windows 10 Enterprise (though many are disabled). All executable files (DLLs &
  EXEs) used by the default Windows 10 scheduled tasks are signed by Microsoft.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\taskhostw.exe'
  parentprocess:
    short: svchost.exe
    long: svchost.exe
  numberofinstances:
    short: 1+
    long: One or more
  useraccount:
    short: Multiple
    long: Multiple taskhostw.exe processes are normal. One or more may be owned by logged-on users and/or by local service accounts.
  starttime:
    short: Varies
    long: Start times vary greatly
---
