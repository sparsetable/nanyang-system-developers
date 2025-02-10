
# Advanced Annotations and Type Checking

## Overview

While basic type hints help document parameter and return types, Python's type system offers more sophisticated features for complex data structures and relationships. Advanced annotations allow for more precise type specifications and enable static type checkers to catch potential errors before runtime.

## Type Aliases

Type aliases help simplify complex type annotations:

```python
from typing import Dict, List, Union

# Instead of this
def process_data(records: Dict[str, Union[int, float, str]]) -> List[Dict[str, Union[int, float, str]]]:
    pass

# Use a type alias
DataRecord = Dict[str, Union[int, float, str]]
def process_data(records: DataRecord) -> List[DataRecord]:
    pass
```

## Generics

Generics allow you to write code that works with multiple types while maintaining type safety:

```python
from typing import TypeVar, List

T = TypeVar('T')

def first_element(lst: List[T]) -> T:
    return lst[0]

# Works with any type
first_element([1, 2, 3])  # Returns int
first_element(['a', 'b'])  # Returns str
```

## Type Checking Tools

### mypy

`mypy` is a static type checker that can analyze your code for type errors:

```python
# example.py
def greet(name: str) -> str:
    return "Hello " + name

# Type error caught by mypy
greet(123)  # Error: Argument 1 to "greet" has incompatible type "int"; expected "str"
```

### Protocols

Protocols define interfaces through method signatures rather than inheritance:

```python
from typing import Protocol

class Drawable(Protocol):
    def draw(self) -> None:
        ...

def render(thing: Drawable) -> None:
    thing.draw()
```

## Best Practices

1. Use type checkers in CI/CD pipelines
2. Document type variables and complex type hierarchies
3. Consider gradual typing for large codebases
4. Use composition of types for complex structures

## Further Reading

- [PEP 593 – Flexible function and variable annotations](https://peps.python.org/pep-0593/)
- [mypy documentation](https://mypy.readthedocs.io/)
