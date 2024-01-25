# VScode
setup .json debugger

// -----------------------------------------------------------------------------------------
tasks.json



{
        "type": "cppbuild",
        "label": "C/C++: g++.exe build active file",
        "command": "C:\\MinGW\\bin\\g++.exe",
        "args": [
            "-g",
            "${file}",
            "-o",
            "${fileDirname}\\${fileBasenameNoExtension}.exe"
        ],
        "options": {
            "cwd": "${workspaceFolder}"
        },
        "problemMatcher": [
            "$gcc"
        ],
        "group": {
            "kind": "build",
            "isDefault": true
        },
        "detail": "Task generated by Debugger."
    }

launch.json

{
        "name": "g++.exe - Build and debug active file",
        "type": "cppdbg",
        "request": "launch",
        "program": "${fileDirname}\\${fileBasenameNoExtension}.exe",
        "args": [],
        "stopAtEntry": false,
        "cwd": "${fileDirname}",
        "environment": [],
        "externalConsole": false,
        "MIMode": "gdb",
        "miDebuggerPath": "C:\\MinGW\\bin\\gdb.exe",
        "setupCommands": [
          {
            "description": "Enable pretty-printing for gdb",
            "text": "-enable-pretty-printing",
            "ignoreFailures": true
          }
        ],
        "preLaunchTask": "C/C++: g++.exe build active file"
    }

// -----------------------------------------------------------------------------------------
