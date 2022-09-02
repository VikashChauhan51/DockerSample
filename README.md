# DockerSample
Sample Dotnet 6 Core API app with docker.
## Prerequisites
- Docker should be installed. If not then please follow [this](https://gist.github.com/VikashChauhan51/fc2dad10334dc4057a24ae23220ce506) document.
- Git should be installed.
- Visual Studio should be installed.

## Publish in Docker
- Open `src` folder in terminal.
- Execute `dotnet restore' command.
- Execute `dotnet build' command.
- Publish code by executing the command `dotnet publish -c Debug -o publish'.
- Create docker build with by executing the command `docker build -t vikashchauhan51/sample-api:1.0.0 -f Dockerfile .`.
- Deploy in docker `docker run -d -p 8080:8080 vikashchauhan51/sample-api:1.0.0`.
