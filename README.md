# Garmin.Connect

Unofficial dotnet garmin connect client

[![Build](https://github.com/pachman/dotnet.garmin.connect/actions/workflows/build.yml/badge.svg)](https://github.com/pachman/dotnet.garmin.connect/actions/workflows/build.yml)
[![NuGet Version](http://img.shields.io/nuget/v/Unofficial.Garmin.Connect.svg)](https://www.nuget.org/packages/Unofficial.Garmin.Connect/)
[![NuGet Downloads](http://img.shields.io/nuget/dt/Unofficial.Garmin.Connect.svg)](https://www.nuget.org/packages/Unofficial.Garmin.Connect/)

## About

This package allows you to request your device, activity and health data from your Garmin Connect account.

**WARNING!** Use the library only for personal automation without too many accounts. For other needs [request access](https://developer.garmin.com/gc-developer-program/overview/) to the developer program.

## Installation

```bash
dotnet add package Unofficial.Garmin.Connect
```

## Using

```dotnet
var login = "<garmin login>";
var password = "<garmin password>";
var authParameters = new BasicAuthParameters(login, password);

var client = new GarminConnectClient(new GarminConnectContext(new HttpClient(), authParameters));
```

## Build and publish

- build `./pack.sh`
- pack `./publish.sh`

## Tests

- set environment variables `GARMIN_LOGIN` and `GARMIN_PASSWORD`
  - JetBrains Rider `File | Settings | Build, Execution, Deployment | Unit Testing | Test Runner`

## Thanks

- The first vision from [cyberjunky/python-garminconnect](https://github.com/cyberjunky/python-garminconnect)
- Icons made by [Freepik](https://www.freepik.com) from [www.flaticon.com](https://www.flaticon.com/)
- Converter JSON to C# [app.quicktype.io](https://app.quicktype.io/)
- and [Garmin](https://connect.garmin.com) for the best devices
