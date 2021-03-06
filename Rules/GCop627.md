﻿# GCop 627

> *"Instead of « ?? false » use the more readable expression of « == true »"*
> 
> *"Instead of !(nullable expression == true) use the more readable alternative of: (nullable expression == false)."*

## Rule description

Human brain can understand positive phrases better than negative ones. When dealing with expressions that are `Nullable<bool>`, using `?? false` is the same as using `== true` whether the expression's value is `true`, `false` or `null`.

## Example1

```csharp
var nullableBool = GetSomeNullableBool(...);
...
if(nullableBool ?? false)
{
   ...
}
```

*should be* 🡻

```csharp
var nullableBool = GetSomeNullableBool(...);
...
if(nullableBool == true)
{
   ...
}
```

## Example2

```csharp
if (!nullableBool == true)
{
   ...
}
```

*should be* 🡻

```csharp
if (nullableBool == false)
{
   ...
}
```
