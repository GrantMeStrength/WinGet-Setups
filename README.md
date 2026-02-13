# Setting up your development system

This catalog lists `winget` commands to install core tools for common developer environments on Windows. Use an elevated terminal for installs that require administrator permissions. You can add `--accept-source-agreements --accept-package-agreements` to reduce prompts.

Tip: verify package IDs with `winget search <name>` before installing.

## Essentials (recommended for most developers)

- Windows Terminal
- Visual Studio Code
- Git
- GitHub CLI

```powershell
winget install --id Microsoft.WindowsTerminal --accept-source-agreements --accept-package-agreements
winget install --id Microsoft.VisualStudioCode --accept-source-agreements --accept-package-agreements
winget install --id Git.Git --accept-source-agreements --accept-package-agreements
winget install --id GitHub.cli --accept-source-agreements --accept-package-agreements
```

## .NET and C-Sharp

- .NET SDK
- Visual Studio 2022 Community
- Visual Studio 2022 Build Tools (C++/MSBuild toolchain)

```powershell
winget install --id Microsoft.DotNet.SDK --accept-source-agreements --accept-package-agreements
winget install --id Microsoft.VisualStudio.2022.Community --accept-source-agreements --accept-package-agreements
winget install --id Microsoft.VisualStudio.2022.BuildTools --accept-source-agreements --accept-package-agreements
```

## Node.js and Web

- Node.js LTS
- NVM for Windows (optional; manage multiple Node versions)

```powershell
winget install --id OpenJS.NodeJS.LTS --accept-source-agreements --accept-package-agreements
winget install --id CoreyButler.NVMforWindows --accept-source-agreements --accept-package-agreements
```

## Python

- Python (CPython)
- pip (included with Python)

```powershell
winget install --id Python.Python --accept-source-agreements --accept-package-agreements
```

## Java

- Microsoft OpenJDK (17)
- Temurin OpenJDK (alternative)

```powershell
winget install --id Microsoft.OpenJDK.17 --accept-source-agreements --accept-package-agreements
winget install --id EclipseAdoptium.Temurin.17.JDK --accept-source-agreements --accept-package-agreements
```

## C++ / Native build tools

- CMake
- Ninja
- LLVM/Clang (optional)

```powershell
winget install --id Kitware.CMake --accept-source-agreements --accept-package-agreements
winget install --id Ninja-build.Ninja --accept-source-agreements --accept-package-agreements
winget install --id LLVM.LLVM --accept-source-agreements --accept-package-agreements
```

## Containers and Cloud CLI

- Docker Desktop
- Azure CLI

```powershell
winget install --id Docker.DockerDesktop --accept-source-agreements --accept-package-agreements
winget install --id Microsoft.AzureCLI --accept-source-agreements --accept-package-agreements
```

## Windows app development

- Visual Studio 2022 Community (with Windows app development workload)
- .NET SDK
- Windows App SDK (installed via Visual Studio workload or NuGet)

```powershell
winget install --id Microsoft.VisualStudio.2022.Community --accept-source-agreements --accept-package-agreements
winget install --id Microsoft.DotNet.SDK --accept-source-agreements --accept-package-agreements
```

For Windows App SDK and WinUI development:
1. During Visual Studio installation, select the **"Windows application development"** workload
2. In your project, add the `Microsoft.WindowsAppSDK` NuGet package
3. Use WinUI project templates available in Visual Studio

See [Windows App SDK documentation](https://learn.microsoft.com/windows/apps/windows-app-sdk/) for more details.

Notes:

- Visual Studio workloads can be customized during installation. Workload automation via `--override` parameters is advanced; consult Visual Studio installer docs if needed.
- Some packages may require restart.

