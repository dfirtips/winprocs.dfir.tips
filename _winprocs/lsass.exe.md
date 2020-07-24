---
description: |
  The Local Security Authentication Subsystem Service process is responsible for authenticating users by
  calling an appropriate authentication package specified in `HKLM\SYSTEM\CurrentControlSet\Control\Lsa`.
  Typically, this will be Kerberos for domain accounts or MSV1_0 for local accounts. In addition to authenticating
  users, `lsass.exe` is also responsible for implementing the local security policy (such as password policies and
  audit policies) and for writing events to the security event log. Only one instance of this process should occur and it
  should not have child processes. 
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\lsass.exe'
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
