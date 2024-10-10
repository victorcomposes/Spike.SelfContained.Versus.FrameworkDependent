## 1. Publishing a .NET Application

### Framework-Dependent Deployment
In this mode, the application depends on the target machine having the .NET runtime installed.

```bash
dotnet publish -c Release --output framework-dependent-publish -r <RUNTIME_IDENTIFIER> --self-contained false
```

Replace <RUNTIME_IDENTIFIER> with the desired runtime. Some examples:

- win-x64 for Windows 64-bit
- linux-x64 for Linux 64-bit
- osx-x64 for macOS 64-bit

### Self-Contained Deployment
In this mode, the .NET runtime is bundled with the application, so no external runtime is needed on the target machine.

```bash
dotnet publish -c Release --output self-contained-publish -r <RUNTIME_IDENTIFIER> --self-contained true
```

Again, replace <RUNTIME_IDENTIFIER> with the desired runtime (examples listed above).

# 2. Common Runtime Identifiers (RIDs)

#### Windows:
- win-x64 (64-bit)
- win-x86 (32-bit)
- win-arm (ARM)
- win-arm64 (ARM64)

#### Linux:

- linux-x64 (64-bit)
- linux-arm (ARM)
- linux-arm64 (ARM64)

#### macOS:

- osx-x64 (64-bit)
- osx-arm64 (ARM64)