
# Docstrings and Annotations

## Overview

Docstrings and annotations are essential tools for documenting Python code and specifying type hints. They help make code more maintainable and self-documenting.

## Key Concepts

### Docstrings
- **Function Docstrings**: Document function purpose, parameters, and return values
- **Class Docstrings**: Describe class purpose and behavior
- **Module Docstrings**: Explain module contents and usage
- **Google Style**: Preferred format for Python documentation

### Type Annotations
- **Function Annotations**: Specify parameter and return types
- **Variable Annotations**: Declare variable types
- **Type Hints**: Import types from typing module
- **Optional and Union Types**: Handle multiple possible types

## Examples

```python
from typing import List, Optional

def calculate_average(numbers: List[float]) -> float:
    """Calculate the average of a list of numbers.
    
    Args:
        numbers: List of numbers to average
        
    Returns:
        float: The calculated average
        
    Raises:
        ValueError: If the input list is empty
    """
    if not numbers:
        raise ValueError("Cannot calculate average of empty list")
    return sum(numbers) / len(numbers)
```

## Best Practices
- Write clear, concise docstrings
- Use type annotations for better code understanding
- Follow consistent documentation style
- Keep docstrings up-to-date with code changes
