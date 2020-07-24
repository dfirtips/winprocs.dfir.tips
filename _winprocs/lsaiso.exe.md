---
description: |
  When Credential Guard is enabled, the functionality of lsass.exe is split between two processes –
  itself and `lsaiso.exe`. Most of the functionality stays within `lsass.exe`, but the important role of safely storing
  account credentials moves to `lsaiso.exe`. It provides safe storage by running in a context that is isolated from other
  processes through hardware virtualization technology. When remote authentication is required, `lsass.exe` proxies
  the requests using an RPC channel with lsaiso.exe in order to authenticate the user to the remote service. Note
  that if Credential Guard is not enabled, `lsaiso.exe` should not be running on the system. 
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\lsaiso.exe'
  parentprocess:
    short: wininit.exe
    long: wininit.exe
  numberofinstances:
    short: 0 - 1
    long: Zero or one
  useraccount:
    short: SYSTEM
    long: Local System
  starttime:
    short: Around boot
    long: Withing seconds of boot time
---
