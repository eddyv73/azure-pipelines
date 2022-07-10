FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /src
COPY ["../Pipelines/BaseDocker/VoyagerApi/VoyagerApi.csproj", "VoyagerApi/"]
RUN dotnet restore "VoyagerApi/VoyagerApi.csproj"
COPY . .
WORKDIR "/src/VoyagerApi"
RUN dotnet build "VoyagerApi.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "VoyagerApi.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "VoyagerApi.dll"]
