# LibreCompilator

LibreCompilator is a Compialtor written in C++ 

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

Requires `nasm` and `ld` on a Linux operating system.

```bash
git clone https://github.com/nConceptions/LibreCompilator
cd LibreCompilator
mkdir build
cmake -S . -B build
cmake --build build
```

Executable will be `hydro` in the `build/` directory.

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

## Credits
Credits go out to Pixeled. Without him this <b>wouldn't be possible.</b>
<br>
"[Pixeled's Channel](https://www.youtube.com/@pixeled-yt)"

## License 

MIT License - feel free to use this project for educational purposes.
