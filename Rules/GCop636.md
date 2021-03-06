﻿# GCop 636

> *"It should be written as if ( {'NullableObject'}?.{'YourProperty'} == someValue)"*

## Rule description

The `?.` operator lets you access members and elements only when the receiver is not-null, returning null result otherwise. It is exactly what we except when checking an object is null or not like the samples below, while `?.` is more meaningful and readable.

## Example

```csharp
if(myObject != null && myObject.myProperty == 0)
{
    ....
}
```

*should be* 🡻

```csharp
if(myObject?.myProperty == 0)
{
    ....
}
```