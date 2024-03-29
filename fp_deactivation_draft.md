# Fp Deactivation Processor
---
It's a service which runs daily to deactivate/activate fp's paid base packages.

### Documentation
---
See the docs folder for more detailed instructions and additional documentation.
### Features
---
 - Demo package expiry
 - Paid package expiry
 - Sends warnings to grace period expiry (within 1, 7, 30, 60 days)
 - Activation of packages. 
 - Expires the call tracker of the fp
### Installation
---

#### Requirements

 - Windows/ Linux / MacOS
 - .NET Core 2.0 (target framework)

#### Setup

Restore packages and build the project using Visual Studio or dotnet CLI.
 - `dotnet restore ./FPDeactivationProcessor.csproj`
 - `dotnet build ./FPDeactivationProcessor.csproj`
#### Run 
 - `dotnet run ./FPDeactivationProcessor.csproj`

### Dependencies
--- 


| Dependency        | Description           | Link
| ------------- |:------------------------:| :------------------:|
| MovingFloats.API.Plugin | Plugin to get partner related details      |    https://nuget.withfloats.com/packages/MovingFloats.API.Plugin/
| MovingFloats.Server.Model2 | Contains DTOs and DAOs    |   https://nuget.withfloats.com/packages/MovingFloats.Server.Model2/
| MovingFloats.API.Model | Contains DTOs and DAOs    |   https://nuget.withfloats.com/packages/WithFloats.API.Model/

#### Package Sources
| Name        | Source           
| ------------- |:------------------------:|
|WithFloats|https://nuget.withfloats.com/api/v2
|Nuget| https://api.nuget.org/v3/index.json

___

### Deployment to production

 - `dotnet publish ./FPDeactivationProcessor.csproj -c Release`
 - Use `./bin/Release/netcoreapp2.0/FPDeactivationProcessor.dll` to run the application.

### Known Limitations
 - `MaxDegreeOfParallelism` for Parallel loops have been set to 10 due to memory issues in the current instance. 