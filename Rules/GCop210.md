﻿# GCop 210

> *"Suffix the name of a service class with 'Service' as it's inside the Services folder."*

## Rule description

Using "*Service*" as a suffix for a class indicates that the class represents a service, which is assumed to be remote.

## Example

```csharp
namespace MyNameSpace.Service
{
    public class SampleClass 
    {   
        ...   
    }
}
```

*should be* 🡻

```csharp
namespace MyNameSpace.Service
{
    public class SampleClassService 
    {   
        ...   
    }
}
```