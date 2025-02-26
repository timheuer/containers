# Getting Started

To build a container from the SDK, add this package and run the `publish` command,
specifying the `DefaultContainer` PublishProfile. You can learn more about Publish Profiles [in the documentation](https://docs.microsoft.com/aspnet/core/host-and-deploy/visual-studio-publish-profiles?view=aspnetcore-6.0#publish-profiles).

```shell
>dotnet add package Microsoft.NET.Build.Containers --prerelease
>dotnet publish --os linux --arch x64 -p:ProfileName=DefaultContainer
...
Pushed container '<your app name>:<your app version>' to registry 'docker://'
...
```

Out of the box, this package will infer a number of properties about the generated container image, including which base image to use, which version of that image to use, and where to push the generated image. You have control over all of these properties, however. You can read more about customizing the container [here](./ContainerCustomization.md)

> **Note**
> This package only supports Linux containers in this version.

> **Note**
> This package only supports Web projects (those that use the `Microsoft.NET.Sdk.Web` SDK) in this version.