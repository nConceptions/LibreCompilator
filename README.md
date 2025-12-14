# LibreCompilator

A simple, educational compiler written in C++ that demonstrates the core phases of compilation: lexical analysis, parsing, semantic analysis, and code generation.

## Features

- **Lexical Analysis**: Tokenizes source code into meaningful symbols
- **Parser**: Builds an Abstract Syntax Tree (AST) from tokens
- **Semantic Analysis**: Type checking and symbol table management
- **Code Generation**: Generates target code (currently C code as intermediate)
- **Cross-platform**: Works on Windows, macOS, and Linux
- **Extensible**: Modular architecture for easy enhancement

## Project Structure

```
LibreCompilator/
├── src/
│   ├── arena.hpp
│   ├── generation.hpp
│   ├── main.cpp
│   ├── parser.hpp
│   ├── tokenization.hpp
│
├── docs/
│   ├── gammar.md
│
├── CMakeLists.txt
├── .clang-format
├── .gitattributes
├── .gitignore
├── test.hy
├── LICENSE.md
└── README.md
```

## Building

### Prerequisites

- C++17 compatible compiler (GCC 7+, Clang 5+, MSVC 2017+)
- CMake 3.10 or higher

### Build Instructions

#### On Windows:

```bash
mkdir build
cd build
cmake ..
cmake --build . --config Release
```

#### On macOS/Linux:

```bash
mkdir build
cd build
cmake ..
make
```

## Usage

```bash
./LibreCompilator input.lc -o output.c
```

### Options

- `-o <file>`: Specify output file (default: output.c)
- `-h, --help`: Display help message
- `-v, --version`: Display version information

## Language Syntax

LibreCompilator supports a simple C-like language:

```c
// Variable declarations
int x = 10;
float y = 3.14;

// Functions
func add(int a, int b) -> int {
    return a + b;
}

// Control flow
if (x > 5) {
    print(x);
} else {
    print(0);
}

// Loops
while (x > 0) {
    x = x - 1;
}
```

## Supported Types

- `int`: Integer type
- `float`: Floating-point type
- `bool`: Boolean type
- `void`: Void type (for functions)

## Example

Input file (`example.lc`):

```c
func factorial(int n) -> int {
    if (n <= 1) {
        return 1;
    }
    return n * factorial(n - 1);
}

int result = factorial(5);
print(result);
```

Compile and run:

```bash
./LibreCompilator example.lc -o example.c
gcc example.c -o example
./example
```

## Development

### Adding New Features

1. **Lexer**: Add new token types in `include/common.h`
2. **Parser**: Extend grammar rules in `src/parser/parser.cpp`
3. **AST**: Add new node types in `src/parser/ast.h`
4. **Semantic**: Add checks in `src/semantic/semantic.cpp`
5. **CodeGen**: Implement code generation in `src/codegen/codegen.cpp`

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

## License

MIT License - feel free to use this project for educational purposes.

## Authors

Created as an educational compiler project demonstrating compilation principles.
