# Client Credential Flow Sample and Test

**Version:** 1.3.6

[![Build Status](https://dev.azure.com/osieng/engineering/_apis/build/status/product-readiness/ADH/aveva.sample-adh-authentication_client_credentials-dotnet?branchName=main)](https://dev.azure.com/osieng/engineering/_build/latest?definitionId=2582&branchName=main)

This client uses the OAuth2/OIDC Client Credential Flow to obtain an access token. See the main Cds Authentication samples page [README](https://github.com/AVEVA/AVEVA-Samples-CloudOperations/blob/main/docs/AUTHENTICATION.md) for more information about this flow.

## Requirements

- .NET 6.0 or later
  - Note: Visual Studio 2022 (v17.1) or later is required for development against .NET 6.0

The sample is configured using the file [appsettings.placeholder.json](ClientCredentialFlow/appsettings.placeholder.json). Before editing, rename this file to `appsettings.json`. This repository's `.gitignore` rules should prevent the file from ever being checked in to any fork or branch, to ensure credentials are not compromised.

Replace the placeholders in the `appsettings.json` file with your Tenant Id, Client Id and Client Secret, and the current Api Version. There is no need to replace the Namespace Id for this sample.

Developed against DotNet 6.0.

## Running the sample

### Prerequisites

- Register a Client Credential client in Cds.
- Replace the placeholders in the `appsettings.json` file with your Tenant Id, Client Id, and Client Secret obtained from registration.
- Note: As a test, a request is made against the users endpoint. If the tenant being used has strict mode enabled and the client does not have Tenant Admin permissions, the test will fail. In this case, it is recommended to change the url to a type or a stream that the client has permission to access. 

### Using Visual Studio

- Load the .csproj
- Rebuild project
- Run it
  - If you want to see the token and other outputs from the program, put a breakpoint at the end of the main method and run in debug mode

### Using Command Line

- Make sure you have the install location of dotnet added to your path
- Run the following command from the location of this project:

```shell
dotnet run
```

## Running the automated test

### Test Using Visual Studio

- Load the .csproj from the ClientCredentialFlowTest directory above this in Visual Studio
- Rebuild project
- Open Test Explorer and make sure there is one test called Test1 showing
- Run the test

### Test Using Command Line

- Make sure you have the install location of dotnet added to your path
- Run the following command from the location of the ClientCredentialFlowTest project:

```shell
dotnet test
```

---

Tested against DotNet 6.0

For the main Cds Authentication samples page [ReadMe](https://github.com/AVEVA/AVEVA-Samples-CloudOperations/blob/main/docs/AUTHENTICATION.md)  
For the main Cds samples page [ReadMe](https://github.com/AVEVA/AVEVA-Samples-CloudOperations)  
For the main AVEVA samples page [ReadMe](https://github.com/AVEVA/AVEVA-Samples)
