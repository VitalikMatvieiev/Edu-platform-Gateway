# Edu-platform_Gateway

This is the Api-Gateway project for the online learning platform. Its purpose is to handle all the requests and transfer them to the proper Web APIs.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Api-Gateway project serves as the central hub for managing and routing requests in the online learning platform. Its primary responsibility is to handle incoming requests and efficiently transfer them to the appropriate Web APIs within the system. This helps to streamline communication and ensure seamless interactions between different components of the online learning platform.

## Getting Started

Explain how to get the project up and running on a local machine.

### Prerequisites

The Project works on .Net 6 and is using next libraries:
- Ocelot - the most importang NuGet Package, that handles all the routes and settings of gateway. 

### Installation
If You are using the other than Windows operating system (Linux / MacOS) You will possibly be needed to install the .Net 6 on Your machine.
You can do that by following one of the next guides:
- https://learn.microsoft.com/en-us/dotnet/core/install/macos
- https://www.youtube.com/watch?v=Jr0XGKHoYU0&ab_channel=MainlyWebStuff
- https://maartenmerken.medium.com/installing-net-6-alpha-on-your-m1-mac-23a35aa6f02c

After that You need:

# Clone the repository
git clone https://github.com/VitalikMatvieiev/Edu-platform-Gateway.git

# Change directory
cd your-project

# Restore dependencies
dotnet restore

# Build the project
dotnet build

# Run the project
dotnet run

## Usage
All the configurations about the routing properties are stored in the "ocelot.json".

Its json file that contains information about all the connected services (List of "Routes") and "Global Configuration" with "Base Url" of the app.

The Routes are built from:
"UpstreamPathTemplate": Path for the Client to get into gateway for route in particular service,
"UpstreamHttpMethod": Allowed methods for Client to call,
"DownstreamScheme": Scheme for calling the service,
"DownstreamHostAndPorts":  Host and Port information about the service,
"DownstreamPathTemplate" Path for gateway to route to the service

## Features
