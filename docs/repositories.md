# Repositories

Each repository in the [Wahine Kai Github organization](https://github.com/wahinekai)
has a specific purpose.

## [docs](https://github.com/wahinekai/docs)

This repository holds all of the documentation for the Wahine Kai codebase.
It is published in Github Pages at [https://wahinekai.github.io/docs](https://wahinekai.github.io/docs).
It uses Jekyll to host a website based on markdown and Bootstrap 4 for styling.

## [memberdatabase-backend](https://github.com/wahinekai/memberdatabase-backend)

This repository holds the code for the backend of the Wahine Kai Member Database application.
This repository is written in C# 9 using the ASP.NET framework. The code uses .NET 5.

This repository has two projects within it - BackendHost and BackendService. BackendHost holds
the entrypoint/startup definitions, properties, and controllers for the application.
BackendService holds Service code for handling of HTTP requests.

This repository is responsible for publication of the memberdatabase-backend package.
This package is a Docker container. A development container (tagged 'dev') is built
automatically on a push to master (using GitHub actions).

## [memberdatabase-azureadconnector](https://github.com/wahinekai/memberdatabase-azureadconnector)

Wahine Kai's member database application uses Azure AD B2C to authenticate & authorize users
throughout the application. This service holds user data in Azure AD. On sign up to the application,
it calls this API. This API then lets Azure AD know whether user sign up should be allowed.
This repository is written in C# 9 using the ASP.NET framework. The code uses .NET 5.

This repository has two projects within it - AzureAdConnectorHost and AzureAdConnectorService.
AzureAdConnectorHost holds the entrypoint/startup definitions, properties, and controllers for the application.
AzureAdConnectorService holds Service code for handling of HTTP requests.

This repository is responsible for publication of the memberdatabase-frontend package.
This package is a Docker container. A development container (tagged 'dev') is built
automatically on a push to master (using GitHub actions).

## See Also

See [Deployment](/deployment.md) for details on how this application is deployed.

See [TypeScript Development](/typescript-development.md) for details on how to get started
developing in TypeScript.

See [C# Development](/csharp-development.md) for details on how to get started
developing in C#.
