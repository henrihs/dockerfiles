FROM microsoft/dotnet:2.1.402-sdk-alpine

RUN dotnet tool install -g dotnet-script

RUN apk update
RUN apk add --no-cache ca-certificates

ENV PATH="$PATH:/root/.dotnet/tools"
