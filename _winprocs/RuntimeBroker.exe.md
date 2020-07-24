---
description: |
  RuntimeBroker.exe acts as a proxy between the constrained
  Universal Windows Platform (UWP) apps (formerly called Metro apps) and the
  full Windows API. UWP apps have limited capability to interface with hardware
  and the file system. Broker processes such as RuntimeBroker.exe
  are therefore used to provide the necessary level of access for UWP
  apps. Generally, there will be one `RuntimeBroker.exe` for each UWP
  app. For example, starting `Calculator.exe` will cause a corresponding
  `RuntimeBroker.exe` process to initiate.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\RuntimeBroker.exe'
  parentprocess:
    short: svchost.exe
    long: svchost.exe
  numberofinstances:
    short: 1+
    long: One or more
  useraccount:
    short: User's
    long: Typically the logged-on user(s)
  starttime:
    short: Varies
    long: Start times vary greatly
---
