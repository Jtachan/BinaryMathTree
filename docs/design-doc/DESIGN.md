# Design Document - Binary Math Trees (BMT)

## Overview

A _Binary Math Tree_ (**BMT**) is defined within this project as a tree capable of containing operations with binary operators.
Each tree is composed by the left and right operands, as well as the math operator to be performed among them.
Each operan can also be defined as a branch of variable depth.

The BMT differs from the AST as it cannot hold any syntaxis, only math equations with limited functions.

**Examples**

All the examples are defined with python math notation.

> A + B

```json
{
    "op": "SUM",
    "left": "A",
    "right": "B"
}
```

> A * T + B ** (1 / 2)

```json
{
    "op": "SUM",
    "left": {
        "op": "MUL",
        "left": "A",
        "right": "T"
    },
    "right": {
        "op": "POW",
        "left": "B",
        "right": {
            "op": "DIV",
            "left": 1,
            "right": 2
        }
    }
}
```
