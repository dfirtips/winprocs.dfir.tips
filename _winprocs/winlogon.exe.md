---
description: |
  Winlogon handles interactive user logons and logoffs. It launches
  `LogonUI.exe`, which uses a credential provider to gather credentials from the
  user, and then passes the credentials to `lsass.exe` for validation. Once the
  user is authenticated, Winlogon loads the user’s `NTUSER.DAT` into `HKCU` and
  starts the user’s shell (usually `explorer.exe`) via `userinit.exe`.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\winlogon.exe'
  parentprocess:
    short: None
    long: Created by an instance of `smss.exe` that exits, so analysis tools usually do not provide the parent process name
  numberofinstances:
    short: 1+
    long: One or more
  useraccount:
    short: SYSTEM
    long: Local System
  starttime:
    short: Multiple
    long: Within seconds of boot time for the first instance (for Session 1). Start times for additional instances occur as new sessions are created, typically through Remote Desktop or Fast User Switching logons.
---
