In development environment, asp.net core will use HMR (HotModuleReplacement) to push
changes to brower automatically.

if (env.IsDevelopment())
{
    app.UseDeveloperExceptionPage();
    // webpack will automatically compile js and css when they are changed
    // add push the changes to brower.
    app.UseWebpackDevMiddleware(new WebpackDevMiddlewareOptions {
        HotModuleReplacement = true
    });
}


## Set env in Windows
* Current session
    > set ASPNETCORE_ENVIRONMENT="Development"
* Machine level
    Control Panel > System > Advanced Settings > add environment variables

## Set env in Mac or Linux
* Current session
    $ export ASPNETCORE_ENVIRONMENT=Development
* Machine level
    $code ~/.bash_profile
    add 
    export ASPNETCORE_ENVIRONMENT=Development
 
Use dotnet-watch to restart server when server side files changed
add referenct to .csproj 
```xml
<ItemGroup>
    <DotNetCliToolReference Include="Microsoft.DotNet.Watcher.Tools" Version="1.0.0" />
</ItemGroup>
```
$ dotnet watch
$ dotnet watch run
