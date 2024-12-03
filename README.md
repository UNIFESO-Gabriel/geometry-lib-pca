# Geometry Library

A modern Python library for geometric calculations, providing an object-oriented interface for manipulating geometric shapes.

## Overview

Geometry Library provides an elegant and extensible way to perform geometric calculations in Python. Using solid object-oriented design principles and design patterns, the library allows you to create and manipulate various geometric shapes in a consistent manner.

## Features

- Unified interface for all geometric shapes
- Support for circles, rectangles, triangles, and regular polygons
- Precise area and perimeter calculations
- Robust input validation
- Factory pattern implementation for object creation
- Static typing for enhanced safety and better documentation

## Installation

First of all, make sure you have already generated a token in PyPI using your account. Add the token as a environment variable by typing in console:

```bash
export PYPI_TOKEN=your-token-here
```
where you must replace the text `your-token-here` by your token.

Next, it is necessary to grant permissions to `build.sh`  before executing it:

```bash
chmod +x build.sh
```

Now, run the script by typing the following command:

```bash
./build.sh
```

If everything goes right, you will be able to install the library in a client project using pip:

```bash
pip install geometry-lib-pca
```

## Example of Client Application

```python
from geometry_lib.shapes.base import Polygon
from geometry_lib import ShapeFactory, ShapeType

# Create a circle
circle = ShapeFactory.create(ShapeType.CIRCLE, 5)
print(f"Circle area: {circle.compute_area():.2f}")
print(f"Circle circumference: {circle.compute_perimeter():.2f}")

# Create a rectangle
rectangle = ShapeFactory.create(ShapeType.RECTANGLE, 4, 6, 4, 6)
print(f"Rectangle area: {rectangle.compute_area():.2f}")
print(f"Rectangle perimeter: {rectangle.compute_perimeter():.2f}")

# Create a triangle
triangle = ShapeFactory.create(ShapeType.TRIANGLE, 3, 4, 5)
print(f"Triangle area: {triangle.compute_area():.2f}")
print(f"Triangle perimeter: {triangle.compute_perimeter():.2f}")
```

## Requirements

- Python 3.9 or higher

## Development

To set up the development environment:

```bash
# Clone the repository
git clone https://github.com/UNIFESO-Gabriel/geometry-lib-pca.git
cd geometry-lib

# Install development dependencies
poetry install
```

To run tests:

```bash
poetry run pytest -v ./tests
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.
