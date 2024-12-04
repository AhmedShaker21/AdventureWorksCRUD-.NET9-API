# Use the .NET 8 SDK image
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS base
WORKDIR /app
EXPOSE 5000

FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY ["AdventureWorksPersistence/AdventureWorksPersistence.csproj", "AdventureWorksPersistence/"]
RUN dotnet restore "AdventureWorksPersistence/AdventureWorksPersistence.csproj"
COPY . .
WORKDIR "/src/AdventureWorksPersistence"
RUN dotnet build "AdventureWorksPersistence.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "AdventureWorksPersistence.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "AdventureWorksPersistence.dll"]
