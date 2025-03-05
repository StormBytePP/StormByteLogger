# StormByte

StormByte is a comprehensive, cross-platform C++ library aimed at easing system programming, configuration management, logging, and database handling tasks. This library provides a unified API that abstracts away the complexities and inconsistencies of different platforms (Windows, Linux).

## Features

- **System Operations**: Handles pipes, processes, and system variables seamlessly across different platforms.
- **Configuration Management**: Provides an intuitive API for reading and writing configuration files.
- **Logging**: Supports various logging levels and outputs, including file-based logging.
- **Database Handling**: Includes SQLite support for embedded database management while hiding SQLite3 internals conveniently.

## Table of Contents

- [Installation](#Installation)
- [Modules](#Modules)
	- [Base](https://dev.stormbyte.org/StormByte)
	- [Config](https://dev.stormbyte.org/StormByte-Config)
	- [Database](https://dev.stormbyte.org/StormByte-Database)
	- **Logger**
	- [System](https://dev.stormbyte.org/StormByte-System)
- [Contributing](#Contributing)
- [License](#License)

## Installation

### Prerequisites

Ensure you have the following installed:

- C++23 compatible compiler
- CMake 3.12 or higher
- SQLite3 (for database support)

### Building

To build the library, follow these steps:

```sh
git clone https://github.com/StormBytePP/StormByte-Logger.git
cd StormByte-Logger
mkdir build
cd build
cmake ..
make
```

## Modules

StormByte Library is composed by several modules:

### Logger

The `Log` module provides a comprehensive logging framework with support for different logging levels and outputs.

#### Example: Log

```cpp
#include <logger/logger.hxx>
#include <iostream>

using namespace StormByte::Logger;

// Example usage
int main() {
	// Simple logger outputing only errors to stdout
	Logger logger(std::cout, StormByte::Log::Level::Error);
	logger << Level::Info << "This is an info message"; // Will not be displayed
	logger << Level::Error << "This is an error message"; // Will be displayed
	return 0;
}
```

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests for any enhancements or bug fixes.

## License

This project is licensed under GPL v3 License - see the [LICENSE](LICENSE) file for details.
