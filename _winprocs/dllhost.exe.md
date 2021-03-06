---
description: |
  The process for running DLL Surrogate COM Objects's on Windows. The dllhost process executes what is known as "Dll surrogates", which are DLL's hosting COM objects running inside processes. The command line argument of the dllhost process is `/Processid:{CLSID}`. Malware author or threat actors can abuse this by registering / hijacking COM Objects and running them via the following command line `dllhost.exe /Processid:{Hijacked CLSID}` utility.
characteristics:
  imagepath:
    short: System32 dir
    long: '%SystemRoot%\System32\dllhost.exe'
  parentprocess:
    short: svchost.exe
    long: Most of the time only two instances of DLLHOST are running on a system as children of "svchost -k DcomLaunch -p" responsible for showing thumbnails, any other process spawned will be as a child of an "svchost.exe" process and the COM object should be refernced from the registry.
  numberofinstances:
    short: 1+
    long: One or more
  useraccount:
    short: 2
    long: Two or more.
  starttime:
    short: Varies
    long: The dllhost process responsible for the "Thumbnail Cache" starts shortly after the service responsible for handling DCOM objects, which in it self start with the system.
---
