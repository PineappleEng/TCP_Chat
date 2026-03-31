# TCP_Chat

TCP Chat Application built with C# and WinForms.

## Overview

`TCP_Chat` is a multi-project C# solution that implements a TCP-based chat system with a Windows Forms client UI and a dedicated server component.

> **Note:** This repository was developed as a school project for learning purposes.

Repository: https://github.com/PineappleEng/TCP_Chat

## Solution Structure

This repository is organized as a Visual Studio solution:

- `ChatApp.sln` — root solution file
- `Client/` — WinForms client application
- `Server/` — TCP chat server logic
- `Common/` — shared classes/models/network code used across projects

### Notable Files

- `Client/Client.csproj`
- `Client/MainForm.cs`
- `Client/Program.cs`
- `Server/Server.csproj`
- `Server/ChatServer.cs`
- `Server/Security.cs`
- `Common/Common.csproj`
- `LICENSE.txt` (MIT License)

## Tech Stack

- **Language:** C# (100%)
- **Framework:** .NET (Visual Studio project format with `packages.config`)
- **UI:** Windows Forms
- **Networking:** TCP sockets (`System.Net.Sockets`)

## Prerequisites

- Windows (required for WinForms client)
- Visual Studio 2022 or newer (recommended)
- .NET developer workload installed in Visual Studio
- NuGet package restore enabled

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/PineappleEng/TCP_Chat.git
   cd TCP_Chat
   ```

2. **Open the solution**
   - Open `ChatApp.sln` in Visual Studio.

3. **Restore NuGet packages**
   - Visual Studio should restore automatically.
   - If needed: right-click solution → **Restore NuGet Packages**.

4. **Build the solution**
   - Build → **Build Solution**.

5. **Run the server**
   - Set `Server` as startup project (or start it first).
   - Launch and verify it is listening.

6. **Run the client**
   - Set `Client` as startup project (or use multiple startup projects).
   - Connect to the server endpoint and begin chatting.

## Recommended Debug Setup (Visual Studio)

For local testing with both apps:

1. Right-click solution → **Set Startup Projects…**
2. Choose **Multiple startup projects**
3. Set both:
   - `Server` → Start
   - `Client` → Start

Optionally start multiple client instances for chat testing.

## Configuration Notes

Configuration files present in the repo:

- `Client/App.config`
- `Server/App.config`
- `Common/app.config`

Use these files (and/or relevant source files) to adjust runtime settings such as host, port, and other app behavior.

## Project Roles

- **Server**
  - Handles TCP listener and client connection management.
  - Core implementation centered in `Server/ChatServer.cs`.
  - Includes security-related helper logic in `Server/Security.cs`.

- **Client**
  - Windows Forms UI for connecting and messaging.
  - Main form logic in `Client/MainForm.cs`.

- **Common**
  - Shared models and networking abstractions in:
    - `Common/Models/`
    - `Common/Network/`

## License

This project is licensed under the **MIT License**.  
See [`LICENSE.txt`](./LICENSE.txt).

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a pull request
