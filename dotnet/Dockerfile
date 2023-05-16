#Build image base
FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build-env
ENV ASPNETCORE_ENVIRONMENT=production DOTNET_PRINT_TELEMETRY_MESSAGE=false
ARG Configuration=Release
WORKDIR /build
COPY /backend/ .
WORKDIR /build/src
ENTRYPOINT tail -f /dev/null