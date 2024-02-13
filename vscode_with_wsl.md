###Vscode with WSL

#####Install Dotnet
- snap install dotnet-sdk --classic

#####Create Console App
- dotnet new console --framework net8.0 --use-program-main

#####Xunit Setup
1) dotnet add package xunit
2) dotnet add package xunit.runner.visualstudio
3) dotnet add package Microsoft.NET.Test.Sdk

#####Build Process
- If Build fails with the following error:
`error CS0017: Program has more than one entry point defined.`
Add the following line to <PropertyGroup> section of the csproj file:
`<StartupObject>"namespace"."class with Main()"</StartupObject>`


#####Code Complete
1) Install extension "C#" in WSL
2) Open Settings-->Extensions-->C#-->OmniSharpe (may require restart of vscode)
3) Under "User", check `Dotnet > Server: Use OmniSharp`
4) Restart vscode and the language server will be installed, code complete function will be enabled
