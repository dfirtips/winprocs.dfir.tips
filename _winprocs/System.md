---
description: |
  The `System` process responsible for most kernel-mode threads. Modules run
  under System are primarily drivers (`.sys` files), but also include several
  important DLLs as well as the kernel executable, `ntoskrnl.exe`
characteristics:
  imagepath:
    short: N/A
    long: N/A for system.exe - Not generated from an executable image
  parentprocess:
    short: None
    long: None
  numberofinstances:
    short: 1
    long: One
  useraccount:
    short: SYSTEM
    long: Local System
  starttime:
    short: Boot time
    long: At boot time
---
