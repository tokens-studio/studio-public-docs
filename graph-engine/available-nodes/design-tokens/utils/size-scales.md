# Size Scales

### What It Does
The Size Scales utility provides standardized naming conventions for size-based scales in design systems. It generates consistent size naming patterns in different formats (default, short, long) that can be used across design token systems.

### How It Works
This utility module generates three different scales:
1. **Default Scale**: Uses standard size abbreviations (xs, sm, md, lg, xl) with numeric prefixes for extended sizes (2xl, 3xl, etc.)
2. **Short Scale**: Uses compact abbreviations (xs, s, m, l, xl) with numeric prefixes
3. **Long Scale**: Uses descriptive names (x-small, small, medium, large, x-large) with multiplicative naming for extended sizes (2x-small, 3x-small, etc.)

### Supported Size Patterns
| Scale Type | Examples |
|------------|----------|
| Default | xs, sm, md, lg, xl, 2xl, 3xl... |
| Short | xs, s, m, l, xl, 2xl, 3xl... |
| Long | x-small, small, medium, large, x-large, 2x-small, 2x-large... |

### Value Ordering
All scales are consistently ordered from smallest to largest, with the numeric values:
- Very small sizes: ..., -4, -3, -2 (xs/x-small)
- Small: -1 (sm/small)
- Medium: 0 (md/medium)
- Large: 1 (lg/large)
- Very large sizes: 2, 3, 4, ... (xl, 2xl, 3xl / x-large, 2x-large, 3x-large)

### Tips
- Choose the scale that best fits your design system's naming conventions.
- The module handles both extended small sizes (2xs, 3xs) and extended large sizes (2xl, 3xl).
- Use the same scale consistently throughout your token system for better readability.

### Use Cases
- **T-shirt Size Node**: Powers the T-shirt Size node's naming schemas.
- **Component Size Variants**: Create consistent size naming across components.
- **Spacing Scales**: Establish readable naming conventions for spacing tokens.
- **Typography Scales**: Define readable size classifications for typography tokens. 