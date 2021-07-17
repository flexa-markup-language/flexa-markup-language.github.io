# C# BPS Handler

## Handler Common Operations

#### Adding and removing data

```csharp
public void Foo()
{
    BPSFile file = new BPSFile();

    // Adding values
    file.Add("key", "value");
    file.Add("int", 10);
    file.Add("float", 1.5);
    file.Add("bool", true);
    file.Add("arr", new List<object> { 0, 1, 2 });

    // Removing values
    file.Remove("key");
    file.Remove("arr");
}
```

#### Disk operations

```csharp
public void Foo(string path)
{
    // Loading a BPS file from disk
    BPSFile file = BPS.Load(path);
    // Adding a value
    file.Add("string", "example");
    // Saving new file
    BPS.Save(file, path);
}
```

---

[Back](index.md)
