# Empty Web Content Project Template .NET Core Projects
<img src="icon.png" width="150" />

This is a .NET Web Project Template that creates a **static content only** out of the root folder. It does the following:

* Adds a `program.cs` with `void static Main()` function (required to build)
* Adds `<IsWebConfigTransformDisabled>True</IsWebConfigTransformDisabled>` to project
* Includes all root folder files (you can customize include/exclude lists)
* Excludes binaries and project files
* Adds a default WebDeploy Publishing Profile

As .NET Core Web SDK projects by default require a code entry point and publish from the `wwwroot` folder this project type publishes output from the site root. It also adds a placeholder `void static Main()` function, adds a Web Deploy template and sets up the project to allow publishing without `web.config` transformations on IIS.

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