#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:6.0 
ARG PUBLISH_FOLDER=publish
RUN groupadd -g 1000 provuser && \
	useradd -r -u 1000 -g provuser provuser
RUN mkdir -p /app && chown provuser /app
USER provuser
WORKDIR /app
COPY $PUBLISH_FOLDER .
EXPOSE 8080
EXPOSE 8081
ENTRYPOINT ["dotnet", "SampleAPI.dll"]
