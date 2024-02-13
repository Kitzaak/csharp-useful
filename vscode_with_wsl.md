Vscode with WSL

Install Dotnet
- snap install dotnet-sdk --classic

Create Console App
- dotnet new console --framework net8.0 --use-program-main

Xunit Setup
1) dotnet add package xunit
2) dotnet add package xunit.runner.visualstudio
3) dotnet add package Microsoft.NET.Test.Sdk

If Build fails with the following error:
`error CS0017: Program has more than one entry point defined.`
Add the following line to <PropertyGroup> section of the csproj file:
`<StartupObject>"namespace"."class with Main()"</StartupObject>`
