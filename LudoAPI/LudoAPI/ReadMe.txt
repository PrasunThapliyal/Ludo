
20 Apr 2020
===========

Trying to create an API project for Ludo board game

Project Creation:
    1. Visual Studio 2019 
        -> New Project 
        -> ASP.NET Core Web Application -> LudoAPI
        -> .NET Core + ASP.NET Core 3.1 + Configure for HTTPS + Enable Docker Support + Linux
        -> API -> Create

Pre-requisites
    1. Docker Desktop

Container Tools kick in immediately, without any user action. It'll download the necessary nugets and docker images
Logs:
        ========== Checking for Container Prerequisites ==========
        Verifying that Docker Desktop is installed...
        Docker Desktop is installed.
        ========== Verifying that Docker Desktop is running... ==========
        Verifying that Docker Desktop is running...
        Docker Desktop is running.
        ========== Verifying Docker OS ==========
        Verifying that Docker Desktop's operating system mode matches the project's target operating system...
        Docker Desktop's operating system mode matches the project's target operating system.
        ========== Pulling Required Images ==========
        Checking for missing Docker images...
        Pulling Docker images. To cancel this download, close the command prompt window.
        docker pull mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim
        docker pull mcr.microsoft.com/dotnet/core/sdk:3.1-buster
        Docker images are ready.
        ========== Warming up container(s) for LudoAPI ==========
        Starting up container(s)...
        docker build -f "C:\Temp\Apps\LudoAPI\LudoAPI\Dockerfile" --force-rm -t ludoapi:dev --target base  --label "com.microsoft.created-by=visual-studio" --label "com.microsoft.visual-studio.project-name=LudoAPI" "C:\Temp\Apps\LudoAPI" 
        Sending build context to Docker daemon  18.94kB

        Step 1/6 : FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS base
         ---> bfd97e47831a
        Step 2/6 : WORKDIR /app
         ---> Running in b3f81428e823
        Removing intermediate container b3f81428e823
         ---> 1fecdb997675
        Step 3/6 : EXPOSE 80
         ---> Running in 978fe2ad3ac9
        Removing intermediate container 978fe2ad3ac9
         ---> 9ad90e94cbae
        Step 4/6 : EXPOSE 443
         ---> Running in 180b401a434a
        Removing intermediate container 180b401a434a
         ---> 63ffd53e7093
        Step 5/6 : LABEL com.microsoft.created-by=visual-studio
         ---> Running in 2bb5fd067f0d
        Removing intermediate container 2bb5fd067f0d
         ---> 07dc3a44ad59
        Step 6/6 : LABEL com.microsoft.visual-studio.project-name=LudoAPI
         ---> Running in 3bd95d4afbde
        Removing intermediate container 3bd95d4afbde
         ---> 87d7e1f56a39
        Successfully built 87d7e1f56a39
        Successfully tagged ludoapi:dev
        SECURITY WARNING: You are building a Docker image from Windows against a non-Windows Docker host. All files and directories added to build context will have '-rwxr-xr-x' permissions. It is recommended to double check and reset permissions for sensitive files and directories.
        C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe -NonInteractive -NoProfile -WindowStyle Hidden -ExecutionPolicy RemoteSigned -File "C:\Users\pthapliy\AppData\Local\Temp\1\GetVsDbg.ps1" -Version vs2017u5 -RuntimeID linux-x64 -InstallPath "C:\Users\pthapliy\vsdbg\vs2017u5"
        Info: Using vsdbg version '16.5.20303.1'
        Info: Using Runtime ID 'linux-x64'
        Info: C:\Users\pthapliy\vsdbg\vs2017u5 exists, deleting.
        Info: Successfully installed vsdbg at 'C:\Users\pthapliy\vsdbg\vs2017u5'
        C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe -NonInteractive -NoProfile -WindowStyle Hidden -ExecutionPolicy RemoteSigned -File "C:\Users\pthapliy\AppData\Local\Temp\1\GetVsDbg.ps1" -Version vs2017u5 -RuntimeID linux-musl-x64 -InstallPath "C:\Users\pthapliy\vsdbg\vs2017u5\linux-musl-x64"
        Info: Using vsdbg version '16.5.20303.1'
        Info: Using Runtime ID 'linux-musl-x64'
        Info: Successfully installed vsdbg at 'C:\Users\pthapliy\vsdbg\vs2017u5\linux-musl-x64'
        docker run -dt -v "C:\Users\pthapliy\vsdbg\vs2017u5:/remote_debugger:rw" -v "C:\Temp\Apps\LudoAPI\LudoAPI:/app" -v "C:\Temp\Apps\LudoAPI:/src/" -v "C:\Users\pthapliy\AppData\Roaming\Microsoft\UserSecrets:/root/.microsoft/usersecrets:ro" -v "C:\Users\pthapliy\AppData\Roaming\ASP.NET\Https:/root/.aspnet/https:ro" -v "C:\Users\pthapliy\.nuget\packages\:/root/.nuget/fallbackpackages2" -v "C:\Program Files\dotnet\sdk\NuGetFallbackFolder:/root/.nuget/fallbackpackages" -e "DOTNET_USE_POLLING_FILE_WATCHER=1" -e "ASPNETCORE_LOGGING__CONSOLE__DISABLECOLORS=true" -e "ASPNETCORE_ENVIRONMENT=Development" -e "ASPNETCORE_URLS=https://+:443;http://+:80" -e "NUGET_PACKAGES=/root/.nuget/fallbackpackages2" -e "NUGET_FALLBACK_PACKAGES=/root/.nuget/fallbackpackages;/root/.nuget/fallbackpackages2" -P --name LudoAPI --entrypoint tail ludoapi:dev -f /dev/null 
        862f6a783f76b5d321a31fbd3ff7c5eeae043d59fa9c80e00d6cbc0f9c6f9cd0
        Container started successfully.
        ========== Finished ==========

