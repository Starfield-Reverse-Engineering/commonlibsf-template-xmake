# CommonLibSF Plugin Template

This is a basic plugin template using CommonLibSF.

### Requirements
* [XMake](https://xmake.io) [2.8.2+]
* C++23 Compiler (MSVC)

## Getting Started
```bat
git clone https://github.com/Starfield-Reverse-Engineering/template-commonlibsf-xmake
cd template-commonlibsf-xmake
```

### Build
To build the project, run the following command:
```bat
xmake build
```

> ***Note:*** *This will generate a `build/windows/` directory in the **project's root directory** with the build output.*

### Project Generation (Optional)

#### Visual studio
If you want to generate a Visual Studio project, run the following command:
```bat
xmake project -k vsxmake
```

> ***Note:*** *This will generate a `vsxmakeXXXX/` directory in the **project's root directory** using the latest version of Visual Studio installed on the system.*

#### VSCode
If you want to generate a compile_commands.json (for use with vscode for example), run the following command:
```bat
xmake project -k compile_commands --lsp=clangd
```

> ***Note:*** *This will generate a `compile_commands.json` file in the **project's root directory**.*

Add this to `.vscode/c_cpp_properties.json` (Requires extension ms-vscode.cpptools)
```json
{
    "configurations": [
        {
            //...existing configuration
            "compileCommands": "${workspaceFolder}/compile_commands.json"
        }
    ],
    "version": 4
}
```
