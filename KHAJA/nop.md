nopCommerce by .NET-7
---------------------
* Source Code [ReferHere](https://github.com/nopSolutions/nopCommerce.git)
* to install .NET-7 on ubuntu-22.04 [ReferHere](https://learn.microsoft.com/en-us/dotnet/core/install/linux-ubuntu#2204-microsoft-package-feed)
* Trying to understand the Dockerfile Commands by manualy running the commands.
  1. `dotnet restore NopCommerce.sln` : The dotnet `restore` command uses NuGet to restore dependencies as well as project-specific tools.
  [ReferHere](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-restore)
  
  2. `dotnet build Nop.Web.csproj -c Release` : The dotnet build command builds the project and its dependencies into a set of binaries. The binaries include the project's code in Intermediate Language (IL) files with a .dll extension.
  [ReferHere](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-build)

  3. `dotnet publish Nop.Web.csproj -c Release -o /app/published` : dotnet publish compiles the application, reads through its dependencies specified in the project file, and publishes the resulting set of files to a directory.
  [ReferHere](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-publish#description)

  4. `.csproj` file: It contains information about all the files used in the project, assemblies used(including the path for other then provided assemblies), output type, assembly name and much more.So, by opening this xml, you can find all the info in under one roof.