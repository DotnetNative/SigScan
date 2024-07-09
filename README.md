# SigScan [![NuGet](https://img.shields.io/nuget/v/Yotic.SigScan.svg)](https://www.nuget.org/packages/Yotic.SigScan)

Library providing classes and methods for internal signatute scan

Create pattern for signature scan
------------------------------
```C#
Mem.CreatePattern("0 2F 90 ?") // 00 2F 90 ??
Mem.CreatePattern("0 0x2F 90 ?????") // 00 2F 90 ??
Mem.CreatePattern("00 2F 90 .") // 00 2F 90 ??

Mem.CreatePattern(2d) // 0x40 00 00 00 00 00 00 00
// So work for all primitive types

Mem.CreatePattern([0, 0x2F, 0x90, null]) // 00 2F 90 ??
```

Signature scan
------------------------------
```C#
var regions = ...;
var pattern = ...;
var found = Mem.Scan(pattern, regions);
```

Used Libraries
------------------------------
**DotnetNativeBase** [![NuGet](https://img.shields.io/nuget/v/DotnetNativeBase.svg)](https://www.nuget.org/packages/DotnetNativeBase) \
**Yotic.Memory.Extensions** [![NuGet](https://img.shields.io/nuget/v/Yotic.Memory.Extensions.svg)](https://www.nuget.org/packages/Yotic.Memory.Extensions) \
**Memory.Manipulation** [![NuGet](https://img.shields.io/nuget/v/Memory.Manipulation.svg)](https://www.nuget.org/packages/Memory.Manipulation)

Versions
------------------------------
| Start ordinal | Framework | Description                  | Date         |
| ---           | ---       | ---                          | ---          |
| 1.0.0         | .net8.0   | Published                    | Apr 30, 2024 |
