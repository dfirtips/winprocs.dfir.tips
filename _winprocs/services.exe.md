---
description: |
  Implements the Unified Background Process Manager (UBPM), which is responsible for background
  activities such as services and scheduled tasks. `Services.exe` also implements the Service Control Manager (SCM),
  which specifically handles the loading of services and device drivers marked for auto-start. In addition, once a user
  has successfully logged on interactively, the SCM (`services.exe`) considers the boot successful and sets the Last
  Known Good control set (`HKLM\SYSTEM\Select\LastKnownGood`) to the value of the CurrentControlSet.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\services.exe'
  parentprocess:
    short: wininit.exe
    long: wininit.exe
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
