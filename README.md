# <a name="top"></a>BPS - Basic Persistence System

BPS is a key-value data storing structure. It allows to store data in several types, even array.


## <a name="menu"></a>Contents

- [Introduction](#introduction)
  * [Features](#features)
  * [Example](#example)
- [Getting Started](#getting-started)
  * [Download & Installation](#download)
- [Documentation](documentation/index.md)
- [License](#license)


## <a name="introduction"></a>Introduction

### <a name="features"></a>Features

- In-code key-value data structure;
- Key-value data persistence;
- Allows store multi-dimensional arrays.


### <a name="example"></a>Example

Here are most common operations in BPS.

#### BPS data storing structure examples

```

# This is a comment

# Literals
string:"strings are in double quotes";
char:'c';

# Numerics
int:10;
float:0.5;

# Booleans
boolTrue:true;
boolFalse:false;

# Vector
stringArr:["yes", "no", "maybe"];
chargArr:['a', 'b', 'c'];
intArr:[0, 1, 2, 10, -5];
floatArr:[0.9, 1.7, -0.2, 1.06, -5.618];
boolArr:[true, false, true];

# Multdimensional array
multArr2:[
  [0, 1, 2],
  [0, 1, 2],
  [0, 1, 2]
];

# And so on
multArr3:[
  [
    [0, 1, 2],
    [0, 1, 2],
    [0, 1, 2]
  ],
  [
    [0, 1, 2],
    [0, 1, 2],
    [0, 1, 2]
  ],
  [
    [0, 1, 2],
    [0, 1, 2],
    [0, 1, 2]
  ]
];

```

#### BPS C# handler common operations

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


## <a name="getting-started"></a>Getting Started

Follow the steps here to get started with BPS.

### <a name="download"></a>Download & Installation

BPS is a data storing structure definition and can be implemented in several languages.

#### <a name="installation"></a> C# BPS Handler Installation

It can be downloaded [here]().
TODO: write installation steps


## <a name="license"></a>License

All BPS projects are open source and released under the [MIT](../LICENSE) license.

<br>

---

[Back top](#top)

<br>
