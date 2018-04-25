﻿# GCop 513

> *"It should be written as \{Collection}.FirstOfDefault(\{argument}) ?? \{conditionWhenFalse}."*

## Rule description

The `FirstOrDefault` is almost the same as `First`. The difference is how it handles empty collections. If a collection is empty, it returns the default value for the type. It is more easy to undrestand than using `Any()` and `First` in a comnditional phrase.

## Example

```csharp
 var myResult = myList.Any() ? myList.First(f => f.ID == 2) : null;
```

*should be* 🡻

```csharp
 var myResult = myList.FirstOrDefault() ?? null;
```