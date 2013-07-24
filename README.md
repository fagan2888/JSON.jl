#JSON parsing and printing for Julia. 
[![Build Status](https://travis-ci.org/aviks/JSON.jl.png)](https://travis-ci.org/aviks/JSON.jl)

##Installation

```julia
Pkg.add("JSON")
```

##Usage

```julia
using JSON
JSON.parse(s)
json(a)
```

##The API

```julia
JSON.print(io::IO, s::String)
JSON.print(io::IO, s::Union(Integer, FloatingPoint))
JSON.print(io::IO, n::Nothing)
JSON.print(io::IO, b::Bool)
JSON.print(io::IO, a::Associative)
JSON.print(io::IO, v::AbstractVector)

Writes a compact (no extra whitespace or identation) JSON representation
to the supplied IO
```

```julia
json(a::Any)

Returns a compact JSON representation as a String
```

```julia
JSON.parse(s::String)
JSON.parse(io::IO)

Parses a JSON String into a nested Array or Dict
```
