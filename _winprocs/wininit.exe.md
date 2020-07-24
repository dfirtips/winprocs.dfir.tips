---
description: |
  Wininit.exe starts key background processes within Session 0.
  It starts the Service Control Manager (`services.exe`), the Local Security
  Authority process (`lsass.exe`), and `lsaiso.exe` for systems with Credential
  Guard enabled. Note that prior to Windows 10, the Local Session Manager
  process (`lsm.exe`) was also started by wininit.exe. As of Windows 10, that
  functionality has moved to a service DLL (`lsm.dll`) hosted by `svchost.exe`. 
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\wininit.exe'
  parentprocess:
    short: None
    long: Created by an instance of `smss.exe` that exits, so tools usually do not provide the parent process name
  numberofinstances:
    short: 1
    long: One
  useraccount:
    short: SYSTEM
    long: Local System
  starttime:
    short: Around boot
    long: Within seconds of boot time
---
