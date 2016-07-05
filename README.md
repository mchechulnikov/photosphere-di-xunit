# Photosphere.DependencyInjection.xUnit
xUnit extension for support Photosphere.DependencyInjection.

## Install
Will be available throught NuGet soon!

## How to use
Just use `InjectDependency` instead `InlineData` into your theories.
``` C#
[Theory]
[InjectDependency(42, "foo")]
void Test(int someNumber, string someString, IFoo foo, IBar bar)
{
  Assert.Equal(42, someNumber);
  Assert.Equal("foo", someString);
  Assert.NotNull(foo);
  Assert.NotNull(bar);
}

```
