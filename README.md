# Dock Panel C++ Application

A Windows dock panel application built with C++ and Win32/GDI.

## Project Structure

```
/workspace
└── src/                    # C++ source files
    ├── main.cpp           # Application entry point and message loop
    ├── button.h           # Button class declarations
    ├── button.cpp         # Button implementations
    ├── dock_panel.h       # DockPanel class declaration
    └── dock_panel.cpp     # DockPanel implementation
```

## Building the C++ Application (Windows)

Requires Visual Studio with C++ workload and Windows SDK:

```bash
# Using MSBuild (if .sln file exists)
msbuild src/dock_panel.sln /p:Configuration=Release

# Or compile manually
g++ -o dock_panel.exe src/*.cpp -lgdi32 -luser32 -lshell32 -mwindows
```

## Architecture

The codebase follows Google C++ Style Guide with clear separation of concerns:

- **Button classes** (`button.h/cpp`): Abstract base class and concrete implementations
- **DockPanel** (`dock_panel.h/cpp`): UI composition and event handling
- **Main** (`main.cpp`): Windows message loop and initialization

## Development Workflow

1. Make changes to C++ code in `src/`
2. Build and run the application locally to verify behavior
3. Commit and push

## Requirements

- **Runtime**: Windows 10+
- **Development**: Visual Studio 2019+ or MinGW with Win32 support
