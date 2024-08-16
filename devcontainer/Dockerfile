# Use the official .NET image from the Microsoft Container Registry
FROM mcr.microsoft.com/dotnet/sdk:8.0

# Install additional dependencies
RUN apt-get update \
    && apt-get install -y \
       libgtk-3-dev \
       libpango1.0-dev \
       libatk1.0-dev \
       libcairo2-dev \
       libgdk-pixbuf2.0-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /workspace

# Install .NET MAUI check tool
RUN dotnet tool install -g maui-check

# Set PATH to include global tools
ENV PATH="${PATH}:/root/.dotnet/tools"
