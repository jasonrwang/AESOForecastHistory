---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.2'
      jupytext_version: 1.3.2
  kernelspec:
    display_name: Julia 1.5.3
    language: julia
    name: julia-1.5
---

# Example Notebook

```julia
# Activate project environment
] activate ../
```

```julia
# Confirm what is in Project.toml file
print(read("../Project.toml", String))
```

```julia
using DataFrames
using Gadfly
```

## Data


Create some random data to plot

```julia
x = 1:10;
y = rand(10);
```

```julia
df = DataFrame(x=x, y=y)
```

```julia
df
```

## Plot

```julia
plot(df, x=:x, y=:y,  Geom.point)
```

```julia

```
