# Nano CC Compiler

A C/C++ compiler with lexical analysis built for educational purposes, demonstrating the key phases of compilation: lexical analysis, syntax analysis, and semantic analysis.

## Features

- Web-based interface for writing and compiling C/C++ code
- Visual representation of compiler phases
- Lexical analysis with token generation
- Syntax analysis with parse table generation
- Interactive terminal for program I/O
- Windows-only environment support

## Project Structure

```
nano-cc-compiler/
├── client/             # React frontend
│   ├── src/           # Source code
│   ├── public/        # Static assets
│   └── package.json   # Frontend dependencies
├── server/            # Node.js backend
│   ├── lexical/       # Lexical analysis implementation
│   ├── syntax/        # Syntax analysis implementation
|   ├── semantic/      # Semantic analysis implementation
│   ├── compiler.bat   # Windows batch script for compilation
│   ├── index.js       # Express server
│   └── package.json   # Backend dependencies
├── start.bat          # Windows startup script
└── package.json       # Root package.json for running both client and server
```

## Getting Started

### Prerequisites

- Windows operating system
- Node.js (v14 or higher)
- npm (v6 or higher)
- GCC compiler (for actually compiling C/C++ code)
- lex (for lexical analysis)
- win_bison (for syntax and semantic analysis)
- Graphviz (for creating graphs)
- Git Bash (for running shell scripts)

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/SanchitNegi177/Nano-CC-Compiler.git
   cd nano-cc-compiler
   ```

2. Install dependencies:
   ```
   npm run install:all
   ```
   This will install dependencies for both client and server.

3. Run the development server:
   ```
   npm run dev
   ```
   Or simply double-click the `start.bat` file.

4. Open your browser and navigate to `http://localhost:3000`

### Windows Setup Requirements

For Windows users:
- The application uses a .bat file for running the compiler process
- Make sure you have GCC installed and added to your PATH
- Make sure you have renamed your 'win_flex.exe' to 'lex.exe'
- Ensure Git Bash is installed (usually comes with Git for Windows)
- Install win_bison for Windows (not the Unix version)

## How It Works

1. User writes C/C++ code in the editor
2. Code is sent to the Node.js backend
3. Backend processes the code through multiple phases:
   - Lexical analysis (token generation)
   - Syntax analysis (parse tree generation)
   - Semantic analysis (Verified AST)
4. Results are sent back to the frontend and displayed
5. The compiled program can be executed and its output viewed in the terminal

## Future Plans

- Implement full Lex/Yacc integration
- Support for more C/C++ language features
- Better error handling and debugging tools
- Integration with LLVM for better code generation
- Support for multiple compiler backends

## License

This project is licensed under the ISC License.

## Acknowledgments

- [React](https://reactjs.org/)
- [Material-UI](https://mui.com/)
- [Monaco Editor](https://microsoft.github.io/monaco-editor/)
- [Express](https://expressjs.com/)
- [GCC](https://gcc.gnu.org/) 
