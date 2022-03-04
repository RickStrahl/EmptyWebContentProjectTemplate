# Empty Web Content Project Template .NET Core Projects
<img src="icon.png" width="150" />

.NET currently doesn't have an obvious content only Web project. If you have a static Web Site that contains only static resources in a root folder and below, there's no easy way to include a project in a .NET solution.

This is a .NET Web Project Template that creates a **static content only Web Site** that publishes out of the root folder and allows a static content project to 'work' without errors when the Solution  is built.

It does the following:

* Adds a `program.cs` with `void static Main()` function (required to build)
* Adds `<IsWebConfigTransformDisabled>True</IsWebConfigTransformDisabled>` to project
* Publishes all root folder files (you can customize include/exclude lists)
* Supports Publishing via WebDeploy to IIS out of the box
* Excludes binaries and project files
* Adds a default WebDeploy Publishing Profile

For more info and reasoning behind this template, please see the following detailed blog post:

* [Creating a Static Web Content Project for Publishing with WebDeploy](https://weblog.west-wind.com/posts/2022/Mar/03/Creating-a-Static-Web-Content-Project-for-Publishing-WebDeploy)

## Usage
This project template is [installable via NuGet](https://www.nuget.org/packages/EmptyWebContentProject.Template/):

**Install the Template**

```ps
dotnet new -i EmptyWebContentProject.Template
```

**Use the Template**

```ps
md MyProject
cd MyProject

dotnet new EmptyWebContentProject

# Open your IDE or editor
code . 
```