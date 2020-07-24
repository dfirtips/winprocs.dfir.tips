---
description: |
  The Session Manager process is responsible for creating new sessions. The first instance creates a child instance for each new session. Once the child instance initializes the new session by starting the Windows subsystem (`csrss.exe`) and `wininit.exe` for Session 0 or `winlogon.exe` for Session 1 and higher, the child instance exits.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\smss.exe'
  parentprocess:
    short: System
    long: System
  numberofinstances:
    short: 1+
    long: One master instance and another child instance per session. Children exit after creating their session.
  useraccount:
    short: SYSTEM
    long: Local System
  starttime:
    short: Around boot
    long: Within seconds of boot time for the master instance
---
