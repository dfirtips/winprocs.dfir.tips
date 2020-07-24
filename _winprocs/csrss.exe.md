---
description: |
  The Client/Server Run-Time Subsystem is the user-mode process for the Windows subsystem. Its duties
  include managing processes and threads, importing many of the DLLs that provide the Windows API, and facilitating
  shutdown of the GUI during system shutdown. An instance of `csrss.exe` will run for each session. Session 0 is for
  services and Session 1 for the local console session. Additional sessions are created through the use of Remote
  Desktop and/or Fast User Switching. Each new session results in a new instance of `csrss.exe`. 
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\csrss.exe'
  parentprocess:
    short: None
    long: Created by an instance of smss.exe that exits, so analysis tools usually do not provide the parent process name.
  numberofinstances:
    short: 2+
    long: Two or more
  useraccount:
    short: SYSTEM
    long: Local System
  starttime:
    short: Multiple
    long: Within seconds of boot time for the first two instances (for Session 0 and 1). Start times for additional instances occur as new sessions are created, although often only Sessions 0 and 1 are created.
---
