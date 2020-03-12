# Migration Guide to SAFE v2

1. install dotnet SDK 3.1.101
1. `dotnet new globaljson --sdk-version 3.1.101`
1. `dotnet new tool-manifest`
1. `dotnet tool install fake-cli`
1. `dotnet tool install paket`
1. use Saturn for Server (Suave deprecated, Giraffe comes with Saturn)
1. update Server to .net core 3.1
1. paket.dependencies - remove `storage: none` for main group
1. install SAFE; SAFE.Client; SAFE.Server projects
1. paket simplify
1. install @theimowski/safe package
1. npm simplify? npm-dedupe?
1. add Version.fs to Client
1. move webpack.config.js to root
1. set webpack port to 8080
1. create `safe.fsx`
1. create Shared.fsproj and reference it from Client and Server