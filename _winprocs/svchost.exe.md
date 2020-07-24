---
description: |
  Generic host process for Windows services. It is used for running service DLLs. Windows will
  run multiple instances of svchost.exe, each using a unique `“-k”` parameter for grouping similar services.
  Typical `“-k”` parameters include DcomLaunch, RPCSS, LocalServiceNetworkRestricted, LocalServiceNoNetwork,
  LocalServiceAndNoImpersonation, netsvcs, NetworkService, and more. Malware authors often take advantage of the
  ubiquitous nature of svchost.exe and use it either to host a malicious DLL as a service, or run a malicious process
  named `svchost.exe` or similar spelling. Beginning in Windows 10 version 1703, Microsoft changed the default
  grouping of similar services if the system has more than 3.5 GB of RAM. In such cases, most services will run under
  their own instance of `svchost.exe`. On systems with more than 3.5 GB RAM, expect to see more than 50 instances of `svchost.exe`
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\system32\svchost.exe'
  parentprocess:
    short: services.exe
    long: services.exe
  numberofinstances:
    short: ~10+
    long: Many (generally at least 10)
  useraccount:
    short: Multiple
    long: Varies depending on svchost instance, though it typically will be Local System, Network Service, or Local Service accounts. Windows 10 also has some instances running as logged-on users.
  starttime:
    short: Varies
    long: Typically within seconds of boot time. However, services can be started after boot (e.g., at logon), which results in new instances of svchost.exe after boot time
---
