---
layout: page
title: Contribute
---

## Structure

Each WinProc entry is defined in a file in the [`_winprocs/`] folder named as `<windows process name>.md`, such file consists only of a [YAML] front matter which describes the entry and its characteristics.

The full syntax is the following:

```
---
description: Optional description of the entry
characteristics:
  CHARACTERISTIC:
    description: Optional description of the example
    short: 1
    long: One or more
  CHARACTERISTIC:
    description: Optional description of the example
    short: services.exe
    long: %SystemRoot%\System32\services.exe
  ...
---
```

Where `CHARACTERISTIC` is one of the values described in the [`_data/characteristics.yml`] file.

Feel free to use any file in the [`_winprocs/`] folder as an example.

## Pull request process

Missed or new Windows processes PR are welcomed. Non-Windows related processes are subject of public discussion and will be merged if it proves its rationale.

Pull requests adding new characteristics in [`_data/characteristics.yml`] are allowed and subjected to project maintainers vetting.

[YAML]: http://yaml.org/
[`_data/characteristics.yml`]: https://github.com/dfirtips/winprocs.dfir.tips/blob/master/_data/characteristics.yml
[`_winprocs/`]: https://github.com/dfirtips/winprocs.dfir.tips/blob/master/_winprocs/
