# Repository Content
Library to implement authorization application logics

[![Build Status](https://garaproject.visualstudio.com/UmbrellaFramework/_apis/build/status/Umbrella.Security?branchName=main)](https://garaproject.visualstudio.com/UmbrellaFramework/_build/latest?definitionId=78&branchName=main)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=Umbrella.Security&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=Umbrella.Security)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=Umbrella.Security&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=Umbrella.Security)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=Umbrella.Security&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=Umbrella.Security)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=Umbrella.Security&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=Umbrella.Security)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=Umbrella.Security&metric=bugs)](https://sonarcloud.io/summary/new_code?id=Umbrella.Security)

# Installation
To install it, use proper command:
```
dotnet add package Umbrella.Security 
```

[![Nuget](https://img.shields.io/nuget/v/Umbrella.Security.svg?style=plastic)](https://www.nuget.org/packages/Umbrella.Security/)
[![NuGet Downloads](https://img.shields.io/nuget/dt/Umbrella.Security.svg)](https://www.nuget.org/packages/Umbrella.Security/)

For more details about download, see [NuGet Web Site](https://www.nuget.org/packages/Umbrella.Security/)

# Usage of Decorators
to decorate a specific method of a class (example: API controller) to require a claim to be executed, follow the snippet below:

```c#
        /// <summary>
        /// Reders the index view
        /// </summary>
        /// <returns></returns>
        [HttpGet]
        [ClaimsAuthorize(ClaimTypes.RANKING, "R")]
        public IActionResult Index()
        {
          .....
        }
```
