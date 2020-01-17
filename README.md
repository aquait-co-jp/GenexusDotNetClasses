# GeneXus Standard Classes for .NET and .NET Core
GeneXus Standard Classes for .NET and .NET Core generators.

### Build status
| Branch | Status
|---|---
|master|[![](https://github.com/genexuslabs/dotnetclasses/workflows/Build/badge.svg?branch=master)](https://github.com/genexuslabs/dotnetclasses/actions?query=workflow%3ABuild+branch%3Amaster)
|beta|[![](https://github.com/genexuslabs/dotnetclasses/workflows/Build/badge.svg?branch=beta)](https://github.com/genexuslabs/dotnetclasses/actions?query=workflow%3ABuild+branch%3Abeta)

## Modules

| Name  | Description | .NET Package Name | .NET Core Package Name
|---|---|---|---
| GxEncrypt | Classes common to .NET and .NET Core related to encryption based on Twofish algorithm | GeneXus.Encrypt | GeneXus.Encrypt
| DynService.Core | Provide data types to support DynamoDB, OData and Fabric | GeneXus.DynService.Core | N/A
| DynService.DynamoDB | Provide classes that support Amazon DynamoDB | GeneXus.DynService.DynamoDB | N/A
| DynService.Fabric | Provide classes that support Hyperledger Fabric storage | GeneXus.DynService.Fabric | N/A
| DynServiceOData | Provide classes that support Microsoft OData protocol | GeneXus.DynService.OData | N/A
| GxClasses.Win | Provide classes to support windows operative system interaction such has MessageBox and Shell function | GeneXus.Classes.Win | N/A
| GxClasses | Core classes related to data access, presentation views and data types used by generated code | GeneXus.Classes | GeneXus.Classes.Core
| GxExcel | Provide classes that support Excel data type | GeneXus.Excel | GeneXus.Excel.Core
| GxMail | Provide classes that support Mail data type | GeneXus.Mail | GeneXus.Mail.Core
| GxMaps | Provide classes that support Map data type | GeneXus.Maps | GeneXus.Maps.Core
| GxPdfReportsCS | Provides classes related to PDF manipulation | GeneXus.PdfReportsCS | GeneXus.PdfReportsCS.Core
| GxSearch | Provides classes related to full text search | GeneXus.Search | GeneXus.Search.Core
| GxWebSocket | Provides classes related to notifications | GeneXus.WebSockets | GeneXus.WebSockets.Core
| StoreManager | Provides classes related to push notifications | GeneXus.StoreManager | GeneXus.StoreManager.Core
| Artech.Genexus.SDAPI | Provides classes related to smart devices push notifications | GeneXus.SDAPI | GeneXus.SDAPI.Core
| GxMemcached | Provides support for manipulation of the distributed memory object cached system Memcached | GeneXus.Memcached | GeneXus.Memcached.Core
| GxRedis | Provides support for manipulation of the distributed memory object cached system Redis | GeneXus.Redis | GeneXus.Redis.Core
| GXAmazonS3 | Provides classes related to Amazon Simple Storage Service | GeneXus.AmazonS3 | GeneXus.AmazonS3.Core
| GXAzureStorage | Provides classes related to Azure Store service | GeneXus.Azure | N/A
| GXBluemix | Provides classes related to Bluemix platform | GeneXus.Bluemix | N/A
| GXGoogleCloud | Provides classes related to Google Cloud Platform | GeneXus.Google.Cloud | N/A
| GXOpenStack | Provides classes related to Open Stack Platform | GeneXus.OpenStack | N/A
| Reor | Executable utility to execute reorganization | GeneXus.Reorganization | GeneXus.Reorganization.Core
| GxSetFrm | Executable utility to handle GXPRN.INI (reports configuration file) | GeneXus.SetFrm | GeneXus.SetFrm
| GxConfig | Executable utility to update web.config | GeneXus.Config | N/A
| GxDataInitialization | Executable utility to support dynamic transactions initialization at impact process | GeneXus.DataInitialization | GeneXus.DataInitialization.Core

This repository contains projects for .NET and .NET CORE. It uses the following directory structure:

```
├── .editorconfig (configuration for visual studio)
├── README.md (this file)
├── dotnet/ 
    ├── src/
        ├── dotnetcommon/ (Shared projects that build for both TargetFrameworks: dotnet and dotnetcore)
        ├── dotnetcore/ (.NET Core projects, many of them share sources with dotnetframework projects)
        └── dotnetframework/ (.NET projects)
    ├── Directory.Build.props (default common configuration for all the projects, imported early in the import order)
    ├── Directory.Build.targets (configuration for particular projects, imported late in the build order)
    ├── DotNetStandardClasses.sln (solution to build all the projects)
    └── StandardClasses.ruleset (Code analysis rulesets)
```

# How to build

## Requirements
- Visual Studio 2019 >= 16.3
- dotnet SDK >= 3.1 
- .Net framework >= 4.6 

# Instructions

## How to build all projects?
- ```dotnet build DotNetStandardClasses.sln```

## How to build a specific project?
- ```dotnet build project.csproj```

## How to copy assemblies to build directory?
- ```dotnet msbuild /t:build;CopyAssemblies DotNetStandardClasses.sln```

It copies the .NET assemblies to the folder build/*gxnet/bin* and .NET CORE assemblies to build/*gxnetcore/bin*

## License

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
