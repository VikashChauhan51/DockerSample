# DockerSample
Sample Dotnet 6 Core API app with docker.
## Prerequisites
- Docker should be installed. If not then please follow [this](https://gist.github.com/VikashChauhan51/fc2dad10334dc4057a24ae23220ce506) document.
- Git should be installed.
- Visual Studio should be installed.

## Project Structure

```
C:/DockerSample
└───src
    └───SampleAPI
        ├───Controllers
        └───Properties
```

## Run in Dev
- Run docker desktop on you system.
- Build project and run it with `docker` profile from Visual Studio.
> Here, Visual Studio will generate docker dev image and start container automatically.

## Create Docker Image from Visual Studio
- Build project from Visual Studio.
- Right click on Dockerfile and select `Build docker image` option from context menu.

## Deploy API image in Docker
- Run ` docker run -p 5000:80 -e SimpleProperty="docker!" -e ASPNETCORE_ENVIRONMENT="Development" --name=coreapi -d sampleapi` command to create container.
- http://localhost:5000/swagger/index.html