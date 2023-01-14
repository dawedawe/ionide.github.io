---
title: Running your code
menu_order: 6
---

# Running your code

### Smart launch configurations

Ionide generates VSCode [Launch Configurations](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) for running and debugging each runnable project in your workspace. Generally this means projects with a `ProjectType` of `Exe`. These autogenerated configurations act essentially the same as running `dotnet run` in the project's directory.

Ionide will generate additional launch configurations for any projects that have a [`Properties/launchSettings.json`](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/environments?view=aspnetcore-6.0#development-and-launchsettingsjson) file. This file is often generated by Visual Studio, but can be generated manually as well. These launch settings profiles can be run by Visual Studio, `dotnet run`, `dotnet watch`, and JetBrains Rider, and now VSCode joins the bunch! Any launch settings profiles with a `commandName` of `Project` can be run, and any `applicationUrl`, `environmentVariables`, and `commandLineArgs` settings will be used.

The generated launch configurations will set a `preLaunchTask` dependency on the `Build` task for their associated project, so you'll always run the most up-to-date build before running your code.

### Running a launch configuration

To explicitly run one of the new launch configurations, choose the Debug menu, and select a configuration from the drop-down menu. From there, you're all set!