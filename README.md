

# LuaFileSystem with CMake Support

Forked from https://lunarmodules.github.io/luafilesystem.

## Description

- LuaFileSystem is a Lua library developed to complement the set of functions related to file systems offered by the standard Lua distribution.

- LuaFileSystem offers a portable way to access the underlying directory structure and file attributes.
- LuaFileSystem is free software and uses the same license as Lua 5.x (MIT).

## Building and Installing LuaFileSystem

### Prerequisites

LuaFileSystem with CMake Support relies on an installation of [Lua with CMake Support](https://github.com/KritzelKratzel/lua#readme). The same toolchain which has been used with *Lua with CMake Support* is required. LuaFileSystem gets all necessary path, header and library information from CMake `liblua` package data and will be installed automatically into the right directory locations - no hassle with `package.path` settings anymore.

**Notice:** Present `Makefiles`  stem from original LuaFileSystem source code and are not used within the context of the CMake-based build infrastructure. Simply ignore them.

### Build and Install

Open `Developer Command Prompt for VS 2022` and change drive and directory. Download and unpack sources or simply clone this repository:

```cmd
c:
cd c:\Temp
git clone https://github.com/KritzelKratzel/luafilesystem
cd luafilesystem
```

CMake strongly encourages out-of-source builds.

```cmd
mkdir build
cd build
cmake .. -G "Visual Studio 17 2022" -A <arch>
cmake --build . --config Release
cmake --install . --config Release
```

Replace `<arch>` with your desired architecture. Available architectures with selected `Visual Studio 17 2022` generator are `Win32`, `x64`, `ARM` and `ARM64`. LuaFileSystem documentation is available in `<lua_install_dir>/share/doc/luafilesystem` after install and also at the [project website](https://lunarmodules.github.io/luafilesystem).

## Sync this fork with original LuaFileSystem repository

Open Git Bash and execute `./SyncFork.sh`.

```bash
John Doe@DESKTOP-1HK25HF MINGW64 /c/misc/luafilesystem (master)
$ ./SyncFork.sh
Original remote repo found.
Already on 'master'
Your branch is up to date with 'origin/master'.
From github.com:KritzelKratzel/luafilesystem
 * branch            master     -> FETCH_HEAD
Already up to date.
Already up to date.
Everything up-to-date
John Doe@DESKTOP-1HK25HF MINGW64 /c/misc/luafilesystem (master)
```

